---
title: Aperçu de la sécurité de Surface Duo
description: Cet article explique comment Surface Duo offre une sécurité de qualité entreprise sur un appareil mobile via le système d’exploitation Android et l’UEFI conçu par Microsoft.
ms.technology: windows
ms.prod: surface
ms.mktglfcycl: manage
ms.sitesec: library
author: coveminer
ms.author: greglin
ms.topic: article
ms.date: 8/12/2020
ms.reviewer: karand
manager: laurawi
ms.audience: itpro
audience: ITPro
ms.localizationpriority: medium
appliesto:
- Surface Duo
ms.openlocfilehash: 91eb893dbdc6dae93cf402a602b64a83309388e8
ms.sourcegitcommit: 37e0994e2b8ae62b0352b016b698edcc7ca500fb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
test: test
ms.locfileid: "11326156"
---
# Aperçu de la sécurité de Surface Duo

Surface Duo dispose d’une protection intégrée à chaque couche avec du matériel, des microprogrammes et des logiciels entièrement intégrés pour garantir la sécurité de vos appareils, identités et données. En tant qu’appareil Android 10, Surface Duo utilise les fonctionnalités de sécurité Android au niveau du système d’exploitation et au niveau de la couche des services Google. Le système d’exploitation Android tire parti des contrôles de sécurité du système d’exploitation traditionnels pour protéger les données utilisateur et les ressources système, protège l’intégrité de l’appareil contre les programmes malveillants et assure l’isolation des applications. En outre, Google fournit un certain nombre de services superposés sur le système d’exploitation qui, lorsqu’ils sont combinés avec la sécurité du système d’exploitation Android, contribuent à protéger en permanence l’utilisateur Android.

- **UEFI personnalisé.** L’interface UEFI (Unified Extensible Firmware Interface) personnalisée de Microsoft, qui permet un contrôle total sur les composants du microprogramme, est propre à Surface Duo, parmi les appareils Android. Microsoft offre une sécurité de qualité entreprise à Surface Duo en écrivant ou en réactivant chaque ligne de code du microprogramme en interne, ce qui permet à Microsoft de répondre directement et agilement aux menaces potentielles de microprogramme et d’atténuer les risques de sécurité de la chaîne d’approvisionnement.
- **Démarrage vérifié.** À partir du niveau matériel lors de la connectez-vous, le démarrage vérifié s’efforce de s’assurer que le code exécuté provient uniquement d’une source fiable. Il établit une chaîne complète d’confiance, de la racine de confiance protégée par le matériel au chargeur de démarrage, à la partition de démarrage et à d’autres partitions vérifiées. Lorsque Surface Duo démarre, chaque étape vérifie l’intégrité et l’authenticité de l’étape suivante avant de remettre l’exécution.
- **Séparation de l’application.** Le sandboxing d’application isole et protège les applications Android, empêchant ainsi les applications malveillantes d’accéder aux informations privées. Le chiffrement obligatoire, toujours en cours et la gestion des clés contribuent à protéger les données en transit et au repos, même si les appareils tombent entre de mauvaises mains. Le chiffrement est protégé par des clés de magasin de clés, qui stockent les clés de chiffrement dans un conteneur, ce qui rend plus difficile l’extraction à partir d’un appareil.
- **Google Play Protect.** Sur la couche logicielle, Surface Duo utilise la détection des menaces Google Play Protect, qui analyse toutes les applications, y compris les applications publiques de Google Play, les applications système mises à jour par Microsoft et les opérateurs, ainsi que les applications téléchargées de nouveau.
- **Microsoft Defender ATP.** Le logiciel de protection antivirus et anti-programme malveillant de niveau entreprise pour Windows 10 est désormais disponible pour les appareils Android gérés à partir d’Intune. Pour en savoir plus, [consultez Microsoft defender ATP pour Android.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-android) 


## Sécurité de la gestion des appareils mobiles

Surface Duo est sécurisé dans un environnement d’entreprise à l’aide d’une solution Enterprise Mobility Management (EMM) qui fournit un ensemble cohérent d’outils de protection, de technologies et de meilleures pratiques que vous pouvez adapter pour répondre à vos exigences d’organisation et de conformité. Un large éventail d’API de gestion offre aux services informatiques les outils permettant d’éviter les fuites de données et d’appliquer la conformité dans divers scénarios. La prise en charge multi-profil et les options de gestion des appareils permettent la séparation des données personnelles et de travail, ce qui permet de sécuriser les données d’entreprise.

La sécurité MDM repose sur un ensemble étendu de technologies de configuration pour permettre aux utilisateurs d’être productifs en cours tout en protégeant la propriété intellectuelle d’entreprise critique. Cela inclut les stratégies de protection des applications, les stratégies de restriction des appareils et les technologies associées conçues pour vous permettre d’atteindre des objectifs spécifiques en fonction de votre environnement , que votre entreprise consiste à livrer des commandes de prise de restaurant, à gérer les services informatiques pour les bureaux de secours ou à gérer les informations de sécurité nationale sensibles. 

Par exemple, vous souhaitez peut-être renforcer l’authentification des appareils en demandant aux utilisateurs d’entrer un code confidentiel alphanumérique à 6 chiffres avec l’authentification à 2 facteurs.  Vous pouvez limiter les appareils que les utilisateurs peuvent inscrire pour vous assurer que vous respectez les limites de licence ou éviter d’accorder l’accès à des téléphones « jailbreakés » ou à d’autres types d’appareils non pris en compte.
Intune et d’autres emms offrent aux organisations la flexibilité nécessaire pour gérer les appareils en fonction de leurs besoins.

## Stratégies de protection des applications

Les stratégies de protection des applications (APP) sont des règles qui garantissent que les données d’une organisation restent sûres ou contenues dans une application gérée. Une stratégie peut être une règle appliquée lorsque l’utilisateur tente d’accéder ou de déplacer des données « d’entreprise », ou un ensemble d’actions qui sont interdites ou surveillées lorsque l’utilisateur se trouve à l’intérieur de l’application. Une application gérée est une application qui dispose de stratégies de protection d’application qui lui sont appliquées et qui peut être gérée par Intune.

Les stratégies de protection des applications vous permettent de gérer et de protéger les données de votre organisation au sein d’une application. De nombreuses applications de productivité, telles que les applications Microsoft Office, peuvent être gérées par Intune MAM. Consultez la liste officielle des applications protégées par [Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-supported-intune-apps) disponibles pour une utilisation publique.

## Considérations en matière de sécurité pour la gestion de Surface Duo

Le nombre croissant de paramètres de stratégie disponibles dans les solutions de gestion des appareils mobiles permet aux organisations d’ajuster les niveaux de protection pour répondre à leurs besoins spécifiques. Pour aider les organisations à hiérarchiser les paramètres de sécurité pour Surface Duo (ou tout autre appareil Android), Intune a introduit son infrastructure de configuration de sécurité [Android Enterprise](https://docs.microsoft.com/mem/intune/enrollment/android-configuration-framework) organisée dans plusieurs scénarios de configuration distincts, fournissant des conseils pour le profil de travail et les scénarios entièrement gérés.
 

| Niveau Sécurité                                                                                                       | Ciblé sur                                                                                                                                                                      | Résumé                                                                                                                                                                                     | Informations sur les paramètres                                                                                                                                                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sécurité de base du profil professionnel - Niveau 1                                                                                | Appareils personnels ayant accès aux données scolaires ou de travail.                                                                                                                             | Présente les exigences de mot de passe, sépare les données personnelles et de travail, et valide l’attestation d’appareil Android.                                                                               | [Paramètres de niveau de profil professionnel 1](https://microsoft.sharepoint.com/teams/EpsilonAdminGuide/Shared%20Documents/General/•%09https:/docs.microsoft.com/mem/intune/enrollment/android-work-profile-security-settings#work-profile-basic-security) |
| Profil professionnel haute sécurité - Niveau 3<br>(En raison des conventions d’infrastructure, il s’agit du niveau suivant au-dessus du niveau 1.)<br> ** | Appareils utilisés par des utilisateurs ou des groupes à risque élevé. Par exemple, les utilisateurs qui gèrent des données hautement sensibles lorsque la divulgation non autorisée entraîne une perte matérielle considérable. | Introduit la protection contre les menaces mobiles ou Microsoft Defender ATP, définit la version minimale d’Android sur 8.0, met en place des stratégies de mot de passe plus puissantes et limite davantage la séparation personnelle et le travail. | [Paramètres de niveau de profil professionnel 3](https://docs.microsoft.com/mem/intune/enrollment/android-work-profile-security-settings#work-profile-high-security)                                                                                         |
| Sécurité de base entièrement gérée -Niveau 1                                                                                | Configuration de sécurité minimale pour un appareil d’entreprise, applicable à la plupart des utilisateurs mobiles accédant aux données scolaires ou professionnels.                                                          | Présente les exigences de mot de passe, définit la version minimale d’Android sur 8.0 et applique certaines restrictions d’appareil.                                                                          | [Paramètres de niveau 1 entièrement gérés](https://docs.microsoft.com/mem/intune/enrollment/android-fully-managed-security-settings#fully-managed-basic-security)                                                                                     |
| Niveau de sécurité améliorée entièrement géré 2                                                                              | Appareils où les utilisateurs accèdent à des informations sensibles ou confidentielles.                                                                                                                | Édicte des stratégies de mot de passe plus puissantes et désactive les fonctionnalités utilisateur/compte.                                                                                                                   | [Ensembles de niveau 2 entièrement gérés](https://docs.microsoft.com/mem/intune/enrollment/android-fully-managed-security-settings#fully-managed-enhanced-security)                                                                                   |
| Niveau de sécurité élevé entièrement géré 3                                                                                  | Appareils utilisés par des utilisateurs ou des groupes à risque élevé. Par exemple, les utilisateurs qui gèrent des données hautement sensibles lorsque la divulgation non autorisée entraîne une perte matérielle considérable. | Augmente la version minimale d’Android à 10.0, introduit la protection contre les menaces mobiles ou Microsoft Defender ATP et applique des restrictions supplémentaires sur les appareils.                                     | [Paramètres de niveau 3 entièrement gérés](https://docs.microsoft.com/mem/intune/enrollment/android-fully-managed-security-settings#fully-managed-high-security)                                                                                      |
 
Comme pour n’importe quelle infrastructure, les paramètres au sein d’un niveau correspondant peuvent avoir besoin d’être ajustés en fonction des besoins de l’organisation, car la sécurité doit évaluer l’environnement des menaces, l’augmentation des risques et l’impact sur l’utilisation.
 
 
**Si vous souhaitez en savoir plus**


- [Infrastructure de configuration de la sécurité Android Enterprise](https://docs.microsoft.com/mem/intune/enrollment/android-configuration-framework)
- [Vue d’ensemble des stratégies de protection des applications](https://docs.microsoft.com/mem/intune/apps/app-protection-policy)
- [Paramètres de stratégie de protection des applications Android dans Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/app-protection-policy-settings-android)
- [Définir des restrictions d’inscription](https://docs.microsoft.com/mem/intune/enrollment/enrollment-restrictions-set)
- [Livre blanc sur Android Enterprise Security](https://static.googleusercontent.com/media/www.android.com/en//static/2016/pdfs/enterprise/Android_Enterprise_Security_White_Paper_2019.pdf)
 
