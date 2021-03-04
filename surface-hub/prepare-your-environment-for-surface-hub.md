---
title: Préparer votre environnement pour Microsoft Surface Hub (v1)
description: Cette section contient une vue d’ensemble des étapes nécessaires à la préparation de votre environnement pour que vous puissiez utiliser toutes les fonctionnalités du Microsoft Surface Hub.
ms.assetid: 336A206C-5893-413E-A270-61BFF3DF7DA9
ms.reviewer: ''
manager: laurawi
keywords: préparer l’environnement, fonctionnalités du Surface Hub, créer et tester un compte d’appareil, vérifier la disponibilité du réseau
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 03/03/2021
ms.localizationpriority: medium
appliesto:
- Surface Hub
ms.openlocfilehash: 075724153709fd86ccc00ef98ad532bf45557714
ms.sourcegitcommit: 5c904229a0257297be7f724c264e484d2c4b5168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387446"
---
# <a name="prepare-your-environment-for-microsoft-surface-hub-v1"></a>Préparer votre environnement pour Microsoft Surface Hub (v1)


Cette section contient une vue d’ensemble des dépendances relatives à l’installation et du processus d’installation. Examinez les informations sur les e-s pour vous aider à préparer votre environnement et à collecter les informations nécessaires à la mise en place de votre Surface Hub.


## <a name="review-infrastructure-dependencies"></a>Passer en revue les dépendances relatives à l’infrastructure
Passez en revue ces dépendances pour vous assurer que les fonctionnalités du SurfaceHub fonctionnent dans votre infrastructure informatique.

| Dépendance        | Objectif           |
|-------------|------------------|
| ActiveDirectory ou AzureActiveDirectory (AzureAD) | <p>Le SurfaceHub utilise un compte ActiveDirectory ou AzureAD (appelé **compte d’appareil**) pour accéder aux services Exchange et SkypeEntreprise. Le SurfaceHub doit être en mesure de se connecter au contrôleur de domaine ActiveDirectory ou à votre client AzureAD pour valider les informations d’identification du compte d’appareil, et pour accéder à des informations telles que le nom complet du compte d’appareil, l’alias, le serveur Exchange et l’adresse SIP.</p>Vous pouvez également utiliser la jonction de domaine ou la jonction AzureAD pour permettre à un groupe d’utilisateurs autorisés de configurer les paramètres sur le SurfaceHub. |
| Exchange (Exchange2013 ou version ultérieure, ou ExchangeOnline) et Exchange ActiveSync | <p>Exchange est utilisé pour l’activation des fonctionnalités de messagerie et de calendrier et permet également aux personnes utilisant l’appareil d’envoyer des demandes de réunion au SurfaceHub et de joindre une réunion par un simple toucher.</p>ActiveSync est utilisé pour synchroniser la messagerie et le calendrier du compte d’appareil avec le Surface Hub. Si l’appareil ne peut pas utiliser ActiveSync, les réunions ne s’afficheront pas sur l’écran d’accueil et la participation à des réunions et l’envoi par courrier électronique de tableaux blancs ne seront pas activés. |
| SkypeEntreprise (LyncServer2013 ou version ultérieure, ou SkypeEntrepriseOnline)  | SkypeEntreprise est utilisé pour diverses fonctionnalités de conférence, comme les appels vidéo, la messagerie instantanée et le partage d’écran.|
| Solution de gestion des périphériques mobiles (MDM) (Microsoft Intune, Microsoft Endpoint Configuration Manager ou fournisseur de gestion des périphériques mobiles tiers pris en charge) | Si vous voulez appliquer des paramètres et installer des applications à distance, vous devez configurer une solution GPM et inscrire l’appareil à cette solution. Pour plus d’informations, voir [Gérer les paramètres avec un fournisseur GPM](manage-settings-with-mdm-for-surface-hub.md). |
|Azure Monitor   | Azure Monitor est utilisé pour surveiller l’état d’état des appareils Surface Hub. Voir [Surveiller les Surface Hub avec Azure Monitor pour suivre leur état d’santé.](https://docs.microsoft.com/azure/azure-monitor/insights/surface-hubs) 
| Accès réseau et Internet   | Pour fonctionner correctement, le SurfaceHub doit avoir accès à un réseau filaire ou sans fil. En règle générale il est préférable d'utiliser une connexion filaire. L’authentification 802.1X est prise en charge pour les connexions câblées et sans fil.</br></br></br>**Authentification 802.1X:** dans Windows10, version1703, l'authentification 802.1X pour les connexions câblées et sans fil est activée par défaut dans le Surface Hub. Si votre organisation n’utilise pas l’authentification 802.1X, aucune configuration n’est requise et le Surface Hub continue de fonctionner normalement. Si vous utilisez l’authentification 802.1X, vous devez vous assurer que la certification de l’authentification est installée sur le Surface Hub. Vous pouvez délivrer le certificat au Surface Hub à l’aide du [CSP ClientCertificateInstall](https://msdn.microsoft.com/windows/hardware/commercialize/customize/mdm/clientcertificateinstall-csp) dans GPM, ou vous pouvez [créer un package d’approvisionnement](provisioning-packages-for-surface-hub.md) et l’installer lors de la première utilisation ou par l'intermédiaire de l’application Paramètres. Une fois que le certificat est appliqué au Surface Hub, l'authentification 802.1X commencera à fonctionner automatiquement.</br><br>**Remarque:** Pour plus d’informations sur l’activation de l'authentification 802.1X câblée sur le Surface Hub, voir [Activer l’authentification 802.1x câblée](enable-8021x-wired-authentication.md).</br></br>**IP dynamique:** le SurfaceHub ne peut pas être configuré pour utiliser une adresse IP statique. Il doit utiliser DHCP pour affecter une adresse IP.</br></br>**Serveurs Proxy:** si votre topologie nécessite une connexion à un serveur proxy pour joindre les services Internet, vous pouvez la configurer lors de la première utilisation ou dans les paramètres. Les informations d’identification du proxy sont stockées dans les sessions SurfaceHub et ne doivent être définies qu’une seule fois. |

En outre, notez que SurfaceHub nécessite que les ports suivants soient ouverts:
- HTTPS: 443
- HTTP: 80
- NTP: 123

Si vous utilisez le Surface Hub avec Skype Entreprise, vous devez ouvrir des ports supplémentaires. Suivez les instructions ci-dessous :
- Si vous utilisez Skype Entreprise Online, consultez [LES URL ET plages d’adresses IP Office 365.](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US)
- Si vous utilisez Skype Entreprise Server, consultez Skype Entreprise Server : [ports et protocoles pour les serveurs internes.](https://docs.microsoft.com/SkypeForBusiness/plan-your-deployment/network-requirements/ports-and-protocols) 
- Si vous utilisez un hybride de Skype Entreprise Online et Skype Entreprise Server, vous devez ouvrir tous les ports documentés à partir d’URL et de [plages d’adresses IP Office 365](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2?ui=en-US&rs=en-US&ad=US) et skype entreprise server : ports et [protocoles](https://docs.microsoft.com/SkypeForBusiness/plan-your-deployment/network-requirements/ports-and-protocols?toc=/SkypeForBusiness/toc.json&bc=/SkypeForBusiness/breadcrumb/toc.json)pour les serveurs internes.

Microsoft collecte des données de diagnostic pour améliorer votre expérience du SurfaceHub. Ajoutez ces sites à votre liste verte:
- Point de terminaison client des données de diagnostic: `https://vortex.data.microsoft.com/`
- Point de terminaison des paramètres de données de diagnostic: `https://settings.data.microsoft.com/`

### <a name="proxy-configuration"></a>Configuration du proxy

Si votre organisation limite la connexion à Internet des ordinateurs de votre réseau, un ensemble d’URL doit être disponible pour que les appareils puissent accéder au MicrosoftStore pour Entreprises. Certaines des fonctionnalités du Microsoft Store pour Entreprises utilisent l’application et les services du Microsoft Store. Les appareils utilisant le Store pour Entreprises, que ce soit pour acquérir, installer ou mettre à jour des applications, doivent pouvoir accéder à ces URL. Si vous utilisez un serveur proxy pour bloquer le trafic, votre configuration doit autoriser les URL ci-dessous :

- login.live.com
- login.windows.net
- account.live.com
- clientconfig.passport.net
- windowsphone.com
- *.wns.windows.com
- *.microsoft.com
- www.msftncsi.com (antérieur à Windows10 version1607)
- www.msftconnecttest.com/connecttest.txt (remplace www.msftncsi.com à partir de Windows10 version1607)


## <a name="work-with-other-admins"></a>Collaborer avec d’autres administrateurs

SurfaceHub interagit avec différents produits et services. Selon la taille de votre entreprise, plusieurs personnes prennent en charge différents produits dans votre environnement. Vous voudrez probablement inclure à votre planning des personnes qui gèrent Exchange, ActiveDirectory (ou AzureActiveDirectory), la GPM et les ressources réseau, et vous préparer aux déploiements SurfaceHub. 


## <a name="create-and-verify-device-account"></a>Créer et vérifier un compte d’appareil

Un compte d’appareil est un compte de ressource Exchange que SurfaceHub utilise pour afficher son calendrier des réunions, participer à des appels SkypeEntreprise, envoyer des courriers électroniques et (éventuellement) s’authentifier auprès d’Exchange. Pour plus d’informations, voir [Créer et tester un compte d’appareil](create-and-test-a-device-account-surface-hub.md).

Une fois que vous avez créé votre compte d’appareil, pour vérifier qu’il est correctement configuré, exécutez les scripts PowerShell de validation du compte de l’appareil Surface Hub. Pour plus d’informations, voir [Scripts PowerShell pour le Surface Hub](appendix-a-powershell-scripts-for-surface-hub.md) plus loin dans ce guide. 

 

## <a name="prepare-for-first-run-program"></a>Se préparer au programme de première utilisation 
Plusieurs éléments sont à prendre en compte avant de commencer le [programme de première utilisation](first-run-program-surface-hub.md).  

### <a name="create-provisioning-packages-optional"></a>Créer des packages de mise en service (facultatif)
Vous pouvez utiliser des packages de mise en service pour ajouter des certificats, personnaliser les paramètres et installer des applications. Pour plus d’informations, voir [Créer des packages de mise en service](provisioning-packages-for-certificates-surface-hub.md). Vous pouvez [installer des packages e mise en service lors de la première utilisation](first-run-program-surface-hub.md#first-page).

### <a name="set-up-admin-groups"></a>Définir des groupes d’administration
Chaque SurfaceHub peut être configuré localement à l’aide de l’application Paramètres sur celui-ci. Pour empêcher les utilisateurs non autorisés de modifier les paramètres, l’application Paramètres nécessite des informations d’identification d’administration pour ouvrir l’application. Pour plus d’informations sur la configuration et la gestion des groupes d’administration, voir [Administrer la gestion des groupes](admin-group-management-for-surface-hub.md). Vous allez [configurer des administrateurs pour l’appareil lors de la première utilisation](first-run-program-surface-hub.md#setup-admins).

### <a name="review-and-complete-surface-hub-setup-worksheet-optional"></a>Passer en revue et remplir la fiche d’installation SurfaceHub (facultatif)
Lorsque vous accédez au programme de première utilisation pour votre SurfaceHub, vous devez fournit certaines informations. La fiche d’installation récapitule ces informations et fournit des listes d’informations spécifiques à l’environnement dont vous avez besoin pour accéder au programme de première utilisation. Pour plus d’informations, voir [Fiche d’installation](setup-worksheet-surface-hub.md).


## <a name="in-this-section"></a>Dans cette section

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sujet</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="create-and-test-a-device-account-surface-hub.md" data-raw-source="[Create and test a device account](create-and-test-a-device-account-surface-hub.md)">Créer et tester un compte d’appareil</a></p></td>
<td align="left"><p>Cette rubrique indique comment créer et tester le compte d’appareil utilisé par le Surface Hub pour communiquer avec Skype.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="provisioning-packages-for-certificates-surface-hub.md" data-raw-source="[Create provisioning packages](provisioning-packages-for-certificates-surface-hub.md)">Créer des packages de mise en service</a></p></td>
<td align="left"><p>Pour Windows10, les paramètres qui utilisent le Registre ou une plateforme de services de contenu (CSP) peuvent être configurés à l’aide de packages de mise en service. Vous pouvez également ajouter des certificats lors de la première utilisation à l’aide de la mise en service.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="admin-group-management-for-surface-hub.md" data-raw-source="[Admin group management](admin-group-management-for-surface-hub.md)">Administrer la gestion des groupes</a></p></td>
<td align="left"><p>Chaque Surface Hub peut être configuré individuellement en ouvrant l’application Paramètres sur celui-ci. Toutefois, pour empêcher la modification des paramètres par des personnes autres que des administrateurs, l’application Paramètres requiert la saisie d’informations d’identification d’administrateur pour ouvrir l’application et modifier les paramètres.</p>
<p>L’ouverture de l’application Paramètres requiert la saisie d’informations d’identification d’administrateur local.</p></td>
</tr>
</tbody>
</table>

## <a name="more-information"></a>Informations supplémentaires

- [Billet de blog: Surface Hub et liste des domaines approuvés Skype Entreprise](https://blogs.technet.microsoft.com/y0av/2017/10/25/95/)
- [Billet de blog: Surface Hub dans un environnement à domaines multiples](https://blogs.technet.microsoft.com/y0av/2017/11/08/11/)
- [Billet de blog: configuration d’un proxy pour votre Surface Hub](https://blogs.technet.microsoft.com/y0av/2017/12/03/7/)

 

 





