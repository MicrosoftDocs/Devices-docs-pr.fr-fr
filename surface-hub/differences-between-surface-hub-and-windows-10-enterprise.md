---
title: Notions fondamentales sur le système d’exploitation (SurfaceHub)
description: Cette rubrique explique les aspects uniques du système d’exploitation Windows 10 Team et sa différence par rapport à Windows 10 Entreprise.
keywords: historique des modifications
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 03/03/2021
ms.reviewer: ''
manager: laurawi
ms.localizationpriority: medium
ms.openlocfilehash: f3ffcc46912fba3313e4489f5713b6ffcacf2d8a
ms.sourcegitcommit: 5c904229a0257297be7f724c264e484d2c4b5168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387477"
---
# <a name="operating-system-essentials-surface-hub"></a>Notions fondamentales sur le système d’exploitation (SurfaceHub)

Le système d’exploitation du Surface Hub, Windows10 Collaboration, est basé sur Windows10 Entreprise, ce qui garantit une excellente prise en charge de la gestion de l’entreprise, de la sécurité et d’autres fonctionnalités. Toutefois, il existe des différences importantes entre les deux. Si l’édition Entreprise est destinée aux PC, Windows10 Collaboration est entièrement conçu pour une utilisation sur grand écran et dans les salles de réunion. Lorsque vous évaluez les exigences en matière de sécurité et de gestion du Surface Hub, il est préférable de le considérer comme un nouveau système d’exploitation. Cet article est conçu pour vous aider à mettre en évidence les différences clés entre Windows10 Collaboration sur le Surface Hub et Windows10 Entreprise, ainsi que leurs conséquences pour votre organisation.

À compter de septembre 2020, les clients ont la possibilité de migrer vers Windows 10 Professionnel ou Entreprise sur Surface Hub 2S. Pour en savoir plus, consultez les rubriques suivantes :

- [Annonce de la disponibilité de Windows 10 Professionnel et Entreprise sur Surface Hub 2](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/announcing-the-availability-of-windows-10-pro-and-enterprise-on/ba-p/1624107).

- [Migrer vers Windows10 Professionnel ou Entreprise sur Surface Hub2](surface-hub-2s-migrate-os.md)

## <a name="user-interface"></a>Interface utilisateur

### <a name="shell-os-user-interface"></a>Interpréteur de commandes (interface utilisateur du système d’exploitation)

L’interpréteur de commandes du Surface Hub est entièrement conçu pour une utilisation sur grand écran et bénéficie d’une fonctionnalité tactile optimisée. Il n’utilise pas le même interpréteur de commandes que Windows10 Entreprise.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les paramètres relatifs aux contrôles dans l’interpréteur de commandes de Windows10 Entreprise ne s’appliquent pas au Surface Hub.

### <a name="lock-screen-and-screensaver"></a>Écran de verrouillage et écran de veille

Surface Hub ne dispose pas d’un écran de verrouillage ni d’un écran de veille, mais il possède une fonctionnalité similaire appelée «écran d’accueil». L’écran d’accueil affiche les réunions planifiées à partir du calendrier du compte de l’appareil et fournit des points d’accès faciles vers les principales applications du Surface Hub: Skype Entreprise, Tableau blanc et Se connecter.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les paramètres de l’écran de verrouillage, du délai d’expiration de l’écran et de l’écran de veille ne s’appliquent pas au Surface Hub.

### <a name="user-sign-in"></a>Connexion de l’utilisateur

Le Surface Hub est conçu pour être utilisé dans des espaces communs, tels que des salles de réunion. À la différence des PC Windows, n’importe qui peut utiliser un Surface Hub sans nécessiter d'infos d'identification de la part de l'utilisateur. Pour activer cette fonctionnalité communautaire, Surface Hub ne prend pas en charge la connexion Windows de la même façon que Windows10 Entreprise (par ex. connexion de l'utilisateur au système d'exploitation et utilisation de ces informations d'identification dans tout le SE). Au lieu de cela, l'utilisateur est toujours connecté en local, automatiquement et avec peu de privilèges au Surface Hub. Surface Hub ne prend pas en charge la connexion d’autres utilisateurs, y compris les administrateurs (par exemple, lorsqu’un administrateur se connecte, il n'est pas connecté au système d’exploitation).

Les utilisateurs peuvent se connecter à un Surface Hub, mais pas au système d’exploitation. Par exemple, lorsqu’un utilisateur se connecte aux Applications ou à Mes réunions et mes fichiers, il est connecté uniquement à ces applications ou services, mais pas au système d’exploitation. Par conséquent, l’utilisateur connecté est en mesure de récupérer ses fichiers sur le cloud et les réunions personnelles stockées dans le cloud, et ces informations d’identification sont supprimées lorsque l'option **Terminer la session** est activée.


*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> En règle générale, le Surface Hub utilise les fonctionnalités de verrouillage plutôt que le contrôle de l’accès des utilisateurs pour garantir la sécurité. Les stratégies liées aux exigences de mot de passe, à l’ouverture de session interactive, aux comptes d’utilisateur et au contrôle de l’accès ne s’appliquent pas au Surface Hub.

### <a name="saving-and-browsing-files"></a>Enregistrement et consultation de fichiers

Les utilisateurs ont accès à un ensemble limité de répertoires sur le Surface Hub:
- Musique
- Vidéos
- Documents
- Images
- Téléchargements

Les fichiers enregistrés localement dans ces répertoires sont supprimés lorsque l’utilisateur appuie sur **Terminer la session**. Pour enregistrer le contenu créé au cours d’une réunion, les utilisateurs doivent enregistrer les fichiers sur une clé USB ou sur OneDrive.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les stratégies relatives aux autorisations d’accès et à la propriété des fichiers et des dossiers ne s’appliquent pas au Surface Hub. Les utilisateurs ne peuvent pas parcourir et enregistrer des fichiers dans les répertoires du système et dans les dossiers du réseau.

## <a name="applications"></a>Applications

### <a name="default-applications"></a>Applications par défaut

Sauf quelques rares exceptions, les applications de plateforme Windows universelle (UWP) disponibles par défaut sur Surface Hub sont les mêmes que celles présentes sur les PC Windows10.

Applications UWP pré-installées sur Surface Hub:
- Alarmes et horloge
- Calculatrice
- Se connecter
- ExcelMobile
- Hub de commentaires
- Explorateur de fichiers*
- Prise en main
- Cartes
- MicrosoftEdge
- MicrosoftPowerBI
- OneDrive
- Photos
- PowerPointMobile
- Paramètres*
- Skype Entreprise*
- Store
- Tableau blanc*
- WordMobile

*Les applications comportant un astérisque (&ast;) sont propres au Surface Hub.*

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Reportez-vous aux recommandations de Windows10 Entreprise pour déterminer les fonctionnalités et les exigences de réseau des applications disponibles par défaut sur le Surface Hub.

### <a name="installing-apps-drivers-and-services"></a>Installation des applications, des pilotes et des services

Pour vous aider à préserver la nature fonctionnelle de l’appareil, le Surface Hub prend en charge uniquement l’installation d’applications de plateforme Windows universelle (UWP) et non l’installation d’applications, de services et de pilotes Win32 classiques. En outre, seuls les administrateurs disposent des accès nécessaires à l’installation des applications UWP.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les employés peuvent uniquement utiliser les applications qui ont été installées par les administrateurs, ce qui contribue à limiter les utilisations indésirables. Le Surface Hub ne prend pas en charge l’installation des agents Win32 requis par la plupart des outils d’analyse et de gestion des PC traditionnels.

## <a name="security-and-lockdown"></a>Sécurité et verrouillage

Le Surface Hub étant utilisé dans des espaces communs, tels que des salles de réunion, son système d’exploitation personnalisé comprend de nombreuses fonctionnalités de sécurité et de verrouillage disponibles dans Windows10.

Le Surface Hub implémente les fonctionnalités de sécurité de Windows10 suivantes:
- [Démarrage sécurisé UEFI](https://msdn.microsoft.com/windows/hardware/commercialize/manufacture/desktop/secure-boot-overview)
- [Intégrité du code en mode utilisateur (UMCI, User Mode Code Integrity) avec Device Guard](https://technet.microsoft.com/itpro/windows/keep-secure/introduction-to-device-guard-virtualization-based-security-and-code-integrity-policies)
- [Stratégies de restriction d’applications via AppLocker](https://technet.microsoft.com/itpro/windows/keep-secure/applocker-overview)
- [Chiffrement de lecteur BitLocker](https://technet.microsoft.com/itpro/windows/keep-secure/bitlocker-overview)
- [Module de plateforme sécurisée](https://technet.microsoft.com/itpro/windows/keep-secure/trusted-platform-module-overview)
- [WindowsDefender](https://technet.microsoft.com/itpro/windows/keep-secure/windows-defender-in-windows-10)
- [Contrôle de compte d’utilisateur (UAC)](https://technet.microsoft.com/itpro/windows/keep-secure/user-account-control-overview) pour l’accès à l’application Paramètres

Les fonctionnalités Surface Hub suivantes fournissent une sécurité supplémentaire:
- Microprogramme UEFI personnalisé
- Interpréteur de commandes personnalisé et menu Démarrer limitant l’appareil aux fonctions de réunion
- Explorateur de fichiers personnalisé n’autorisant l’accès qu’aux fichiers et dossiers situés dans le dossier Mes Documents
- Application Paramètres personnalisée permettant uniquement aux administrateurs de modifier les paramètres de l’appareil
- Téléchargement de pilotes Plug-and-Play avancés désactivé

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Prenez en compte ces fonctionnalités lors de l’évaluation du Surface Hub en matière de sécurité.

## <a name="management"></a>Gestion

### <a name="device-settings"></a>Paramètres de l’appareil

Les paramètres de l’appareil peuvent être configurés par le biais de l’application Paramètres. L’application Paramètres du Surface Hub est personnalisée, mais elle reprend également de nombreux paramètres que vous connaissez de Windows10Desktop. Une invite de contrôle de compte d’utilisateur (UAC) s’affiche à l’ouverture de l’application Paramètres pour vérifier les informations d’identification de l’administrateur, sans pour autant le connecter.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les employés peuvent utiliser le Surface Hub dans le cadre de réunions, mais ils ne peuvent modifier aucun paramètre de l’appareil. En plus des fonctionnalités de verrouillage, cela permet de s’assurer qu’ils utilisent uniquement l’appareil dans le cadre des fonctions de réunion.

### <a name="administrative-features"></a>Fonctionnalités d’administration

Les fonctionnalités d’administration de Windows10 Entreprise, telles que Microsoft Management Console, Run, Command Prompt, PowerShell, l’Éditeur du Registre, l’Observateur d’événements et le Gestionnaire des tâches ne sont pas pris en charge sur le Surface Hub. L’application Paramètres contient toutes les fonctionnalités d’administration localement disponibles sur Surface Hub.

### <a name="remote-management-and-monitoring"></a>Analyse et gestion à distance

Le Surface Hub prend en charge la gestion à distance via des solutions de gestion des périphériques mobiles (MDM) telles que [Microsoft Intune](https://docs.microsoft.com/intune/) et la surveillance via [Azure Monitor.](https://azure.microsoft.com/services/monitor/) 

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Le Surface Hub ne prend pas en charge l’installation des agents Win32 requis par la plupart des outils d’analyse et de gestion des PC traditionnels, tels que System Center Operations Manager.

### <a name="group-policy"></a>Stratégie de groupe

Le Surface Hub ne prend pas en charge la stratégie de groupe Windows, y compris l’audit. Au lieu de cela, utilisez GPM pour appliquer des stratégies à votre Surface Hub. Pour plus d’informations sur la GPM, voir [Gérer les paramètres avec un fournisseur GPM](manage-settings-with-mdm-for-surface-hub.md).

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Utilisez GPM pour gérer le Surface Hub au lieu de la stratégie de groupe.

### <a name="remote-assistance"></a>Assistance à distance

Le Surface Hub ne prend pas en charge l’assistance à distance.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les stratégies relatives à l’assistance à distance ne s’appliquent pas au Surface Hub.

## <a name="network"></a>Réseau

### <a name="domain-join-and-azure-active-directory-azure-ad-join"></a>Jonction de domaine et jonction à Azure ActiveDirectory (AzureAD) 

Le Surface Hub utilise la jonction de domaine et la jonction à Azure AD principalement pour fournir un groupe d’administration reposant sur le répertoire. Les utilisateurs ne peuvent pas se connecter avec un compte de domaine. Pour obtenir plus d’informations, voir [Administrer la gestion des groupes](admin-group-management-for-surface-hub.md).

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les stratégies de groupe ne sont pas appliquées lorsqu’un Surface Hub est lié à votre domaine. Les stratégies relatives à l’appartenance à un domaine ne s’appliquent pas au Surface Hub.

### <a name="accessing-domain-resources"></a>Accès aux ressources de domaine

Les utilisateurs peuvent se connecter à MicrosoftEdge pour accéder à des sites intranet et à des ressources en ligne (par exemple, Office 365). Si votre Surface Hub est configuré avec un compte d’appareil, le système l’utilise pour accéder à Exchange et à Skype Entreprise. Toutefois, le Surface Hub ne prend pas en charge l’accès aux ressources de domaine telles que les partages de fichiers et les imprimantes.

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Les stratégies relatives à l’accès aux objets de domaine ne s’appliquent pas au Surface Hub.

<!--
### Endpoints



*Organization policies that this may affect:* <br> 
-->

### <a name="diagnostic-data"></a>Données de diagnostic

Le système d’exploitation du Surface Hub utilise le composant Expériences des utilisateurs connectés et télémétrie de Windows10 pour collecter et transmettre des données de diagnostic. Pour plus d’informations, voir [Configurer les données de diagnostic Windows dans votre organisation](https://technet.microsoft.com/itpro/windows/manage/configure-windows-diagnostic-data-in-your-organization).

*Stratégies d’entreprise que cela est susceptible d’affecter:* <br> Configurez les données de diagnostic du Surface Hub de la même manière que pour Windows10 Entreprise.
