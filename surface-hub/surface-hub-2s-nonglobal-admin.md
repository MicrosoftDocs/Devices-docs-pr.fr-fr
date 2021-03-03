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
# <a name="configure-non-global-admin-accounts-on-surface-hub-2s"></a><span data-ttu-id="64572-104">Configurer les comptes d’administrateur non global sur surface Hub 2S</span><span class="sxs-lookup"><span data-stu-id="64572-104">Configure non Global admin accounts on Surface Hub 2S</span></span>

<span data-ttu-id="64572-105">Lorsque vous associez surface Hub 2S à un domaine Azure AD, vous pouvez configurer des comptes d’administrateur non globaux qui limitent les autorisations de gestion de l’application Paramètres sur Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="64572-105">When you join Surface Hub 2S to an Azure AD domain, you can configure non Global admin accounts that limit permissions to management of the Settings app on Surface Hub 2S.</span></span> <span data-ttu-id="64572-106">Cela vous permet d’étenduer les autorisations d’administrateur pour Surface Hub 2S uniquement et d’empêcher tout accès administrateur potentiellement indésirable sur l’ensemble d’un domaine Azure AD.</span><span class="sxs-lookup"><span data-stu-id="64572-106">This enables you to scope admin permissions for Surface Hub 2S only and prevent potentially unwanted admin access across an entire Azure AD domain.</span></span> <span data-ttu-id="64572-107">Avant de commencer, assurez-vous que votre Surface Hub 2S est joint à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="64572-107">Before you begin, make sure your Surface Hub 2S is joined to Azure AD.</span></span> <span data-ttu-id="64572-108">Si ce n’est pas le cas, vous devrez réinitialiser surface Hub 2S et terminer le premier programme d’installation OOBE (Out-of-the-box), en choisissant l’option pour rejoindre Azure AD.</span><span class="sxs-lookup"><span data-stu-id="64572-108">If not, you will need to reset Surface Hub 2S and complete the first-time, out-of-the-box (OOBE) setup program, choosing the option to join Azure AD.</span></span>

## <a name="summary"></a><span data-ttu-id="64572-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="64572-109">Summary</span></span> 

<span data-ttu-id="64572-110">Le processus de création de comptes d’administrateur non globaux implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="64572-110">The process of creating non Global admin accounts involves the following steps:</span></span> 

1. <span data-ttu-id="64572-111">Dans Microsoft Intune, créez un groupe de sécurité contenant les administrateurs désignés pour gérer surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="64572-111">In Microsoft Intune, create a Security group containing the admins designated to manage Surface Hub 2S.</span></span>
2. <span data-ttu-id="64572-112">Obtenez le SID du groupe Azure AD à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64572-112">Obtain Azure AD Group SID using PowerShell.</span></span>
3. <span data-ttu-id="64572-113">Créez un fichier XML contenant le SID du groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="64572-113">Create XML file containing Azure AD Group SID.</span></span>
4. <span data-ttu-id="64572-114">Créez un groupe de sécurité contenant les appareils Surface Hub 2S qui seront gérés par le groupe de sécurité Des administrateurs non globaux.</span><span class="sxs-lookup"><span data-stu-id="64572-114">Create a Security Group containing the Surface Hub 2S devices that will be managed by the non-Global admins Security group.</span></span>
5. <span data-ttu-id="64572-115">Créez un profil de configuration personnalisé ciblant le groupe de sécurité qui contient vos appareils Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="64572-115">Create a custom Configuration profile targeting the security group that contains your Surface Hub 2S devices.</span></span> 


## <a name="create-azure-ad-security-groups"></a><span data-ttu-id="64572-116">Créer des groupes de sécurité Azure AD</span><span class="sxs-lookup"><span data-stu-id="64572-116">Create Azure AD security groups</span></span>

<span data-ttu-id="64572-117">Tout d’abord, créez un groupe de sécurité contenant les comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="64572-117">First create a security group containing the admin accounts.</span></span> <span data-ttu-id="64572-118">Ensuite, créez un autre groupe de sécurité pour les appareils Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="64572-118">Then create another security group for Surface Hub devices.</span></span>  

### <a name="create-security-group-for-admin-accounts"></a><span data-ttu-id="64572-119">Créer un groupe de sécurité pour les comptes d’administrateur</span><span class="sxs-lookup"><span data-stu-id="64572-119">Create security group for Admin accounts</span></span>

1. <span data-ttu-id="64572-120">Connectez-vous à Intune via le \*\*\*\* Centre d’administration [Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431)sélectionnez Groupes Nouveaux groupes > et sous Type de  >  \*\*\*\* groupe, sélectionnez **Sécurité.**</span><span class="sxs-lookup"><span data-stu-id="64572-120">Sign into Intune via the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select **Groups** > **New Group** > and under Group type, select **Security.**</span></span> 
2. <span data-ttu-id="64572-121">Entrez un nom de groupe (par exemple, Administrateurs locaux **du Surface Hub),** puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="64572-121">Enter a Group name -- for example, **Surface Hub Local Admins** -- and then select **Create.**</span></span> 

     ![Créer un groupe de sécurité pour les administrateurs hub](images/sh-create-sec-group.png)

3. <span data-ttu-id="64572-123">Ouvrez le groupe, sélectionnez \*\*\*\* **Membres,** puis sélectionnez Ajouter des membres pour entrer les comptes Administrateur que vous souhaitez désigner comme administrateurs non globaux sur Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="64572-123">Open the group, select **Members**, and then choose **Add members** to enter the Administrator accounts that you wish to designate as non Global admins on Surface Hub 2S.</span></span> <span data-ttu-id="64572-124">Pour en savoir plus sur la création de groupes dans Intune, voir Ajouter des [groupes pour organiser les utilisateurs et les appareils.](https://docs.microsoft.com/mem/intune/fundamentals/groups-add)</span><span class="sxs-lookup"><span data-stu-id="64572-124">To learn more about creating groups in Intune, see  [Add groups to organize users and devices](https://docs.microsoft.com/mem/intune/fundamentals/groups-add).</span></span>

### <a name="create-security-group-for-surface-hub-2s-devices"></a><span data-ttu-id="64572-125">Créer un groupe de sécurité pour les appareils Surface Hub 2S</span><span class="sxs-lookup"><span data-stu-id="64572-125">Create security group for Surface Hub 2S devices</span></span>

1. <span data-ttu-id="64572-126">Répétez la procédure précédente pour créer un groupe de sécurité distinct pour les appareils Hub . par exemple, les **appareils Surface Hub.**</span><span class="sxs-lookup"><span data-stu-id="64572-126">Repeat the previous procedure to create a separate security group for Hub devices; for example, **Surface Hub devices**.</span></span> 

     ![Créer un groupe de sécurité pour les appareils Hub](images/sh-create-sec-group-devices.png) 

## <a name="obtain-azure-ad-group-sid-using-powershell"></a><span data-ttu-id="64572-128">Obtenir le SID du groupe Azure AD à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="64572-128">Obtain Azure AD Group SID using PowerShell</span></span>

1. <span data-ttu-id="64572-129">Lancez PowerShell avec des privilèges de compte élevés **(exécuter**en tant qu’administrateur) et assurez-vous que votre système est configuré pour exécuter des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64572-129">Launch PowerShell with elevated account privileges (**Run as Administrator**) and ensure your system is configured to run PowerShell scripts.</span></span> <span data-ttu-id="64572-130">Pour en savoir plus, consultez la procédure [à propos des stratégies d’exécution.](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?)</span><span class="sxs-lookup"><span data-stu-id="64572-130">To learn more, refer to [About Execution Policies](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?).</span></span> 
2. <span data-ttu-id="64572-131">[Installez le module Azure PowerShell.](https://docs.microsoft.com/powershell/azure/install-az-ps)</span><span class="sxs-lookup"><span data-stu-id="64572-131">[Install Azure PowerShell module](https://docs.microsoft.com/powershell/azure/install-az-ps).</span></span>
3. <span data-ttu-id="64572-132">Connectez-vous à votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="64572-132">Sign into your Azure AD tenant.</span></span>

    ```powershell
    Connect-AzureAD
    ```

4. <span data-ttu-id="64572-133">Lorsque vous êtes inscrit à votre client, exécutez l’let de commande suivant.</span><span class="sxs-lookup"><span data-stu-id="64572-133">When you're signed into your tenant, run the following commandlet.</span></span> <span data-ttu-id="64572-134">Il vous invite à « Veuillez taper l’ID d’objet de votre groupe Azure AD ».</span><span class="sxs-lookup"><span data-stu-id="64572-134">It will prompt you to "Please type the Object ID of your Azure AD Group."</span></span>

    ```powershell
    function Convert-ObjectIdToSid
    {    param([String] $ObjectId)   
         $d=[UInt32[]]::new(4);[Buffer]::BlockCopy([Guid]::Parse($ObjectId).ToByteArray(),0,$d,0,16);"S-1-12-1-$d".Replace(' ','-')
         
    }
    ```

5. <span data-ttu-id="64572-135">Dans Intune, sélectionnez le groupe que vous avez créé précédemment et copiez l’ID d’objet, comme illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="64572-135">In Intune, select the group you created earlier and copy the Object id, as shown in the following figure.</span></span> 

     ![Copier l’ID d’objet du groupe de sécurité](images/sh-objectid.png)

6. <span data-ttu-id="64572-137">Exécutez l’let de commande suivante pour obtenir le SID du groupe de sécurité :</span><span class="sxs-lookup"><span data-stu-id="64572-137">Run the following commandlet to get the security group's SID:</span></span>

    ```powershell
    $AADGroup = Read-Host "Please type the Object ID of your Azure AD Group"
    $Result = Convert-ObjectIdToSid $AADGroup
    Write-Host "Your Azure Ad Group SID is" -ForegroundColor Yellow $Result
    ```
    
7. <span data-ttu-id="64572-138">Collez l’ID d’objet dans l’let de commande PowerShell, appuyez sur **Entrée,** puis copiez le SID du groupe **Azure AD** dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="64572-138">Paste the Object id into the PowerShell commandlet, press **Enter**, and then copy the **Azure AD Group SID** into a text editor.</span></span> 

## <a name="create-xml-file-containing-azure-ad-group-sid"></a><span data-ttu-id="64572-139">Créer un fichier XML contenant le SID du groupe Azure AD</span><span class="sxs-lookup"><span data-stu-id="64572-139">Create XML file containing Azure AD Group SID</span></span>

1. <span data-ttu-id="64572-140">Copiez ce qui suit dans un éditeur de texte :</span><span class="sxs-lookup"><span data-stu-id="64572-140">Copy the following into a text editor:</span></span> 

    ```xml
      <groupmembership>   
      <accessgroup desc = "Administrators">        
      <member name = "Administrator" />        
      <member name = "S-1-12-1-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXXX" />  
      </accessgroup>
      </groupmembership>
      ```

2. <span data-ttu-id="64572-141">Remplacez le SID d’espace réservé (à partir de S-1-12-1) par votre SID de groupe **Azure AD,** puis enregistrez le fichier au XML . par exemple, **aad-local-admin.xml**.</span><span class="sxs-lookup"><span data-stu-id="64572-141">Replace the placeholder SID (beginning with S-1-12-1) with your **Azure AD Group SID** and then save the file as XML; for example, **aad-local-admin.xml**.</span></span> 

## <a name="create-custom-configuration-profile"></a><span data-ttu-id="64572-142">Créer un profil de configuration personnalisé</span><span class="sxs-lookup"><span data-stu-id="64572-142">Create Custom configuration profile</span></span>

1. <span data-ttu-id="64572-143">Dans endpoint Manager, sélectionnez **Profils de**  >  **configuration des appareils**Créer un  >  **profil.**</span><span class="sxs-lookup"><span data-stu-id="64572-143">In Endpoint Manager, select **Devices** > **Configuration profiles** > **Create profile**.</span></span> 
2. <span data-ttu-id="64572-144">Sous Plateforme, **sélectionnez Windows 10 et les ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="64572-144">Under Platform select **Windows 10 and later.**</span></span> <span data-ttu-id="64572-145">Sous Profil, **sélectionnez Personnalisé,** puis **Créer.**</span><span class="sxs-lookup"><span data-stu-id="64572-145">Under Profile, select **Custom**, and then select **Create.**</span></span>
3. <span data-ttu-id="64572-146">Ajoutez un nom et une description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="64572-146">Add a name and description and then select **Next.**</span></span>
4. <span data-ttu-id="64572-147">Sous **Paramètres de configuration**  >  **OMA-URI, sélectionnez** **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="64572-147">Under **Configuration settings** > **OMA-URI Settings**, select **Add**.</span></span>
5. <span data-ttu-id="64572-148">Dans le volet Ajouter une ligne, ajoutez un nom et sous     **OMA-URI**, ajoutez la chaîne suivante :</span><span class="sxs-lookup"><span data-stu-id="64572-148">In the Add Row pane, add a name and under     **OMA-URI**, add the following  string:</span></span> 

    ```OMA-URI
    ./Device/Vendor/MSFT/Policy/Config/RestrictedGroups/ConfigureGroupMembership
    ```
6. <span data-ttu-id="64572-149">Sous Type de données, **sélectionnez Chaîne XML** et recherchez le fichier XML que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="64572-149">Under Data type, select **String XML** and browse to open the XML file you created in the previous step.</span></span> 

     ![télécharger le fichier de config xml d’administration local](images/sh-local-admin-config.png)

7. <span data-ttu-id="64572-151">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="64572-151">Click **Save**.</span></span>
8. <span data-ttu-id="64572-152">Cliquez **sur Sélectionner les groupes à inclure et** choisissez le groupe de sécurité que vous avez créé [précédemment](#create-security-group-for-surface-hub-2s-devices) **(appareils Surface Hub).**</span><span class="sxs-lookup"><span data-stu-id="64572-152">Click **Select groups to include** and choose the [security group you created earlier](#create-security-group-for-surface-hub-2s-devices) (**Surface Hub devices**).</span></span> <span data-ttu-id="64572-153">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="64572-153">Click **Next.**</span></span>
9. <span data-ttu-id="64572-154">Sous règles d’applicabilité, ajoutez une règle si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="64572-154">Under Applicability rules, add a Rule if desired.</span></span> <span data-ttu-id="64572-155">Dans le cas contraire, **sélectionnez Suivant,** puis **Créer.**</span><span class="sxs-lookup"><span data-stu-id="64572-155">Otherwise, select **Next** and then select **Create**.</span></span>

<span data-ttu-id="64572-156">Pour en savoir plus sur les profils de configuration personnalisés à l’aide de chaînes OMA-URI, voir Utiliser des paramètres personnalisés pour les appareils [Windows 10 dans Intune.](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10)</span><span class="sxs-lookup"><span data-stu-id="64572-156">To learn more about custom configuration profiles using OMA-URI strings, see [Use custom settings for Windows 10 devices in Intune](https://docs.microsoft.com/mem/intune/configuration/custom-settings-windows-10).</span></span>


## <a name="non-global-admins-managing-surface-hub-2s"></a><span data-ttu-id="64572-157">Administrateurs non globaux gérant Surface Hub 2S</span><span class="sxs-lookup"><span data-stu-id="64572-157">Non Global admins managing Surface Hub 2S</span></span>

<span data-ttu-id="64572-158">Les membres du groupe Sécurité des **administrateurs** locaux du Surface Hub peuvent désormais se connecter à l’application Paramètres sur Surface Hub 2S et gérer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="64572-158">Members of the **Surface Hub Local Admins** Security group can now sign in to the Settings app on Surface Hub 2S and manage settings.</span></span>
