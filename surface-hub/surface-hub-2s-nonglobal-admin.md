---
title: Configurer les comptes d’administrateur non global sur surface Hub 2S
description: Cet article explique comment configurer des comptes d’administrateur non globaux pour gérer surface Hub 2S.
keywords: SurfaceHub2S
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 12/07/2020
ms.localizationpriority: Medium
appliesto:
- Surface Hub 2S 2020 Update
ms.openlocfilehash: e16e4f8bd4b2b253233fa9790987287cf17966c7
ms.sourcegitcommit: 7e1b351024e33926901ddbdc562ba12aea0b4196
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385172"
---
# <a name="configure-non-global-admin-accounts-on-surface-hub-2s"></a>Configurer les comptes d’administrateur non global sur surface Hub 2S

Lorsque vous associez surface Hub 2S à un domaine Azure AD, vous pouvez configurer des comptes d’administrateur non globaux qui limitent les autorisations de gestion de l’application Paramètres sur Surface Hub 2S. Cela vous permet d’étenduer les autorisations d’administrateur pour Surface Hub 2S uniquement et d’empêcher tout accès administrateur potentiellement indésirable sur l’ensemble d’un domaine Azure AD. Avant de commencer, assurez-vous que votre Surface Hub 2S est joint à Azure AD. Si ce n’est pas le cas, vous devrez réinitialiser surface Hub 2S et terminer le premier programme d’installation OOBE (Out-of-the-box), en choisissant l’option pour rejoindre Azure AD.

## <a name="summary"></a>Résumé 

Le processus de création de comptes d’administrateur non globaux implique les étapes suivantes : 

1. Dans Microsoft Intune, créez un groupe de sécurité contenant les administrateurs désignés pour gérer surface Hub 2S.
2. Obtenez le SID du groupe Azure AD à l’aide de PowerShell.
3. Créez un fichier XML contenant le SID du groupe Azure AD.
4. Créez un groupe de sécurité contenant les appareils Surface Hub 2S qui seront gérés par le groupe de sécurité Des administrateurs non globaux.
5. Créez un profil de configuration personnalisé ciblant le groupe de sécurité qui contient vos appareils Surface Hub 2S. 


## <a name="create-azure-ad-security-groups"></a>Créer des groupes de sécurité Azure AD

Tout d’abord, créez un groupe de sécurité contenant les comptes d’administrateur. Ensuite, créez un autre groupe de sécurité pour les appareils Surface Hub.  

### <a name="create-security-group-for-admin-accounts"></a>Créer un groupe de sécurité pour les comptes d’administrateur

1. Connectez-vous à Intune via le **** Centre d’administration [Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431)sélectionnez Groupes Nouveaux groupes > et sous Type de  >  **** groupe, sélectionnez **Sécurité.** 
2. Entrez un nom de groupe (par exemple, Administrateurs locaux **du Surface Hub),** puis sélectionnez **Créer.** 

     ![Créer un groupe de sécurité pour les administrateurs hub](images/sh-create-sec-group.png)

3. Ouvrez le groupe, sélectionnez **** **Membres,** puis sélectionnez Ajouter des membres pour entrer les comptes Administrateur que vous souhaitez désigner comme administrateurs non globaux sur Surface Hub 2S. Pour en savoir plus sur la création de groupes dans Intune, voir Ajouter des [groupes pour organiser les utilisateurs et les appareils.](https://docs.microsoft.com/mem/intune/fundamentals/groups-add)

### <a name="create-security-group-for-surface-hub-2s-devices"></a>Créer un groupe de sécurité pour les appareils Surface Hub 2S

1. Répétez la procédure précédente pour créer un groupe de sécurité distinct pour les appareils Hub . par exemple, les **appareils Surface Hub.** 

     ![Créer un groupe de sécurité pour les appareils Hub](images/sh-create-sec-group-devices.png) 

## <a name="obtain-azure-ad-group-sid-using-powershell"></a>Obtenir le SID du groupe Azure AD à l’aide de PowerShell

1. Lancez PowerShell avec des privilèges de compte élevés **(exécuter**en tant qu’administrateur) et assurez-vous que votre système est configuré pour exécuter des scripts PowerShell. Pour en savoir plus, consultez la procédure [à propos des stratégies d’exécution.](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?) 
2. [Installez le module Azure PowerShell.](https://docs.microsoft.com/powershell/azure/install-az-ps)
3. Connectez-vous à votre client Azure AD.

    ```powershell
    Connect-AzureAD
    ```

4. Lorsque vous êtes inscrit à votre client, exécutez l’let de commande suivant. Il vous invite à « Veuillez taper l’ID d’objet de votre groupe Azure AD ».

    ```powershell
    function Convert-ObjectIdToSid
    {    param([String] $ObjectId)   
         $d=[UInt32[]]::new(4);[Buffer]::BlockCopy([Guid]::Parse($ObjectId).ToByteArray(),0,$d,0,16);"S-1-12-1-$d".Replace(' ','-')
         
    }
    ```

5. Dans Intune, sélectionnez le groupe que vous avez créé précédemment et copiez l’ID d’objet, comme illustré dans la figure suivante. 

     ![Copier l’ID d’objet du groupe de sécurité](images/sh-objectid.png)

6. Exécutez l’let de commande suivante pour obtenir le SID du groupe de sécurité :

    ```powershell
    $AADGroup = Read-Host "Please type the Object ID of your Azure AD Group"
    $Result = Convert-ObjectIdToSid $AADGroup
    Write-Host "Your Azure Ad Group SID is" -ForegroundColor Yellow $Result
    ```
    
7. Collez l’ID d’objet dans l’let de commande PowerShell, appuyez sur **Entrée,** puis copiez le SID du groupe **Azure AD** dans un éditeur de texte. 

## <a name="create-xml-file-containing-azure-ad-group-sid"></a>Créer un fichier XML contenant le SID du groupe Azure AD

1. Copiez ce qui suit dans un éditeur de texte : 

    ```xml
      <groupmembership>   
      <accessgroup desc = "Administrators">        
      <member name = "Administrator" />        
      <member name = "S-1-12-1-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX" />  
      </accessgroup>
      </groupmembership>
      ```

2. Remplacez le SID d’espace réservé (à partir de S-1-12-1) par votre SID de groupe **Azure AD,** puis enregistrez le fichier au XML . par exemple, **aad-local-admin.xml**. 

## <a name="create-custom-configuration-profile"></a>Créer un profil de configuration personnalisé

1. Dans endpoint Manager, sélectionnez **Profils de**  >  **configuration des appareils**Créer un  >  **profil.** 
2. Sous Plateforme, **sélectionnez Windows 10 et les ultérieures.** Sous Profil, **sélectionnez Personnalisé,** puis **Créer.**
3. Ajoutez un nom et une description, puis sélectionnez **Suivant.**
4. Sous **Paramètres de configuration**  >  **OMA-URI, sélectionnez** **Ajouter.**
5. Dans le volet Ajouter une ligne, ajoutez un nom et sous     **OMA-URI**, ajoutez la chaîne suivante : 

    ```OMA-URI
    ./Device/Vendor/MSFT/Policy/Config/RestrictedGroups/ConfigureGroupMembership
    ```
6. Sous Type de données, **sélectionnez Chaîne XML** et recherchez le fichier XML que vous avez créé à l’étape précédente. 

     ![télécharger le fichier de config xml d’administration local](images/sh-local-admin-config.png)

7. Cliquez sur **Enregistrer**.
8. Cliquez **sur Sélectionner les groupes à inclure et** choisissez le groupe de sécurité que vous avez créé [précédemment](#create-security-group-for-surface-hub-2s-devices) **(appareils Surface Hub).** Cliquez sur **Suivant**.
9. Sous règles d’applicabilité, ajoutez une règle si vous le souhaitez. Dans le cas contraire, **sélectionnez Suivant,** puis **Créer.**

Pour en savoir plus sur les profils de configuration personnalisés à l’aide de chaînes OMA-URI, voir Utiliser des paramètres personnalisés pour les appareils [Windows 10 dans Intune.](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10)


## <a name="non-global-admins-managing-surface-hub-2s"></a>Administrateurs non globaux gérant Surface Hub 2S

Les membres du groupe Sécurité des **administrateurs** locaux du Surface Hub peuvent désormais se connecter à l’application Paramètres sur Surface Hub 2S et gérer les paramètres.
