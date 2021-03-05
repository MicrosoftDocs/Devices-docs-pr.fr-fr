---
title: Configurer Windows 10 Professionnel ou Entreprise sur Surface Hub 2
description: Cet article inclut des recommandations pour garantir la meilleure expérience lors de l’utilisation d’un écran tactile et d’un stylet personnalisés.
keywords: Surface Hub, Windows 10, bureau, installer, configuration
ms.prod: surface-hub
ms.mktglfcycl: deploy
ms.localizationpriority: low
ms.sitesec: library
ms.pagetype: deploy
audience: admin
manager: laurawi
ms.audience: itpro
author: greg-lindsay
ms.author: greglin
ms.collection: M365-modern-desktop
ms.topic: article
ms.date: 12/08/2020
appliesto:
- Surface Hub 2S
ms.openlocfilehash: 076d29462ffb949492291e120bcdad538f4287ec
ms.sourcegitcommit: e859374f90d640a5cd4be1c8dcc823bcd537ebdc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "11393592"
---
# <a name="configure-windows-10-pro-or-enterprise-on-surface-hub-2"></a>Configurer Windows 10 Professionnel ou Entreprise sur Surface Hub 2

Une fois que vous avez terminé le processus d’installation de la migration vers Windows 10 Professionnel ou Entreprise, vous pouvez effectuer les étapes suivantes pour configurer les applications et les paramètres sur votre Surface Hub 2. Ces étapes sont recommandées pour garantir la meilleure expérience possible lors de l’utilisation de cet ordinateur tactile et stylet personnalisé sur grand écran.

Lorsque vous effectuez ces étapes, il peut s’avérer utile d’utiliser un clavier et une souris câblés ou sans fil.

## <a name="configure-system-settings"></a>Configurer les paramètres système

1. Connectez-vous avec un compte qui dispose de privilèges d’administrateur local sur l’appareil.  

    - Sur les appareils joints à Azure AD, l’utilisateur qui effectue la jointre Azure AD est automatiquement ajouté au groupe d’administrateurs local. Les administrateurs globaux Azure AD et les administrateurs d’appareils Azure AD sont <a href="https://docs.microsoft.com/azure/active-directory/devices/assign-local-admin" target="_blank"> également des administrateurs </a> locaux. 
    
    - Vous pouvez taper **net localgroup administrators** at a command prompt to list the accounts that have local administrator rights.
    
2. Renommez l’appareil à l’aide d’un nom convivial, par exemple **: username-SHub-Desktop**.

3. Sélectionnez ****  >  **Paramètres de démarrage**  >  **Comptes**  >  **Synchroniser vos paramètres** et désactiver **les paramètres de** synchronisation. 

    - Les paramètres utilisés ici sont destinés à permettre la meilleure expérience tactile sur grand écran et, par conséquent, vous ne souhaitez peut-être pas synchroniser d’autres appareils.
    
4. Redémarrez l’appareil.

## <a name="enable-the-touch-keyboard-and-touchpad"></a>Activer le clavier tactile et le pavé tactile

1. Sélectionnez **Paramètres**de démarrage - Saisie des périphériques et activer l’écran du clavier tactile  >  ****  >  ****  >  **** **lorsqu’il n’est** pas en mode tablette et qu’aucun clavier n’est connecté.

2. Appuyez de nouveau ou cliquez avec **** le bouton droit sur la barre des tâches, puis sélectionnez Afficher le bouton du clavier tactile et Afficher le **bouton du pavé tactile.** 

    - Le clavier tactile est utile pour les entrées directes de l’utilisateur, et le pavé tactile virtuel facilite les sélections précises, les pointes de l’écran de pointage ou comme alternative à l’utilisation d’un clic droit pour appuyer et maintenir. 
    
    - Consultez l’exemple suivant.

      ![Paramètres tactiles](images/touch.png)

3. Configurez le clavier tactile sur QWERTY et flottant.

    1. Sélectionnez **l’icône** Clavier dans la barre des tâches pour afficher le clavier tactile.
    
    1. Sur le clavier tactile, sélectionnez l’icône du clavier dans le coin supérieur gauche pour ouvrir les paramètres du clavier.
    
    1. Sélectionnez le dernier type de clavier sur la ligne supérieure pour activer QWERTY et la dernière option sur la deuxième ligne pour activer le flottant, ce qui est très utile sur ce grand écran. Consultez les exemples suivants.

       ![Paramètres du clavier](images/kbd.png)
 
4. Configurez les paramètres du clavier virtuel.

    1. Sélectionnez **l’icône Paramètres** sur le clavier tactile ou recherchez et ouvrez **les paramètres de saisie.**
    
       ![Paramètres du clavier virtuel](images/sh2-softkeyboard.png)

    1. Activez toutes les options sous Clavier orthographique, de saisie et tactile.


L’exemple suivant montre le trackpad, ce qui est utile pour naviguer et sélectionner des options. Le clavier à l’écran est utilisé pour effectuer des recherches dans le Microsoft Store :

![Utilisation du trackpad](images/store.png)

## <a name="configure-bluetooth-keyboard-and-mouse-optional"></a>Configurer Bluetooth clavier et souris (facultatif)

Connectez un clavier et une souris si vous utilisez l’appareil comme périphérique Windows principal, ou si vous l’utilisez souvent pour la saisie ou le travail de précision.

Si votre appareil Surface Hub est proche d’un PC, vous pouvez utiliser la souris sans bordure pour vous déplacer en toute transparence entre le <a href="https://aka.ms/mm" target="_blank"> Surface Hub et le </a> PC. Pour plus d’informations, <a href="https://blogs.microsoft.com/ai/microsoft-download-from-the-garage-mouse-without-borders/" target="_blank"> voir téléchargement Microsoft à partir de The Garage: Mouse without Borders. </a>

## <a name="example-of-taskbar-layout"></a>Exemple de disposition de la barre des tâches

Après avoir effectué les étapes ci-dessous pour configurer votre Surface Hub 2 pour Windows 10 Professionnel ou Entreprise, nous vous recommandons d’utiliser l’épinglage de vos applications les plus utilisées à la barre des tâches pour un lancement tactile rapide de chaque application. Voici un exemple de ce à quoi pourrait ressembler votre barre des tâches :

 ![Disposition de la barre des tâches](images/taskblyt.png)
### <a name="update-installed-apps"></a>Mettre à jour les applications installées

Pour mettre à jour toutes les applications du Windows Store installées :

1. Ouvrez l’application du Microsoft Store et sélectionnez **les** autres ellipses dans le coin supérieur droit.
2. Sélectionnez **Téléchargements et mises à jour.**
3. Sélectionner **Obtenir les mises à jour**

### <a name="scan-for-and-install-all-windows-updates"></a>Recherchez et installez toutes les mises à jour Windows
Après la migration vers Windows 10 Professionnel ou Windows 10 Entreprise, vous pouvez installer des mises à jour de maintenance et de fonctionnalités. 

- Go to **Settings**  >  **Update & Security** > and then select Check for **updates**.
- S’il existe des mises à jour, installez-les, redémarrez, puis répétez le processus jusqu’à ce que la notification suivante s’insère :

> [!div class="mx-imgBorder"]
> ![Notification « Vous êtes à jour » de Windows Update](images/wustatus.png)


## <a name="onedrive-for-business"></a>OneDriveEntreprise

Utilisez OneDrive Entreprise pour partager facilement des outils, des journaux et d’autres <a href="https://docs.microsoft.com/onedrive/onedrive" target="_blank"> fichiers entre tous vos appareils de </a> travail.

- OneDrive vous permet de partager vos fichiers de travail entre vos ordinateurs portables, votre bureau Surface Hub et vos appareils mobiles gérés par Intune. Les fichiers peuvent être modifiés sur n’importe quel appareil, et tous les appareils connectés au réseau seront mis à jour avec les modifications.

- Si vous examinez la taille du SSD Surface Hub (128 Go), si vous configurez OneDrive sur votre appareil de bureau Surface Hub, assurez-vous que la configuration par défaut consiste à conserver les fichiers en ligne et à télécharger les fichiers pendant que vous les utilisez.

Pour configurer OneDrive pour télécharger des fichiers **** uniquement si nécessaire, définissez le paramètre Fichiers à la demande sur Économiser de l’espace et téléchargez les fichiers à mesure que **vous les utilisez.** Pour plus d’informations, voir Requête et définir des états De fichiers <a href="https://docs.microsoft.com/onedrive/files-on-demand-windows" target="_blank"> à la demande dans Windows </a> .

![Paramètres OneDrive](images/onedrive.png)

> [!NOTE]
> Vous pouvez également répéter ces étapes pour configurer un OneDrive personnel, mais assurez-vous d’économiser de l’espace disque et de télécharger uniquement les fichiers dont vous avez besoin.

## <a name="sharepoint-and-teams"></a>SharePoint et Teams

Les fichiers de canal SharePoint et Teams peuvent également être synchronisés localement avec vos appareils de bureau, tels que les ordinateurs portables et les Surface Hub, à l’aide du moteur de synchronisation OneDrive.

Pour synchroniser des fichiers d’entreprise internes avec votre lecteur local avec l’application de synchronisation OneDrive :

1. Accédez à un site SharePoint et accédez au répertoire de documents de niveau supérieur pour les fichiers que vous souhaitez afficher ou modifier à partir de votre appareil local.

2. Sélectionnez le **bouton Synchroniser** en haut du ruban SharePoint.

3. Sélectionnez **Ouvrir** sur la fenêtre popup **Ce site tente d’ouvrir Microsoft OneDrive.**

4. Vérifiez que les fichiers SharePoint sont synchronisés avec votre lecteur local en sélectionnant sur l’icône OneDrive en bas à droite de la barre des tâches.

5. Vérifiez que la configuration est définie pour conserver les fichiers en ligne et téléchargez les fichiers uniquement lorsque vous les utilisez :

    1. Ouvrez l’Explorateur de fichiers.
    
    2. Accédez à et cliquez avec le bouton droit sur votre nom SharePoint ; par exemple, **Contoso \<SharePoint Document Folder Name\> \ **.
    
    3. Sélectionnez **Libérer de l’espace.**
    
    4. La colonne État affiche l’état des fichiers et des dossiers. Pour plus d’informations, voir <a href="https://support.microsoft.com/office/sync-sharepoint-files-with-the-onedrive-sync-client-groove-exe-59b1de2b-519e-4d3a-8f45-51647cf291cd" target="_blank"> Synchroniser des fichiers SharePoint avec le client de synchronisation OneDrive. </a>
    
6. Les fichiers de canal Teams sont stockés dans des sites SharePoint, avec les mêmes fonctionnalités de document SharePoint, notamment l’historique des versions et la synchronisation avec vos appareils de bureau locaux. Pour synchroniser les fichiers du canal Teams :

    1. Accédez au canal Teams qui vous intéresse et sélectionnez **l’onglet Fichiers** dans la partie supérieure. Ensuite, **sélectionnez Synchroniser.** Les fichiers démarrent la synchronisation et sont visibles dans l’Explorateur de fichiers au **bureau \ \<name of the Teams Channel\> Contoso \ **.
    
    2. Utilisez la même procédure que celle que vous avez utilisée pour synchroniser les sites SharePoint afin de conserver les fichiers dans le cloud et **** de les télécharger uniquement lorsque vous les utilisez, en tapant et maintenant ou en cliquant avec le bouton droit dans l’Explorateur de fichiers sur le nom du canal Teams, puis en sélectionnant Libérer de l’espace.

## <a name="surface-hub-pen-settings"></a>Paramètres du stylet Surface Hub

**Jumeler Bluetooth stylet Surface Hub**

Associez le stylet pour maintenir le microprogramme du stylet à jour, définissez les raccourcis du stylet et obtenez des informations sur la charge de la batterie sur la page des paramètres de l’appareil Bluetooth ou dans l’application Surface :

1. Sélectionnez ****  >  **Périphériques de paramètres de**  >  **démarrage.**

2. Sélectionnez **Ajouter Bluetooth ou un autre appareil.**

3. Choisissez **Bluetooth**.

4. Supprimez le bouton avant du stylet et agitez-le pour déconnecter la connexion de la batterie.

5. Resserez la let, puis maintenez-la en place jusqu’à ce que le coupage clignote.

6. Sur les paramètres de Bluetooth surface Hub, choisissez **stylet Surface Hub 2.**

7. Terminez l’opération de jumelage. 

8. Si le jumelage ne réussit pas, vous pouvez essayer de jumeler à nouveau le stylet. Si cela ne fonctionne pas, vous pouvez tester si la batterie est chargée en vérifiant que le stylet fonctionne dans l’application Tableau blanc. Si ce n’est pas le cas, remplacez la batterie, puis tentez à nouveau d’apparier le stylet. Si nécessaire, redémarrez l’appareil, puis réessayez.

**Définir des raccourcis de stylet** Le stylet Surface Hub possède un bouton de raccourci parfois appelé « clic arrière ». Pour configurer des raccourcis, vous devez d’abord coupler le stylet, comme décrit précédemment.

1. Recherchez stylet et **sélectionnez Stylet & paramètres Windows Ink.**

2. Dans la partie inférieure de la page, sélectionnez les raccourcis stylet qui ouvrent la boîte de dialogue, présentée ici :

   ![Raccourcis du stylet](images/sh2-pen-shortcuts.png)

## <a name="camera-configuration"></a>Configuration de l’appareil photo

Vous pouvez monter l’appareil photo en haut ou de part et d’autre de l’appareil. Montez l’appareil photo à une position pour optimiser l’angle de la caméra si vous utilisez le Hub avec un support de bureau au lieu d’un panier, ou si vous êtes à proximité du Hub. L’appareil photo ne pivote pas automatiquement, vous devez donc avoir une touche hex de 2 mm pour faire pivoter manuellement la caméra. 

Pour plus d’informations sur le montage latéral de l’appareil photo et la rotation manuelle de l’appareil photo, voir l’orientation de l’objectif de l’appareil photo <a href="https://support.microsoft.com/help/4509729/surface-hub-2s-camera-lens-orientation" target="_blank"> Surface Hub 2S. </a>

## <a name="windows-hello-configuration"></a>Configuration de Windows Hello

Surface Hub 2S exécutant Windows 10 Entreprise permet la suite complète d’applications de bureau Win32, ainsi que les options Windows Hello biométriques. L’accesseur lecteur d’empreintes digitales Surface Hub 2 peut être branché sur n’importe quel port USB-C de l’appareil. 

Pour commander un lecteur d’empreintes digitales Surface Hub 2 ou afficher des spécifications techniques, voir (surface-hub-2-essential-add-ons.md» target="_blank">Essential add-ons for Windows 10 Pro and Enterprise on Surface Hub 2 </a> . 

Après avoir inséré le **** lecteur d’empreintes digitales, sélectionnez Les  >  **paramètres**de démarrage comptes se connectent  >  ****  >  **aux options**  >  **Windows Hello Fingerprint** pour inscrire votre empreinte digitale.

Utilisez un appareil certifié Windows Hello pour la reconnaissance faciale. L’appareil photo Surface Hub 2S ne prend pas en charge la reconnaissance faciale Windows Hello.

## <a name="enable-a-lock-screen-shortcut-icon-on-the-taskbar"></a>Activer une icône de raccourci d’écran de verrouillage dans la barre des tâches

Pour ajouter une icône à la barre des tâches qui active le verrouillage d’écran tactile semblable au raccourci clavier Windows-L : 

1.  Appuyez et maintenez la souris ou cliquez avec le bouton droit sur le Bureau, sélectionnez **Nouveau**  >  **raccourci**  >  **Parcourir**  >  **le Bureau**  >  **OK**  >  **Suivant.**

1.  Fournissez un nom pour le raccourci tel que **Verrouiller mon PC,** puis sélectionnez **Terminer.**

1.  Cliquez avec le bouton droit ou appuyez et maintenez le raccourci nouvellement créé sur le Bureau, puis sélectionnez **Propriétés.** Sous **l’onglet Raccourci,** entrez ce qui suit dans le **champ** ** Cible :Rundll32.exe User32.dll,LockWorkStation**

1.  Sélectionnez le **bouton Modifier l’icône** et ** accédezC:\Windows\System32\imageres.dll** puis sélectionnez une icône à utiliser. 

    Consultez l’exemple suivant:

    ![Choisir une icône](images/lock.png)
    
1.  Sélectionnez **OK** pour enregistrer le raccourci.

1.  Cliquez ou appuyez avec le bouton droit et maintenez le raccourci, puis sélectionnez **Épingler à la barre des tâches.**

1. Une fois que vous avez épinglé le raccourci de verrouillage à la barre des tâches, vous pouvez le supprimer du Bureau.

## <a name="applications"></a>Applications


### <a name="microsoft-whiteboard"></a>Tableau blanc Microsoft

Pour installer le tableau blanc Microsoft :

 - Sélectionnez **l’icône Espace** de travail Windows Ink en bas à droite de la barre des tâches et téléchargez **tableau blanc.**
 
   ![Espace de travail d’entrée manuscrite](images/ink.png) 

Vous pouvez également installer tableau blanc à partir du Microsoft Store :

1. Ouvrez l’application du Microsoft Store et recherchez **Tableau blanc.**

2. Choisissez **Non merci** pour vous inscrire et l’utiliser sur tous les appareils.

3. Épinglez tableau blanc à la barre des tâches.

### <a name="surface-app"></a>Application Surface

1. Dans le Microsoft Store, recherchez **Surface**.

2. Définissez **le filtre Disponible sur** Tous les **appareils.**

3. Installez **l’application Surface.** Il doit s’agit de la première application répertoriée. Vous devrez peut-être associer votre compte MSA au Store pour installer l’application.

4. Épinglez **l’application Surface** à la barre des tâches.

### <a name="snip--sketch"></a>Capture d'écran et Croquis

1. Ouvrez **l’application & Sketch** et épinglez-la à la barre des tâches.

2. Sélectionnez les ellipses dans le coin supérieur droit, puis sélectionnez **Paramètres.**

3. Dans **Paramètres,** activer la copie automatique dans **le Presse-papiers,** enregistrer **les snips**et plusieurs **fenêtres** (facultatif).

### <a name="microsoft-office"></a>Microsoft Office

1. Ouvrez <a href="https://portal.office.com/account#installs" target="_blank"> le portail Office et installez les applications </a> souhaitées.

2. Épinglez les applications Office souhaitées à la barre des tâches.

3. Si Outlook est installé, assurez-vous de définir l’OST Outlook de sorte qu’il enregistre uniquement le cache des deux dernières semaines. Cela permet de réduire considérablement l’utilisation du disque et le temps d’installation.

    - Sélectionnez ****  >  **Paramètres du compte de fichier** et sélectionnez votre compte.
    
    - Sélectionnez **Modifier** et définissez le curseur pour utiliser le **mode Exchange** mis en cache sur 14 jours.

### <a name="microsoft-teams"></a>Microsoft Teams

1. Téléchargez et installez <a href="https://teams.microsoft.com/downloads" target="_blank"> Microsoft </a> Teams.

2. Configurer les paramètres de l’application de démarrage automatique (facultatif).

3. Épinglez Teams à la barre des tâches.

4. Envisagez de réduire les notifications Teams sur l’appareil pour éviter les distractions (facultatif).

   ![Notifications Teams](images/teams.png)

### <a name="connect-app"></a>Application de connexion

> [!IMPORTANT]
> Dans Windows 10, version 2004 et ultérieure, l’application Se connecter pour la projection sans fil à l’aide de Miracast n’est pas installée par défaut, mais elle est disponible en tant que fonctionnalité facultative. Si vous avez installé (ou mis à jour vers) Windows version 2004 ou ultérieure, vous pouvez voir les informations suivantes sur l’écran Projeter sur ce PC dans les paramètres :

![Projeter sur ce PC](images/sh2-project.png) 


1. Pour installer l’application à partir de la page de paramètres « Projecting to this PC », sélectionnez **Fonctionnalités**facultatives Ajouter une fonctionnalité, puis installez l’application  >  **** **Affichage** sans fil.

2. Sous certains appareils Windows et Android, vous pouvez projeter sur ce PC lorsque vous dites que **c’est OK,** choisissez :

    - **Disponible partout si** l’appareil ne se trouve pas sur un réseau d’entreprise.
    - Dans le cas contraire, choisissez **Disponible partout sur les réseaux sécurisés.**
    
3. Under **Ask to project to this PC**, choose First time **only**.

4. Under **Require PIN for pairing**, choose **Never**.

5. Pour lancer l’application et l’épingler à la barre des tâches, recherchez **Connect**.

6. Ouvrez l’application. Lorsque l’application est ouverte, cliquez avec le bouton droit sur l’icône Connecter l’application dans la barre des tâches, puis sélectionnez épingler **à la barre des tâches.**

7. Fermez ensuite l’application Se connecter. **Project to this PC** might not work unless the app has been run at least once.

Configuration recommandée lorsqu’elle n’est pas sur le réseau d’entreprise :

![Paramètres à la maison](images/project1.png)

Configuration recommandée sur le réseau d’entreprise :

![Paramètres au travail](images/project2.png)

### <a name="your-phone"></a>Votre Téléphone

**L’application** Votre téléphone est installée par défaut sur Windows 10. S’il n’est pas présent, vous pouvez également l’installer à partir du Windows Store.

Pour plus d’informations sur la configuration de l’application, voir Comment configurer votre téléphone sur Windows 10 et synchroniser les données <a href="https://www.windowscentral.com/how-set-your-phone-windows-10" target="_blank"> entre votre PC et votre téléphone </a> . Découvrez également <a href="https://www.windowscentral.com/how-fix-common-problems-your-phone-app-windows-10" target="_blank"> comment résoudre les problèmes courants liés à votre application Téléphone sur Windows 10. </a>

###  <a name="fancy-zones"></a>Zones de ville


**Les zones de** ville font partie d’un ensemble d’outils <a href="https://github.com/microsoft/PowerToys/releases" target="_blank"> appelés PowerToys </a> sur GitHub. Il s’agit d’un excellent moyen d’utiliser l’espace de l’écran sur un Surface Hub 2 en vous donnant la possibilité de définir des dispositions fixes sur votre écran (« zones ») et de sélectionner l’application qui s’exécutera ensuite dans chaque zone. 


Le [wiki PowerToys](https://github.com/microsoft/PowerToys/wiki) dispose d’instructions sur l’utilisation et la personnalisation de chaque outil, y compris [FancyZones](https://github.com/microsoft/PowerToys/wiki/FancyZones-Overview). À un niveau élevé : après avoir installé PowerToys, vous pouvez sélectionner ou créer une disposition personnalisée, puis maintenir la touche de déplacement vers le bas et faire glisser ou utiliser des touches de clavier pour déplacer une application en cours d’exécution dans des zones spécifiques. L’utilisation d Bluetooth clavier et d’une souris USB vous aidera, ou vous pouvez utiliser le clavier tactile à l’écran et le pavé tactile.

**Conseils power toys**
- Pour recevoir des notifications par courrier électronique des mises à jour de publication powerToys sur GitHub, cliquez sur le bouton « Inscription » en haut de la [page.](https://github.com/microsoft/PowerToys/releases)
- Une fois PowerToys installé, vous pouvez recevoir des notifications Windows et/ou télécharger et installer les dernières mises à jour en configurant les **paramètres** PowerToys Télécharger automatiquement les mises à jour.
- Pour obtenir les paramètres PowerToys, sélectionnez la **carat** haut exécutant les applications dans la barre des tâches, puis cliquez avec le bouton droit ou appuyez sur l’icône PowerToys jusqu’à ce que le menu s’affiche. Sélectionnez « Paramètres ».
- En bas de la page des paramètres PowerToys, activer automatiquement le téléchargement **des** mises à jour.
- Lorsqu’une mise à jour a été publiée, une notification Windows s’affiche, vous donnant la possibilité de savoir quand installer la mise à jour.


### <a name="edge-chromium-browser"></a>Navigateur Edge Chromium

Téléchargez et installez le nouveau <a href="https://www.microsoft.com/en-us/edge?form=MY01BL&OCID=MY01BL" target="_blank"> navigateur Edge Chromium. </a>


### <a name="surface-hub-hardware-diagnostic-tool"></a>Outil de diagnostic du matériel Du Surface Hub

L’outil de diagnostic du matériel Surface <a href="https://www.microsoft.com/p/surface-hub-hardware-diagnostic/9nblggh51f2g" target="_blank"> Hub </a> disponible gratuitement à partir du Microsoft Store. L’outil est conçu pour vous aider à vous assurer que votre Surface Hub s’exécute au mieux. Il contient des tests pour déterminer si votre microprogramme est à jour et configuré correctement. Les tests interactifs vous permettent de confirmer que les fonctionnalités essentielles fonctionnent comme prévu. Si des problèmes surviennent, les résultats peuvent être enregistrés et partagés avec l’équipe du Support Surface Hub. Cliquez sur le lien pour l’installer à partir du Microsoft Store, puis épinglez l’application à votre barre des tâches.

## <a name="additional-settings"></a>Paramètres supplémentaires

### <a name="pen-tail-select-to-launch-whiteboard"></a>Stylet tail select to launch Whiteboard

1. Recherchez **stylet** et **sélectionnez Stylet & paramètres Windows Ink.**

2. Dans la partie inférieure de la page, sous les **raccourcis stylet,** définissez **Sélectionner** une fois sur **Tableau blanc Microsoft.** 

### <a name="power-management"></a>Gestion de l’alimentation

Plusieurs paramètres d’alimentation sont disponibles pour obtenir la meilleure expérience possible à l’aide de Windows 10 Professionnel ou Entreprise sur Surface Hub 2. Cela inclut les délai d’affichage d’écran et de pc et la façon dont ils interagissent avec la détection de présence humaine intégrée (Doppler), l’économiseur d’écran et la protection par mot de passe, puis, le cas échéant, comment passer les paramètres d’alimentation de stratégie de groupe destinés aux utilisateurs d’ordinateurs portables/de bureau.

Windows 10 Professionnel ou Entreprise sur Surface Hub 2 empêche l’écran de passer en veille par les actions tactiles, de souris et de clavier, ainsi que par la détection d’occupation humaine intégrée (Doppler). La détection de l’occupation humaine est activée par défaut, mais si vous le souhaitez, elle peut être désactivée dans UEFI en basculeant l’option d’appareil dans l’outil De configuration UEFI Surface dans le cadre de la migration initiale ou en construisant et en appliquant un package de configuration UEFI ultérieur. 

**Gestion de l’alimentation : paramètres de veille d’écran et de PC**

1. Sélectionnez **Démarrer**  >  **l’alimentation**  >  **système**  >  **des paramètres & veille.**

2. Définissez le curseur en mode d’alimentation **sur Les meilleures performances.**

3. Configurez les valeurs d’écran et de veille selon vos préférences, tout en maintenant compte de la détection de présence Doppler qui s’affiche lorsque des mouvements sont détectés. Par conséquent, il est recommandé de définir Screen to **Turn off after 2 hours** et le PC à Turn off après **4 heures.**

**Gestion de l’alimentation : économiseur d’écran**

1. Recherchez les **paramètres de l’écran de** verrouillage et ouvrez **l’écran de verrouillage.**

2. Configurez les **paramètres de délai d’affichage de** l’écran et de l’économiseur **d’écran** à votre préférence. Les valeurs par défaut recommandées sont les :

   - Économiseur d’écran dans (Aucun) ou un économiseur d’écran de votre choix.
   - Délai d’attente de 15 minutes.
   - À la reprise, affichez l’écran d’accueil.


**Gestion de l’alimentation : stratégie de groupe**

Avant d’effectuer la procédure suivante, consultez votre service informatique pour obtenir votre approbation afin d’exclure un appareil Surface Hub 2S de la stratégie globale de gestion de l’alimentation. Certains paramètres de gestion de l’alimentation peuvent désactiver la fonction de détection de présence.

1. Recherchez **le Centre logiciel et** ouvrez-le.

2. Sélectionnez **options.**

3. Développez la **gestion de l’alimentation** et sélectionnez Ne pas appliquer les **paramètres d’alimentation de mon service informatique à cet ordinateur.**

   ![Paramètres logiciels](images/soft-cntr.png)

### <a name="storage-sense"></a>Assistant Stockage

Le Surface Hub 2 dispose d’un SSD de 128 Go pour le stockage local. Il est donc nécessaire d’envisager l’utilisation de mesures d’enregistrement de stockage lors d’une utilisation normale.  Pour configurer l’Sens du stockage :

1.  Recherchez **les paramètres de stockage,** qui se trouvent sous **Paramètres système.**

2.  Sous **Paramètres,** **sélectionnez Activer le sens du stockage** pour ouvrir la page **Paramètres** de stockage.

3.  Activer l’Sense de **stockage.**

4.  Sélectionnez **Configurer l’Sens** du stockage ou exécutez-le maintenant et configurez les paramètres pour conserver les fichiers en ligne autant que possible (en raison de l’espace disque limité).

Paramètres recommandés :

- Exécuter l’Sens du stockage = Tous les jours.
- Supprimer les fichiers temporaires que mes applications n’utilisent pas = Tous les 14 jours (au moins).
- Supprimez des fichiers dans mon dossier Téléchargements s’ils y sont depuis plus de 30 jours.
- OneDrive : le contenu devient en ligne uniquement s’il n’est pas ouvert pendant plus de = 30 jours.

### <a name="tablet-mode"></a>Mode tablette

Activer le mode tablette si vous le souhaitez pour des besoins d’accessibilité.


### <a name="sound-settings"></a>Paramètres sonores

1. Recherchez **les paramètres sons et** ouvrez cette page.

2. Sélectionnez **panneau de contrôle sonore** sur la droite et sélectionnez **l’onglet Sons.**

3. Sous **Les événements de programme** **définissent Device Connect** et Device **Disconnect** sur **None**.

### <a name="silence-notifications"></a>Notifications de silence

1. Recherchez **l’assistance focus** et ouvrez cette page.

2. Sélectionnez **Alarmes uniquement.** Cela permet d’éviter les volants de notification constants.

### <a name="disk-cleanup"></a>Nettoyage de disque

1. Recherchez **nettoyage de disque et** ouvrez cette application.

2. Sous **Fichiers à supprimer,** sélectionnez les fichiers à supprimer. 

3. Sélectionnez également **Nettoyer les fichiers système.**

## <a name="complete-and-verify"></a>Terminer et vérifier

1. Recherchez et installez toutes les mises à jour Windows.

2. Mettre à jour la stratégie de groupe.

   1. À une invite de commandes avec élévation de niveau élevé, entrez **gpupdate /force /boot /wait:0**.
   
3. Redémarrez l’appareil.

4. Vérifiez les applications de la barre des tâches.

   - Se connecter à l’application
   - Icône Verrouiller
   - Capture d'écran et Croquis
   - Teams (le cas échéant)
   - Applications Office (le cas échéant)
   - Application Surface
   - Tableau blanc
    
5. Vérifier la détection de présence.

   - La détection de présence sera une icône verte dans le bac du système.
    
6. Vérifiez que la projecting sur ce PC est activée avec l’application Connect. Après avoir configuré  **Project sur les paramètres** de ce PC, exécutez l’application Se connecter au moins une fois. (Par la suite, l’application De connexion n’a pas besoin d’être en cours d’exécution pour projeter sur le Surface Hub.)

7. Vérifiez les paramètres d’alimentation et de veille.

    - Économiseur d’écran : 15 minutes, définie sur (aucun), Mystify ou Blank ; vérifiez que la case à cocher nécessitant un mot de passe est cocher.
    - Écran : **désactiver après 2 heures.**
    - PC : **désactiver après 4 heures.**
    
8. Vérifiez que Windows Hello fonctionne.

9. Vérifiez que la synchronisation de vos paramètres est désactivée.

10. Vérifiez les applications de démarrage.

> [!TIP]
> Après avoir installé et configuré Windows 10, le Surface Hub 2S peut être géré comme n’importe quel autre appareil Windows 10.

## <a name="related-topics"></a>Rubriques associées

<a href="surface-hub-2s-migrate-os.md" target="_blank"> Migrer vers Windows10 Professionnel ou Entreprise sur Surface Hub2</a>
