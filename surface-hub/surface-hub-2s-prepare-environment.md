---
title: Préparer votre environnement pour SurfaceHub 2S
description: Découvrez ce que vous devez faire pour préparer votre environnement au Surface Hub 2S.
keywords: séparer les valeurs par des virgules
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 2/26/2021
ms.localizationpriority: Medium
ms.openlocfilehash: caa6372820222f6f2f225f028161b3441b147a82
ms.sourcegitcommit: 7e1b351024e33926901ddbdc562ba12aea0b4196
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385142"
---
# <a name="prepare-your-environment-for-surface-hub-2s"></a>Préparer votre environnement pour SurfaceHub 2S

## <a name="office-365-readiness"></a>Préparation d’Office 365

Si vous utilisez Exchange Online, Skype Entreprise Online, Microsoft Teams ou Tableau blanc Microsoft et que vous avez l’intention de gérer Surface Hub 2S avec Intune, examinez d’abord les conditions requises pour [Office 365](https://docs.microsoft.com/office365/enterprise/office-365-endpoints)pour les points de terminaison.

Les points de terminaison Office 365 permettent d’optimiser votre réseau en envoyant toutes les demandes réseau Office 365 de confiance directement via votre pare-feu, en contournant toute inspection ou traitement supplémentaire au niveau des paquets. Cette fonctionnalité réduit la latence et les besoins en capacité de votre périmètre.

Microsoft met régulièrement à jour le service Office 365 avec de nouvelles fonctionnalités, ce qui peut modifier les ports, LES URL et les adresses IP requis. Pour évaluer, configurer et rester à jour avec les modifications, abonnez-vous au service Web d’URL et d’adresse [IP Office 365.](https://docs.microsoft.com/office365/enterprise/office-365-ip-web-service)

> [!NOTE]
> Le Surface Hub fonctionne avec Microsoft Teams, Skype Entreprise Server 2019, Skype Entreprise Server 2015 ou Skype Entreprise Online.
Les plateformes antérieures, telles que Lync Server 2013, ne sont pas pris en charge. Le Surface Hub n’est pas pris en charge GCC-High environnements DoD ou DoD.


## <a name="device-affiliation"></a>Affiliation d’appareil

Utilisez l’affiliation d’appareil pour gérer l’accès des utilisateurs à l’application Paramètres sur Surface Hub 2S.
Avec le système d’exploitation Windows 10 Team (qui s’exécute sur Surface Hub 2S), seuls les utilisateurs autorisés peuvent ajuster les paramètres à l’aide de l’application Paramètres. Étant donné que le choix de l’affiliation peut avoir un impact sur la disponibilité des fonctionnalités, planifiez correctement pour vous assurer que les utilisateurs peuvent accéder aux fonctionnalités comme prévu.

> [!NOTE]
> Vous ne pouvez définir l’affiliation de l’appareil qu’au cours de la configuration initiale de l’expérience OOBE (Out-of-Box Experience). Si vous devez réinitialiser l’affiliation de l’appareil, vous devrez répéter la configuration OOBE.

## <a name="no-affiliation"></a>Aucune affiliation

Aucune affiliation n’est comme si le Surface Hub 2S était dans un groupe de travail avec un compte d’administrateur local différent sur chaque Surface Hub 2S. Si vous choisissez Aucune affiliation, vous devez enregistrer localement la [clé BitLocker](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-key-management-faq)sur une clé USB. Vous pouvez toujours inscrire l’appareil avec Intune ; Toutefois, seul l’administrateur local peut accéder à l’application Paramètres à l’aide des informations d’identification de compte configurées pendant la OOBE. Vous pouvez modifier le mot de passe du compte Administrateur à partir de l’application Paramètres.

## <a name="active-directory-domain-services"></a>Services de domaine Active Directory

Si vous affilier le Surface Hub 2S avec les services de domaine Active Directory locaux, vous devez gérer l’accès à l’application Paramètres à l’aide d’un groupe de sécurité sur votre domaine. Cela permet de s’assurer que tous les membres du groupe de sécurité sont autorisés à modifier les paramètres du Surface Hub 2S. Notez également les remarques suivantes :

- Lorsque le Surface Hub 2S est affilié à vos services de domaine Active Directory locaux, la clé BitLocker peut être enregistrée dans le schéma Active Directory. Pour plus d’informations, voir [Préparer votre organisation pour BitLocker : Planification et stratégies.](https://docs.microsoft.com/windows/security/information-protection/bitlocker/prepare-your-organization-for-bitlocker-planning-and-policies)

- Les CA racines de confiance de votre organisation sont poussées vers le même conteneur dans Surface Hub 2S, ce qui signifie que vous n’avez pas besoin de les importer à l’aide d’un package d’approvisionnement.

- Vous pouvez toujours inscrire l’appareil avec Intune pour gérer de manière centralisée les paramètres sur votre Surface Hub 2S.

## <a name="azure-active-directory"></a>Azure Active Directory

Lorsque vous choisissez d’affiliér votre Surface Hub 2S à Azure Active Directory (Azure AD), tout utilisateur du groupe de sécurité Administrateurs globaux peut se connecter à l’application Paramètres sur Surface Hub 2S. Vous pouvez également configurer des comptes d’administrateur non globaux qui limitent les autorisations à la gestion de l’application Paramètres sur Surface Hub 2S. Cela vous permet d’étenduer les autorisations d’administrateur pour Surface Hub 2S uniquement et d’empêcher tout accès administrateur potentiellement indésirable sur l’ensemble d’un domaine Azure AD. 

Si vous avez activé l’inscription automatique Intune pour votre organisation, surface Hub 2S s’inscrit automatiquement auprès d’Intune. La clé BitLocker de l’appareil est automatiquement enregistrée dans Azure AD. 

Pour en savoir plus sur la gestion du Surface Hub avec Azure AD, voir : 

 - [Administrer la gestion des groupes](admin-group-management-for-surface-hub.md)
 - [Configurer les comptes d’administrateur non global sur surface Hub 2S](surface-hub-2s-nonglobal-admin.md)

