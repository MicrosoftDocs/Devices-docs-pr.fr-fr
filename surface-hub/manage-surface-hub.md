---
title: Gérer Microsoft Surface Hub
description: Comment gérer votre Surface Hub une fois le programme de première utilisation terminé.
ms.assetid: FDB6182C-1211-4A92-A930-6C106BCD5DC1
ms.reviewer: ''
manager: laurawi
keywords: gérer le Surface Hub
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 01/17/2018
ms.localizationpriority: medium
ms.openlocfilehash: 5e7fca007549d8804a756ef2a042f092f0acb1c3
ms.sourcegitcommit: 5c904229a0257297be7f724c264e484d2c4b5168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387435"
---
# <a name="manage-microsoft-surface-hub"></a>Gérer le Microsoft SurfaceHub

Après la configuration initiale du Microsoft Surface Hub, les paramètres et la configuration de l’appareil peuvent être modifiés de deux manières :

- **Gestion locale**: chaque SurfaceHub peut être configuré localement à l’aide de l’application **Paramètres** de celui-ci. Pour empêcher les utilisateurs non autorisés de modifier les paramètres, l’application Paramètres nécessite des informations d’identification d’administrateur pour ouvrir l’application. Pour plus d’informations, voir [Gestion locale des paramètres SurfaceHub](local-management-surface-hub-settings.md).
- **** Gestion à distance : le Surface Hub permet aux administrateurs informatiques de gérer les paramètres et les stratégies à l’aide d’un fournisseur de gestion des périphériques mobiles (MDM), tel que Microsoft Intune, Microsoft Endpoint Configuration Manager et d’autres fournisseurs tiers. En outre, les administrateurs peuvent surveiller les Surface Hub à l’aide d’Azure Monitor.  Pour plus d’informations, voir Gérer les [paramètres](manage-settings-with-mdm-for-surface-hub.md)avec un fournisseur de gestion des données de gestion des données et surveiller les [Surface Hub avec Azure Monitor pour suivre leur état d’santé.](https://docs.microsoft.com/azure/azure-monitor/insights/surface-hubs) 

> [!NOTE]
> Ces méthodes de gestion ne s’excluent pas mutuellement. Les appareils peuvent être gérés à la fois localement et à distance si vous le souhaitez. Toutefois, les stratégies et paramètres de gestion des stratégies de gestion des données (MDM) vont modifier les modifications locales lors de la synchronisation du Surface Hub avec le serveur de gestion. 

## <a name="in-this-section"></a>Dans cette section

En savoir plus sur la gestion et la mise à jour du SurfaceHub.

| Rubrique | Description |
| ----- | ----------- |
| [Gestion à distance du SurfaceHub](remote-surface-hub-management.md) |Rubriques relatives à la gestion à distance du Surface Hub. Incluent l’installation des applications, la gestion des paramètres avec GPM et la surveillance avec Operations Management Suite. |
| [Gérer les paramètres SurfaceHub](manage-surface-hub-settings.md) |Rubriques associées à la gestion des paramètres SurfaceHub: accessibilité, compte d’appareil, réinitialiser l’appareil, nom de domaine complet, paramètres de WindowsUpdate et réseau sans fil. |
| [Installer des applications sur le SurfaceHub]( https://technet.microsoft.com/itpro/surface-hub/install-apps-on-surface-hub) | Les administrateurs peuvent installer des applications, au choix depuis le Microsoft Store ou le Microsoft Store pour Entreprises.|
[Configurer le menu Démarrer de Surface Hub](surface-hub-start-menu.md) | Utilisez la GPM pour personnaliser le menu Démarrer de Surface Hub.
| [Configurer et utiliser le Tableau blanc collaboratif Microsoft](whiteboard-collaboration.md)  | La dernière mise à jour du tableau blanc Microsoft inclut la possibilité pour deux Surface Hub de collaborer en temps réel sur le même tableau.   |
| [Mettre fin à une réunion avec Terminer la session](https://technet.microsoft.com/itpro/surface-hub/finishing-your-surface-hub-meeting) | À l’issue d’une réunion, les utilisateurs peuvent appuyer sur **Terminer la session** pour nettoyer les données sensibles et préparer l’appareil pour la prochaine réunion.|
| [Se connecter à Surface Hub avec MicrosoftAuthenticator](surface-hub-authenticator-app.md) | Vous pouvez vous connecter à un Surface Hub sans mot de passe à l’aide de l’application MicrosoftAuthenticator, disponible sur iOS et Android.   |
| [Enregistrer la clé BitLocker](https://technet.microsoft.com/itpro/surface-hub/save-bitlocker-key-surface-hub) | Chaque Surface Hub est automatiquement configuré à l’aide du logiciel de chiffrement de lecteur BitLocker. Microsoft vous recommande vivement de sauvegarder vos clés de récupération BitLocker.|
| [Connecter d’autres appareils et les afficher avec le SurfaceHub](https://technet.microsoft.com/itpro/surface-hub/connect-and-display-with-surface-hub) | Vous pouvez connecter un autre appareil à votre SurfaceHub pour en afficher le contenu.|
| [Miracast sur le réseau local ou le réseau sans fil existant](miracast-over-infrastructure.md) | Vous pouvez utiliser Miracast sur votre réseau sans fil ou votre réseau local pour vous connecter à Surface Hub. |
 [Activer l’authentification 802.1x câblée](enable-8021x-wired-authentication.md) | Les stratégies GPM de l’authentification 802.1x câblée ont été activées sur les appareils Surface Hub. 
| [Utilisation d’un système de contrôle d’espace](https://technet.microsoft.com/itpro/surface-hub/use-room-control-system-with-surface-hub) | Les systèmes de contrôle d’espace peuvent être utilisés avec votre Microsoft SurfaceHub.|
[Utilisation de l’outil de récupération de SurfaceHub](surface-hub-recovery-tool.md) | Utilisez l’outil de récupération Surface Hub pour ré-imager le SSD Surface Hub.
[Remplacement du SSD de SurfaceHub](surface-hub-ssd-replacement.md) | Découvrez comment supprimer et remplacer le lecteur SSD dans votre Surface Hub.

## <a name="related-topics"></a>Rubriques associées

- [Afficher le mode de présentation de PowerBI sur SurfaceHub et Windows10](https://powerbi.microsoft.com/documentation/powerbi-mobile-win10-app-presentation-mode/)
