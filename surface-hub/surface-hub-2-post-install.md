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
# <a name="configure-windows-10-pro-or-enterprise-on-surface-hub-2"></a><span data-ttu-id="2d3a6-104">Configurer Windows 10 Professionnel ou Entreprise sur Surface Hub 2</span><span class="sxs-lookup"><span data-stu-id="2d3a6-104">Configure Windows 10 Pro or Enterprise on Surface Hub 2</span></span>

<span data-ttu-id="2d3a6-105">Une fois que vous avez terminé le processus d’installation de la migration vers Windows 10 Professionnel ou Entreprise, vous pouvez effectuer les étapes suivantes pour configurer les applications et les paramètres sur votre Surface Hub 2.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-105">After you have completed the installation process of migrating to Windows 10 Pro or Enterprise, you can perform the following steps to configure apps and settings on your Surface Hub 2.</span></span> <span data-ttu-id="2d3a6-106">Ces étapes sont recommandées pour garantir la meilleure expérience possible lors de l’utilisation de cet ordinateur tactile et stylet personnalisé sur grand écran.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-106">These steps are recommended to ensure the best experience when using this personalized large screen touch and pen computer.</span></span>

<span data-ttu-id="2d3a6-107">Lorsque vous effectuez ces étapes, il peut s’avérer utile d’utiliser un clavier et une souris câblés ou sans fil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-107">When performing these steps, you might find it useful to use a wired or wireless keyboard and mouse.</span></span>

## <a name="configure-system-settings"></a><span data-ttu-id="2d3a6-108">Configurer les paramètres système</span><span class="sxs-lookup"><span data-stu-id="2d3a6-108">Configure system settings</span></span>

1. <span data-ttu-id="2d3a6-109">Connectez-vous avec un compte qui dispose de privilèges d’administrateur local sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-109">Sign in with an account that has local administrator privileges on the device.</span></span>  

    - <span data-ttu-id="2d3a6-110">Sur les appareils joints à Azure AD, l’utilisateur qui effectue la jointre Azure AD est automatiquement ajouté au groupe d’administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-110">On Azure AD joined devices, the user that performs the Azure AD join is automatically added to the local administrator group.</span></span> <span data-ttu-id="2d3a6-111">Les administrateurs globaux Azure AD et les administrateurs d’appareils Azure AD sont <a href="https://docs.microsoft.com/azure/active-directory/devices/assign-local-admin" target="_blank"> également des administrateurs </a> locaux.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-111">Azure AD global administrators and Azure AD devices administrators are <a href="https://docs.microsoft.com/azure/active-directory/devices/assign-local-admin" target="_blank">also local administrators</a>.</span></span> 
    
    - <span data-ttu-id="2d3a6-112">Vous pouvez taper **net localgroup administrators** at a command prompt to list the accounts that have local administrator rights.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-112">You can type **net localgroup administrators** at a command prompt to list the accounts that have local administrator rights.</span></span>
    
2. <span data-ttu-id="2d3a6-113">Renommez l’appareil à l’aide d’un nom convivial, par exemple **: username-SHub-Desktop**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-113">Rename the device using a friendly name, for example: **username-SHub-Desktop**.</span></span>

3. <span data-ttu-id="2d3a6-114">Sélectionnez \*\*\*\*  >  **Paramètres de démarrage**  >  **Comptes**  >  **Synchroniser vos paramètres** et désactiver **les paramètres de** synchronisation.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-114">Select **Start** > **Settings** > **Accounts** > **Sync your settings** and turn **Sync settings** off.</span></span> 

    - <span data-ttu-id="2d3a6-115">Les paramètres utilisés ici sont destinés à permettre la meilleure expérience tactile sur grand écran et, par conséquent, vous ne souhaitez peut-être pas synchroniser d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-115">The settings used here are intended to enable the best large-screen touch experience, and therefore you may not want to sync other devices.</span></span>
    
4. <span data-ttu-id="2d3a6-116">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-116">Restart the device.</span></span>

## <a name="enable-the-touch-keyboard-and-touchpad"></a><span data-ttu-id="2d3a6-117">Activer le clavier tactile et le pavé tactile</span><span class="sxs-lookup"><span data-stu-id="2d3a6-117">Enable the touch keyboard and touchpad</span></span>

1. <span data-ttu-id="2d3a6-118">Sélectionnez **Paramètres**de démarrage - Saisie des périphériques et activer l’écran du clavier tactile  >  \*\*\*\*  >  \*\*\*\*  >  \*\*\*\* **lorsqu’il n’est** pas en mode tablette et qu’aucun clavier n’est connecté.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-118">Select **Start** > **Settings** > **Devices** > **Typing** and turn **Show the touch keyboard when not in tablet mode and there's no keyboard attached** on.</span></span>

2. <span data-ttu-id="2d3a6-119">Appuyez de nouveau ou cliquez avec \*\*\*\* le bouton droit sur la barre des tâches, puis sélectionnez Afficher le bouton du clavier tactile et Afficher le **bouton du pavé tactile.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-119">Tap and hold or right-click the taskbar and then select **Show touch keyboard button** and **Show touchpad button**.</span></span> 

    - <span data-ttu-id="2d3a6-120">Le clavier tactile est utile pour les entrées directes de l’utilisateur, et le pavé tactile virtuel facilite les sélections précises, les pointes de l’écran de pointage ou comme alternative à l’utilisation d’un clic droit pour appuyer et maintenir.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-120">The touch keyboard is helpful for direct user input, and the virtual touchpad helps with precise selections, hovering screen tips, or as an alternative to tap and hold for right-click.</span></span> 
    
    - <span data-ttu-id="2d3a6-121">Consultez l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-121">See the following example.</span></span>

      ![Paramètres tactiles](images/touch.png)

3. <span data-ttu-id="2d3a6-123">Configurez le clavier tactile sur QWERTY et flottant.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-123">Configure the touch keyboard to QWERTY and floating.</span></span>

    1. <span data-ttu-id="2d3a6-124">Sélectionnez **l’icône** Clavier dans la barre des tâches pour afficher le clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-124">Select the **Keyboard** icon on the taskbar to show the touch keyboard.</span></span>
    
    1. <span data-ttu-id="2d3a6-125">Sur le clavier tactile, sélectionnez l’icône du clavier dans le coin supérieur gauche pour ouvrir les paramètres du clavier.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-125">On the touch keyboard, select the keyboard icon in the upper left corner to open keyboard settings.</span></span>
    
    1. <span data-ttu-id="2d3a6-126">Sélectionnez le dernier type de clavier sur la ligne supérieure pour activer QWERTY et la dernière option sur la deuxième ligne pour activer le flottant, ce qui est très utile sur ce grand écran.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-126">Select the next to last keyboard type on the top row to enable QWERTY, and the last option on the second row to enable floating, which is very helpful on this large screen.</span></span> <span data-ttu-id="2d3a6-127">Consultez les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-127">See the following examples.</span></span>

       ![Paramètres du clavier](images/kbd.png)
 
4. <span data-ttu-id="2d3a6-129">Configurez les paramètres du clavier virtuel.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-129">Configure the soft keyboard settings.</span></span>

    1. <span data-ttu-id="2d3a6-130">Sélectionnez **l’icône Paramètres** sur le clavier tactile ou recherchez et ouvrez **les paramètres de saisie.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-130">Select the **Settings** icon on the touch keyboard or search for and open **Typing settings**.</span></span>
    
       ![Paramètres du clavier virtuel](images/sh2-softkeyboard.png)

    1. <span data-ttu-id="2d3a6-132">Activez toutes les options sous Clavier orthographique, de saisie et tactile.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-132">Enable all the options under Spelling, Typing, and Touch keyboard.</span></span>


<span data-ttu-id="2d3a6-133">L’exemple suivant montre le trackpad, ce qui est utile pour naviguer et sélectionner des options.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-133">The following example shows the trackpad, which is useful to navigate and select options.</span></span> <span data-ttu-id="2d3a6-134">Le clavier à l’écran est utilisé pour effectuer des recherches dans le Microsoft Store :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-134">The onscreen keyboard is being used to search the Microsoft Store:</span></span>

![Utilisation du trackpad](images/store.png)

## <a name="configure-bluetooth-keyboard-and-mouse-optional"></a><span data-ttu-id="2d3a6-136">Configurer Bluetooth clavier et souris (facultatif)</span><span class="sxs-lookup"><span data-stu-id="2d3a6-136">Configure Bluetooth keyboard and mouse (optional)</span></span>

<span data-ttu-id="2d3a6-137">Connectez un clavier et une souris si vous utilisez l’appareil comme périphérique Windows principal, ou si vous l’utilisez souvent pour la saisie ou le travail de précision.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-137">Connect a keyboard and mouse if you are using the device as your primary Windows device, or you use it often for typing or precision work.</span></span>

<span data-ttu-id="2d3a6-138">Si votre appareil Surface Hub est proche d’un PC, vous pouvez utiliser la souris sans bordure pour vous déplacer en toute transparence entre le <a href="https://aka.ms/mm" target="_blank"> Surface Hub et le </a> PC.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-138">If your Surface Hub device is near to a PC, you can use <a href="https://aka.ms/mm" target="_blank"> Mouse without Borders</a> to move seamlessly between the Surface Hub and the PC.</span></span> <span data-ttu-id="2d3a6-139">Pour plus d’informations, <a href="https://blogs.microsoft.com/ai/microsoft-download-from-the-garage-mouse-without-borders/" target="_blank"> voir téléchargement Microsoft à partir de The Garage: Mouse without Borders.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-139">For more information, see <a href="https://blogs.microsoft.com/ai/microsoft-download-from-the-garage-mouse-without-borders/" target="_blank"> Microsoft download from The Garage: Mouse without Borders.</span></span> </a>

## <a name="example-of-taskbar-layout"></a><span data-ttu-id="2d3a6-140">Exemple de disposition de la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="2d3a6-140">Example of Taskbar layout</span></span>

<span data-ttu-id="2d3a6-141">Après avoir effectué les étapes ci-dessous pour configurer votre Surface Hub 2 pour Windows 10 Professionnel ou Entreprise, nous vous recommandons d’utiliser l’épinglage de vos applications les plus utilisées à la barre des tâches pour un lancement tactile rapide de chaque application.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-141">After completing the below steps to setup/configure your Surface Hub 2 for Windows 10 Professional or Enterprise, we recommend you utilize pinning your most used applications to the Taskbar for a quick one-touch launch of each application.</span></span> <span data-ttu-id="2d3a6-142">Voici un exemple de ce à quoi pourrait ressembler votre barre des tâches :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-142">Below is an example of what your taskbar could look like:</span></span>

 ![Disposition de la barre des tâches](images/taskblyt.png)
### <a name="update-installed-apps"></a><span data-ttu-id="2d3a6-144">Mettre à jour les applications installées</span><span class="sxs-lookup"><span data-stu-id="2d3a6-144">Update installed apps</span></span>

<span data-ttu-id="2d3a6-145">Pour mettre à jour toutes les applications du Windows Store installées :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-145">To update all installed Store apps:</span></span>

1. <span data-ttu-id="2d3a6-146">Ouvrez l’application du Microsoft Store et sélectionnez **les** autres ellipses dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-146">Open Microsoft Store app and select the **See more** ellipsis in the top-right corner.</span></span>
2. <span data-ttu-id="2d3a6-147">Sélectionnez **Téléchargements et mises à jour.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-147">Select **Downloads and updates.**</span></span>
3. <span data-ttu-id="2d3a6-148">Sélectionner **Obtenir les mises à jour**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-148">Select **Get updates**</span></span>

### <a name="scan-for-and-install-all-windows-updates"></a><span data-ttu-id="2d3a6-149">Recherchez et installez toutes les mises à jour Windows</span><span class="sxs-lookup"><span data-stu-id="2d3a6-149">Scan for and install all Windows Updates</span></span>
<span data-ttu-id="2d3a6-150">Après la migration vers Windows 10 Professionnel ou Windows 10 Entreprise, vous pouvez installer des mises à jour de maintenance et de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-150">After migrating to Windows 10 Professional or Windows 10 Enterprise, there may be servicing and feature updates available for you to install.</span></span> 

- <span data-ttu-id="2d3a6-151">Go to **Settings**  >  **Update & Security** > and then select Check for **updates**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-151">Go to **Settings** > **Update & Security** > and then select **Check for updates**.</span></span>
- <span data-ttu-id="2d3a6-152">S’il existe des mises à jour, installez-les, redémarrez, puis répétez le processus jusqu’à ce que la notification suivante s’insère :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-152">If there are any updates, install them, reboot, and then repeat the process until you see the following notification:</span></span>

> [!div class="mx-imgBorder"]
> ![Notification « Vous êtes à jour » de Windows Update](images/wustatus.png)


## <a name="onedrive-for-business"></a><span data-ttu-id="2d3a6-154">OneDriveEntreprise</span><span class="sxs-lookup"><span data-stu-id="2d3a6-154">OneDrive for Business</span></span>

<span data-ttu-id="2d3a6-155">Utilisez OneDrive Entreprise pour partager facilement des outils, des journaux et d’autres <a href="https://docs.microsoft.com/onedrive/onedrive" target="_blank"> fichiers entre tous vos appareils de </a> travail.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-155">Use <a href="https://docs.microsoft.com/onedrive/onedrive" target="_blank"> OneDrive for Business</a> to easily share tools, logs, and other files between all your work devices.</span></span>

- <span data-ttu-id="2d3a6-156">OneDrive vous permet de partager vos fichiers de travail entre vos ordinateurs portables, votre bureau Surface Hub et vos appareils mobiles gérés par Intune.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-156">OneDrive enables you to share your work files between your laptops, Surface Hub Desktop, and your Intune-managed mobile devices.</span></span> <span data-ttu-id="2d3a6-157">Les fichiers peuvent être modifiés sur n’importe quel appareil, et tous les appareils connectés au réseau seront mis à jour avec les modifications.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-157">Files can be edited on any device, and all network connected devices will be updated with the changes.</span></span>

- <span data-ttu-id="2d3a6-158">Si vous examinez la taille du SSD Surface Hub (128 Go), si vous configurez OneDrive sur votre appareil de bureau Surface Hub, assurez-vous que la configuration par défaut consiste à conserver les fichiers en ligne et à télécharger les fichiers pendant que vous les utilisez.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-158">Considering the size of the Surface Hub SSD (128GB), if you configure OneDrive on your Surface Hub Desktop device, make sure the default configuration is to keep the files online and download files as you use them.</span></span>

<span data-ttu-id="2d3a6-159">Pour configurer OneDrive pour télécharger des fichiers \*\*\*\* uniquement si nécessaire, définissez le paramètre Fichiers à la demande sur Économiser de l’espace et téléchargez les fichiers à mesure que **vous les utilisez.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-159">To configure OneDrive to download files only when needed, set the **Files On-Demand** setting to **Save space and download files as you use them**.</span></span> <span data-ttu-id="2d3a6-160">Pour plus d’informations, voir Requête et définir des états De fichiers <a href="https://docs.microsoft.com/onedrive/files-on-demand-windows" target="_blank"> à la demande dans Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="2d3a6-160">For more information, see <a href="https://docs.microsoft.com/onedrive/files-on-demand-windows" target="_blank"> Query and set Files On-Demand states in Windows</a>.</span></span>

![Paramètres OneDrive](images/onedrive.png)

> [!NOTE]
> <span data-ttu-id="2d3a6-162">Vous pouvez également répéter ces étapes pour configurer un OneDrive personnel, mais assurez-vous d’économiser de l’espace disque et de télécharger uniquement les fichiers dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-162">You can also repeat these steps to configure a personal OneDrive but be sure to conserve drive space and only download files as you need them.</span></span>

## <a name="sharepoint-and-teams"></a><span data-ttu-id="2d3a6-163">SharePoint et Teams</span><span class="sxs-lookup"><span data-stu-id="2d3a6-163">SharePoint and Teams</span></span>

<span data-ttu-id="2d3a6-164">Les fichiers de canal SharePoint et Teams peuvent également être synchronisés localement avec vos appareils de bureau, tels que les ordinateurs portables et les Surface Hub, à l’aide du moteur de synchronisation OneDrive.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-164">SharePoint and Teams Channel files can also sync locally to your desktop devices, such as laptops and Surface Hubs, using the OneDrive sync engine.</span></span>

<span data-ttu-id="2d3a6-165">Pour synchroniser des fichiers d’entreprise internes avec votre lecteur local avec l’application de synchronisation OneDrive :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-165">To sync internal corporate files to your local drive with the OneDrive sync app:</span></span>

1. <span data-ttu-id="2d3a6-166">Accédez à un site SharePoint et accédez au répertoire de documents de niveau supérieur pour les fichiers que vous souhaitez afficher ou modifier à partir de votre appareil local.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-166">Go to a SharePoint site and navigate to the top-level document directory for files that you are interested in viewing or editing from your local device.</span></span>

2. <span data-ttu-id="2d3a6-167">Sélectionnez le **bouton Synchroniser** en haut du ruban SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-167">Select on the **Sync** button on the top of the SharePoint ribbon.</span></span>

3. <span data-ttu-id="2d3a6-168">Sélectionnez **Ouvrir** sur la fenêtre popup **Ce site tente d’ouvrir Microsoft OneDrive.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-168">Select on **Open** on the popup **This site is trying to open Microsoft OneDrive**.</span></span>

4. <span data-ttu-id="2d3a6-169">Vérifiez que les fichiers SharePoint sont synchronisés avec votre lecteur local en sélectionnant sur l’icône OneDrive en bas à droite de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-169">Verify that the SharePoint files are synchronizing to your local drive by selecting on the OneDrive icon at the bottom right of the taskbar.</span></span>

5. <span data-ttu-id="2d3a6-170">Vérifiez que la configuration est définie pour conserver les fichiers en ligne et téléchargez les fichiers uniquement lorsque vous les utilisez :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-170">Verify the configuration is set to keep the files online and download the files only as you use them:</span></span>

    1. <span data-ttu-id="2d3a6-171">Ouvrez l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-171">Open file explorer.</span></span>
    
    2. <span data-ttu-id="2d3a6-172">Accédez à et cliquez avec le bouton droit sur votre nom SharePoint ; par exemple, \*\*Contoso \<SharePoint Document Folder Name\> \ \*\*.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-172">Navigate to and right click your SharePoint name; for example, **Contoso \ \<SharePoint Document Folder Name\>**.</span></span>
    
    3. <span data-ttu-id="2d3a6-173">Sélectionnez **Libérer de l’espace.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-173">Select **Free up space**.</span></span>
    
    4. <span data-ttu-id="2d3a6-174">La colonne État affiche l’état des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-174">The Status column will display the status of files and folders.</span></span> <span data-ttu-id="2d3a6-175">Pour plus d’informations, voir <a href="https://support.microsoft.com/office/sync-sharepoint-files-with-the-onedrive-sync-client-groove-exe-59b1de2b-519e-4d3a-8f45-51647cf291cd" target="_blank"> Synchroniser des fichiers SharePoint avec le client de synchronisation OneDrive. </a></span><span class="sxs-lookup"><span data-stu-id="2d3a6-175">For more information, see <a href="https://support.microsoft.com/office/sync-sharepoint-files-with-the-onedrive-sync-client-groove-exe-59b1de2b-519e-4d3a-8f45-51647cf291cd" target="_blank"> Sync SharePoint files with the OneDrive sync client</a>.</span></span>
    
6. <span data-ttu-id="2d3a6-176">Les fichiers de canal Teams sont stockés dans des sites SharePoint, avec les mêmes fonctionnalités de document SharePoint, notamment l’historique des versions et la synchronisation avec vos appareils de bureau locaux.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-176">Teams Channel files are stored in SharePoint sites, with all of the same SharePoint document functionality, including version history and synchronizing to your local desktop devices.</span></span> <span data-ttu-id="2d3a6-177">Pour synchroniser les fichiers du canal Teams :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-177">To sync Teams Channel files:</span></span>

    1. <span data-ttu-id="2d3a6-178">Accédez au canal Teams qui vous intéresse et sélectionnez **l’onglet Fichiers** dans la partie supérieure.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-178">Navigate to the Teams Channel of interest and select the **Files** tab at the top.</span></span> <span data-ttu-id="2d3a6-179">Ensuite, **sélectionnez Synchroniser.** Les fichiers démarrent la synchronisation et sont visibles dans l’Explorateur de fichiers au \*\*bureau \ \<name of the Teams Channel\> Contoso \ \*\*.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-179">Then select **Sync**. The files will start synchronizing and will be visible in File Explorer at **Desktop \ Contoso \ \<name of the Teams Channel\>**.</span></span>
    
    2. <span data-ttu-id="2d3a6-180">Utilisez la même procédure que celle que vous avez utilisée pour synchroniser les sites SharePoint afin de conserver les fichiers dans le cloud et \*\*\*\* de les télécharger uniquement lorsque vous les utilisez, en tapant et maintenant ou en cliquant avec le bouton droit dans l’Explorateur de fichiers sur le nom du canal Teams, puis en sélectionnant Libérer de l’espace.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-180">Use the same procedure that you used for synchronizing SharePoint sites to keep the files in the cloud and only download them when you use them, by tap and hold or right-click in File Explorer on the Teams Channel name, and then selecting **Free up space**.</span></span>

## <a name="surface-hub-pen-settings"></a><span data-ttu-id="2d3a6-181">Paramètres du stylet Surface Hub</span><span class="sxs-lookup"><span data-stu-id="2d3a6-181">Surface Hub pen settings</span></span>

**<span data-ttu-id="2d3a6-182">Jumeler Bluetooth stylet Surface Hub</span><span class="sxs-lookup"><span data-stu-id="2d3a6-182">Pair the Bluetooth Surface Hub Pen</span></span>**

<span data-ttu-id="2d3a6-183">Associez le stylet pour maintenir le microprogramme du stylet à jour, définissez les raccourcis du stylet et obtenez des informations sur la charge de la batterie sur la page des paramètres de l’appareil Bluetooth ou dans l’application Surface :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-183">Pair the pen to keep the pen firmware up to date, set the pen shortcuts, and get battery charge information on the Bluetooth device settings page, or in the Surface app:</span></span>

1. <span data-ttu-id="2d3a6-184">Sélectionnez \*\*\*\*  >  **Périphériques de paramètres de**  >  **démarrage.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-184">Select **Start** > **Settings** > **Devices**.</span></span>

2. <span data-ttu-id="2d3a6-185">Sélectionnez **Ajouter Bluetooth ou un autre appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-185">Select **Add Bluetooth or other device**.</span></span>

3. <span data-ttu-id="2d3a6-186">Choisissez **Bluetooth**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-186">Choose **Bluetooth**.</span></span>

4. <span data-ttu-id="2d3a6-187">Supprimez le bouton avant du stylet et agitez-le pour déconnecter la connexion de la batterie.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-187">Remove the pen tail button and shake to disconnect the battery connection.</span></span>

5. <span data-ttu-id="2d3a6-188">Resserez la let, puis maintenez-la en place jusqu’à ce que le coupage clignote.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-188">Put the cap back on and press and hold the cap until the pairing LED flashes.</span></span>

6. <span data-ttu-id="2d3a6-189">Sur les paramètres de Bluetooth surface Hub, choisissez **stylet Surface Hub 2.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-189">On the Surface Hub Bluetooth settings, choose **Surface Hub 2 Pen**.</span></span>

7. <span data-ttu-id="2d3a6-190">Terminez l’opération de jumelage.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-190">Complete the pairing operation.</span></span> 

8. <span data-ttu-id="2d3a6-191">Si le jumelage ne réussit pas, vous pouvez essayer de jumeler à nouveau le stylet.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-191">If the pairing is not successful, you can attempt to pair the pen again.</span></span> <span data-ttu-id="2d3a6-192">Si cela ne fonctionne pas, vous pouvez tester si la batterie est chargée en vérifiant que le stylet fonctionne dans l’application Tableau blanc.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-192">If that doesn't work, you can test to see if the battery is charged by verifying the pen works in the Whiteboard application.</span></span> <span data-ttu-id="2d3a6-193">Si ce n’est pas le cas, remplacez la batterie, puis tentez à nouveau d’apparier le stylet.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-193">If not, then replace the battery and then try to pair the pen again.</span></span> <span data-ttu-id="2d3a6-194">Si nécessaire, redémarrez l’appareil, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-194">If necessary, restart the device and then try again.</span></span>

<span data-ttu-id="2d3a6-195">**Définir des raccourcis de stylet** Le stylet Surface Hub possède un bouton de raccourci parfois appelé « clic arrière ».</span><span class="sxs-lookup"><span data-stu-id="2d3a6-195">**Set pen shortcuts** The Surface Hub pen has a shortcut button sometimes referred to as a "tail click".</span></span> <span data-ttu-id="2d3a6-196">Pour configurer des raccourcis, vous devez d’abord coupler le stylet, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-196">Configuring shortcuts requires you to first pair the pen, as described earlier.</span></span>

1. <span data-ttu-id="2d3a6-197">Recherchez stylet et **sélectionnez Stylet & paramètres Windows Ink.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-197">Search for Pen and select **Pen & Windows Ink settings**.</span></span>

2. <span data-ttu-id="2d3a6-198">Dans la partie inférieure de la page, sélectionnez les raccourcis stylet qui ouvrent la boîte de dialogue, présentée ici :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-198">Near the bottom of the page, select Pen shortcuts which opens the dialog box, shown here:</span></span>

   ![Raccourcis du stylet](images/sh2-pen-shortcuts.png)

## <a name="camera-configuration"></a><span data-ttu-id="2d3a6-200">Configuration de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="2d3a6-200">Camera configuration</span></span>

<span data-ttu-id="2d3a6-201">Vous pouvez monter l’appareil photo en haut ou de part et d’autre de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-201">You can mount the camera on the top or on either side of the device.</span></span> <span data-ttu-id="2d3a6-202">Montez l’appareil photo à une position pour optimiser l’angle de la caméra si vous utilisez le Hub avec un support de bureau au lieu d’un panier, ou si vous êtes à proximité du Hub.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-202">Mount the camera in a position to optimize the camera angle if you are using the Hub with a desktop stand instead of a cart, or are in close proximity to the Hub.</span></span> <span data-ttu-id="2d3a6-203">L’appareil photo ne pivote pas automatiquement, vous devez donc avoir une touche hex de 2 mm pour faire pivoter manuellement la caméra.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-203">The camera does not auto-rotate, so you need to have a 2mm hex key to manually rotate the camera.</span></span> 

<span data-ttu-id="2d3a6-204">Pour plus d’informations sur le montage latéral de l’appareil photo et la rotation manuelle de l’appareil photo, voir l’orientation de l’objectif de l’appareil photo <a href="https://support.microsoft.com/help/4509729/surface-hub-2s-camera-lens-orientation" target="_blank"> Surface Hub 2S. </a></span><span class="sxs-lookup"><span data-stu-id="2d3a6-204">For more information on how to side-mount the camera and rotate the camera manually, see <a href="https://support.microsoft.com/help/4509729/surface-hub-2s-camera-lens-orientation" target="_blank"> Surface Hub 2S camera lens orientation</a>.</span></span>

## <a name="windows-hello-configuration"></a><span data-ttu-id="2d3a6-205">Configuration de Windows Hello</span><span class="sxs-lookup"><span data-stu-id="2d3a6-205">Windows Hello configuration</span></span>

<span data-ttu-id="2d3a6-206">Surface Hub 2S exécutant Windows 10 Entreprise permet la suite complète d’applications de bureau Win32, ainsi que les options Windows Hello biométriques.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-206">Surface Hub 2S running Windows 10 Enterprise allows the full suite of Win32 desktop applications as well as biometric Windows Hello options.</span></span> <span data-ttu-id="2d3a6-207">L’accesseur lecteur d’empreintes digitales Surface Hub 2 peut être branché sur n’importe quel port USB-C de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-207">The Surface Hub 2 Fingerprint Reader accessory can be plugged into any USB-C port on the device.</span></span> 

<span data-ttu-id="2d3a6-208">Pour commander un lecteur d’empreintes digitales Surface Hub 2 ou afficher des spécifications techniques, voir (surface-hub-2-essential-add-ons.md» target="_blank">Essential add-ons for Windows 10 Pro and Enterprise on Surface Hub 2 </a> .</span><span class="sxs-lookup"><span data-stu-id="2d3a6-208">To order a Surface Hub 2 Fingerprint Reader or view technical specs, see (surface-hub-2-essential-add-ons.md" target="_blank">Essential add-ons for Windows 10 Pro and Enterprise on Surface Hub 2 </a>.</span></span> 

<span data-ttu-id="2d3a6-209">Après avoir inséré le \*\*\*\* lecteur d’empreintes digitales, sélectionnez Les  >  **paramètres**de démarrage comptes se connectent  >  \*\*\*\*  >  **aux options**  >  **Windows Hello Fingerprint** pour inscrire votre empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-209">After inserting the fingerprint reader, select **Start** > **Settings** > **Accounts** > **Sign-in options** > **Windows Hello Fingerprint** to enroll your fingerprint.</span></span>

<span data-ttu-id="2d3a6-210">Utilisez un appareil certifié Windows Hello pour la reconnaissance faciale.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-210">Use a Windows Hello certified device for face recognition.</span></span> <span data-ttu-id="2d3a6-211">L’appareil photo Surface Hub 2S ne prend pas en charge la reconnaissance faciale Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-211">The Surface Hub 2S camera does not support Windows Hello face recognition.</span></span>

## <a name="enable-a-lock-screen-shortcut-icon-on-the-taskbar"></a><span data-ttu-id="2d3a6-212">Activer une icône de raccourci d’écran de verrouillage dans la barre des tâches</span><span class="sxs-lookup"><span data-stu-id="2d3a6-212">Enable a Lock Screen shortcut icon on the taskbar</span></span>

<span data-ttu-id="2d3a6-213">Pour ajouter une icône à la barre des tâches qui active le verrouillage d’écran tactile semblable au raccourci clavier Windows-L :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-213">To add an icon to the taskbar that enables one-touch screen lock similar to the Windows-L keyboard shortcut:</span></span> 

1.  <span data-ttu-id="2d3a6-214">Appuyez et maintenez la souris ou cliquez avec le bouton droit sur le Bureau, sélectionnez **Nouveau**  >  **raccourci**  >  **Parcourir**  >  **le Bureau**  >  **OK**  >  **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-214">Tap and hold or right-click on the desktop, select **New** > **Shortcut** > **Browse** > **Desktop** > **OK** > **Next**.</span></span>

1.  <span data-ttu-id="2d3a6-215">Fournissez un nom pour le raccourci tel que **Verrouiller mon PC,** puis sélectionnez **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-215">Provide a name for the shortcut such as **Lock my PC**, and then select **Finish**.</span></span>

1.  <span data-ttu-id="2d3a6-216">Cliquez avec le bouton droit ou appuyez et maintenez le raccourci nouvellement créé sur le Bureau, puis sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-216">Right-click or tap and hold the newly created shortcut on the desktop, and select **Properties**.</span></span> <span data-ttu-id="2d3a6-217">Sous **l’onglet Raccourci,** entrez ce qui suit dans le **champ** \*\* Cible :Rundll32.exe User32.dll,LockWorkStation\*\*</span><span class="sxs-lookup"><span data-stu-id="2d3a6-217">On the **Shortcut** tab, enter the following in the **Target** field: **Rundll32.exe User32.dll,LockWorkStation**</span></span>

1.  <span data-ttu-id="2d3a6-218">Sélectionnez le **bouton Modifier l’icône** et \*\* accédezC:\Windows\System32\imageres.dll\*\* puis sélectionnez une icône à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-218">Select the **Change Icon** button and browse to **C:\Windows\System32\imageres.dll** and select an icon to use.</span></span> 

    <span data-ttu-id="2d3a6-219">Consultez l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="2d3a6-219">See the following example:</span></span>

    ![Choisir une icône](images/lock.png)
    
1.  <span data-ttu-id="2d3a6-221">Sélectionnez **OK** pour enregistrer le raccourci.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-221">Select **OK** to save the shortcut.</span></span>

1.  <span data-ttu-id="2d3a6-222">Cliquez ou appuyez avec le bouton droit et maintenez le raccourci, puis sélectionnez **Épingler à la barre des tâches.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-222">Right-click or tap and hold the shortcut and select **Pin to taskbar**.</span></span>

1. <span data-ttu-id="2d3a6-223">Une fois que vous avez épinglé le raccourci de verrouillage à la barre des tâches, vous pouvez le supprimer du Bureau.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-223">After you have pinned the lock shortcut to the taskbar, you can delete it from the desktop.</span></span>

## <a name="applications"></a><span data-ttu-id="2d3a6-224">Applications</span><span class="sxs-lookup"><span data-stu-id="2d3a6-224">Applications</span></span>


### <a name="microsoft-whiteboard"></a><span data-ttu-id="2d3a6-225">Tableau blanc Microsoft</span><span class="sxs-lookup"><span data-stu-id="2d3a6-225">Microsoft Whiteboard</span></span>

<span data-ttu-id="2d3a6-226">Pour installer le tableau blanc Microsoft :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-226">To install the Microsoft Whiteboard:</span></span>

 - <span data-ttu-id="2d3a6-227">Sélectionnez **l’icône Espace** de travail Windows Ink en bas à droite de la barre des tâches et téléchargez **tableau blanc.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-227">Select the **Windows Ink Workspace** icon on the lower right of the taskbar and download **Whiteboard**.</span></span>
 
   ![Espace de travail d’entrée manuscrite](images/ink.png) 

<span data-ttu-id="2d3a6-229">Vous pouvez également installer tableau blanc à partir du Microsoft Store :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-229">Alternatively, you can install Whiteboard from the Microsoft Store:</span></span>

1. <span data-ttu-id="2d3a6-230">Ouvrez l’application du Microsoft Store et recherchez **Tableau blanc.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-230">Open Microsoft Store app and search for **Whiteboard**.</span></span>

2. <span data-ttu-id="2d3a6-231">Choisissez **Non merci** pour vous inscrire et l’utiliser sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-231">Choose **No thanks** to sign in and use across devices.</span></span>

3. <span data-ttu-id="2d3a6-232">Épinglez tableau blanc à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-232">Pin Whiteboard to the taskbar.</span></span>

### <a name="surface-app"></a><span data-ttu-id="2d3a6-233">Application Surface</span><span class="sxs-lookup"><span data-stu-id="2d3a6-233">Surface app</span></span>

1. <span data-ttu-id="2d3a6-234">Dans le Microsoft Store, recherchez **Surface**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-234">In the Microsoft Store, search for **Surface**.</span></span>

2. <span data-ttu-id="2d3a6-235">Définissez **le filtre Disponible sur** Tous les **appareils.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-235">Set the **Available on** filter to **All devices**.</span></span>

3. <span data-ttu-id="2d3a6-236">Installez **l’application Surface.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-236">Install the **Surface** app.</span></span> <span data-ttu-id="2d3a6-237">Il doit s’agit de la première application répertoriée.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-237">This should be the first app listed.</span></span> <span data-ttu-id="2d3a6-238">Vous devrez peut-être associer votre compte MSA au Store pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-238">You might need to associate your MSA to the Store in order to install the app.</span></span>

4. <span data-ttu-id="2d3a6-239">Épinglez **l’application Surface** à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-239">Pin the **Surface** app to taskbar.</span></span>

### <a name="snip--sketch"></a><span data-ttu-id="2d3a6-240">Capture d'écran et Croquis</span><span class="sxs-lookup"><span data-stu-id="2d3a6-240">Snip & Sketch</span></span>

1. <span data-ttu-id="2d3a6-241">Ouvrez **l’application & Sketch** et épinglez-la à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-241">Open the **Snip & Sketch** app and pin it to the taskbar.</span></span>

2. <span data-ttu-id="2d3a6-242">Sélectionnez les ellipses dans le coin supérieur droit, puis sélectionnez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-242">Select the ellipsis in the upper right corner and then select **Settings**.</span></span>

3. <span data-ttu-id="2d3a6-243">Dans **Paramètres,** activer la copie automatique dans **le Presse-papiers,** enregistrer **les snips**et plusieurs **fenêtres** (facultatif).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-243">In **Settings**, turn on **Auto copy to clipboard**, **Save snips**, and **Multiple windows** (optional).</span></span>

### <a name="microsoft-office"></a><span data-ttu-id="2d3a6-244">Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="2d3a6-244">Microsoft Office</span></span>

1. <span data-ttu-id="2d3a6-245">Ouvrez <a href="https://portal.office.com/account#installs" target="_blank"> le portail Office et installez les applications </a> souhaitées.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-245">Open the <a href="https://portal.office.com/account#installs" target="_blank"> Office Portal</a> and install your desired applications.</span></span>

2. <span data-ttu-id="2d3a6-246">Épinglez les applications Office souhaitées à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-246">Pin desired Office applications to the taskbar.</span></span>

3. <span data-ttu-id="2d3a6-247">Si Outlook est installé, assurez-vous de définir l’OST Outlook de sorte qu’il enregistre uniquement le cache des deux dernières semaines.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-247">If Outlook is installed, be sure to set the Outlook OST to only save last two weeks cache.</span></span> <span data-ttu-id="2d3a6-248">Cela permet de réduire considérablement l’utilisation du disque et le temps d’installation.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-248">This will vastly reduce disk usage and setup time.</span></span>

    - <span data-ttu-id="2d3a6-249">Sélectionnez \*\*\*\*  >  **Paramètres du compte de fichier** et sélectionnez votre compte.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-249">Select **File** > **Account Settings** and select your account.</span></span>
    
    - <span data-ttu-id="2d3a6-250">Sélectionnez **Modifier** et définissez le curseur pour utiliser le **mode Exchange** mis en cache sur 14 jours.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-250">Select **Change** and set the slider for **Use Cached Exchange Mode** to 14 days.</span></span>

### <a name="microsoft-teams"></a><span data-ttu-id="2d3a6-251">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2d3a6-251">Microsoft Teams</span></span>

1. <span data-ttu-id="2d3a6-252">Téléchargez et installez <a href="https://teams.microsoft.com/downloads" target="_blank"> Microsoft </a> Teams.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-252">Download and install <a href="https://teams.microsoft.com/downloads" target="_blank"> Microsoft Teams </a>.</span></span>

2. <span data-ttu-id="2d3a6-253">Configurer les paramètres de l’application de démarrage automatique (facultatif).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-253">Configure settings to Auto-start application (optional).</span></span>

3. <span data-ttu-id="2d3a6-254">Épinglez Teams à la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-254">Pin Teams to the taskbar.</span></span>

4. <span data-ttu-id="2d3a6-255">Envisagez de réduire les notifications Teams sur l’appareil pour éviter les distractions (facultatif).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-255">Consider reducing Teams notifications on the device to avoid distractions (optional).</span></span>

   ![Notifications Teams](images/teams.png)

### <a name="connect-app"></a><span data-ttu-id="2d3a6-257">Application de connexion</span><span class="sxs-lookup"><span data-stu-id="2d3a6-257">Connect app</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d3a6-258">Dans Windows 10, version 2004 et ultérieure, l’application Se connecter pour la projection sans fil à l’aide de Miracast n’est pas installée par défaut, mais elle est disponible en tant que fonctionnalité facultative.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-258">In Windows 10, version 2004 and later, the Connect app for wireless projection using Miracast is not installed by default, but is available as an optional feature.</span></span> <span data-ttu-id="2d3a6-259">Si vous avez installé (ou mis à jour vers) Windows version 2004 ou ultérieure, vous pouvez voir les informations suivantes sur l’écran Projeter sur ce PC dans les paramètres :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-259">If you have installed (or updated to) Windows version 2004 or later, you may see the following on the Projecting to this PC screen in settings:</span></span>

![Projeter sur ce PC](images/sh2-project.png) 


1. <span data-ttu-id="2d3a6-261">Pour installer l’application à partir de la page de paramètres « Projecting to this PC », sélectionnez **Fonctionnalités**facultatives Ajouter une fonctionnalité, puis installez l’application  >  \*\*\*\* **Affichage** sans fil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-261">To install the app from the “Projecting to this PC” settings page, select **Optional features** > **Add a feature** and then install the **Wireless Display** app.</span></span>

2. <span data-ttu-id="2d3a6-262">Sous certains appareils Windows et Android, vous pouvez projeter sur ce PC lorsque vous dites que **c’est OK,** choisissez :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-262">Under **Some Windows and Android devices can project to this PC when you say it's OK**, choose:</span></span>

    - <span data-ttu-id="2d3a6-263">**Disponible partout si** l’appareil ne se trouve pas sur un réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-263">**Available everywhere** if the device is not on a corporate network.</span></span>
    - <span data-ttu-id="2d3a6-264">Dans le cas contraire, choisissez **Disponible partout sur les réseaux sécurisés.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-264">Otherwise, choose **Available everywhere on secure networks**.</span></span>
    
3. <span data-ttu-id="2d3a6-265">Under **Ask to project to this PC**, choose First time **only**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-265">Under **Ask to project to this PC**, choose **First time only**.</span></span>

4. <span data-ttu-id="2d3a6-266">Under **Require PIN for pairing**, choose **Never**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-266">Under **Require PIN for pairing**, choose **Never**.</span></span>

5. <span data-ttu-id="2d3a6-267">Pour lancer l’application et l’épingler à la barre des tâches, recherchez **Connect**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-267">To then launch the app and pin it to the taskbar, search for **Connect**.</span></span>

6. <span data-ttu-id="2d3a6-268">Ouvrez l’application.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-268">Open the app.</span></span> <span data-ttu-id="2d3a6-269">Lorsque l’application est ouverte, cliquez avec le bouton droit sur l’icône Connecter l’application dans la barre des tâches, puis sélectionnez épingler **à la barre des tâches.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-269">While the app is open, right-click on the Connect app icon on the taskbar, and select **pin to taskbar**.</span></span>

7. <span data-ttu-id="2d3a6-270">Fermez ensuite l’application Se connecter.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-270">Then close the Connect app.</span></span> <span data-ttu-id="2d3a6-271">**Project to this PC** might not work unless the app has been run at least once.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-271">**Project to this PC** might not work unless the app has been run at least once.</span></span>

<span data-ttu-id="2d3a6-272">Configuration recommandée lorsqu’elle n’est pas sur le réseau d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-272">Recommended configuration when not on the corporate network:</span></span>

![Paramètres à la maison](images/project1.png)

<span data-ttu-id="2d3a6-274">Configuration recommandée sur le réseau d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-274">Recommended configuration on the corporate network:</span></span>

![Paramètres au travail](images/project2.png)

### <a name="your-phone"></a><span data-ttu-id="2d3a6-276">Votre Téléphone</span><span class="sxs-lookup"><span data-stu-id="2d3a6-276">Your Phone</span></span>

<span data-ttu-id="2d3a6-277">**L’application** Votre téléphone est installée par défaut sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-277">The **Your Phone** app is installed by default on Windows 10.</span></span> <span data-ttu-id="2d3a6-278">S’il n’est pas présent, vous pouvez également l’installer à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-278">If it is not present, you can also install it from the Windows Store.</span></span>

<span data-ttu-id="2d3a6-279">Pour plus d’informations sur la configuration de l’application, voir Comment configurer votre téléphone sur Windows 10 et synchroniser les données <a href="https://www.windowscentral.com/how-set-your-phone-windows-10" target="_blank"> entre votre PC et votre téléphone </a> .</span><span class="sxs-lookup"><span data-stu-id="2d3a6-279">For information about setting up the app, see <a href="https://www.windowscentral.com/how-set-your-phone-windows-10" target="_blank"> How to set up Your Phone on Windows 10 and sync data between your PC and phone</a>.</span></span> <span data-ttu-id="2d3a6-280">Découvrez également <a href="https://www.windowscentral.com/how-fix-common-problems-your-phone-app-windows-10" target="_blank"> comment résoudre les problèmes courants liés à votre application Téléphone sur Windows 10. </a></span><span class="sxs-lookup"><span data-stu-id="2d3a6-280">Also see <a href="https://www.windowscentral.com/how-fix-common-problems-your-phone-app-windows-10" target="_blank"> How to fix common problems with Your Phone app on Windows 10</a>.</span></span>

###  <a name="fancy-zones"></a><span data-ttu-id="2d3a6-281">Zones de ville</span><span class="sxs-lookup"><span data-stu-id="2d3a6-281">Fancy Zones</span></span>


<span data-ttu-id="2d3a6-282">**Les zones de** ville font partie d’un ensemble d’outils <a href="https://github.com/microsoft/PowerToys/releases" target="_blank"> appelés PowerToys </a> sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-282">**Fancy Zones** is part of a collection of tools called <a href="https://github.com/microsoft/PowerToys/releases" target="_blank"> PowerToys</a> on GitHub..</span></span> <span data-ttu-id="2d3a6-283">Il s’agit d’un excellent moyen d’utiliser l’espace de l’écran sur un Surface Hub 2 en vous donnant la possibilité de définir des dispositions fixes sur votre écran (« zones ») et de sélectionner l’application qui s’exécutera ensuite dans chaque zone.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-283">It is a great way to utilize the screen real-estate on a Surface Hub 2 by giving you the ability to define fixed layouts on your display (“zones”), and then select which app will then run in each zone.</span></span> 


<span data-ttu-id="2d3a6-284">Le [wiki PowerToys](https://github.com/microsoft/PowerToys/wiki) dispose d’instructions sur l’utilisation et la personnalisation de chaque outil, y compris [FancyZones](https://github.com/microsoft/PowerToys/wiki/FancyZones-Overview).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-284">The [PowerToys wiki](https://github.com/microsoft/PowerToys/wiki) has instructions for how to use and customize each tool, including [FancyZones](https://github.com/microsoft/PowerToys/wiki/FancyZones-Overview).</span></span> <span data-ttu-id="2d3a6-285">À un niveau élevé : après avoir installé PowerToys, vous pouvez sélectionner ou créer une disposition personnalisée, puis maintenir la touche de déplacement vers le bas et faire glisser ou utiliser des touches de clavier pour déplacer une application en cours d’exécution dans des zones spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-285">At a high level – after installing PowerToys, you can select or create a custom layout, and then hold the shift key down and drag or use keyboard keys to move a running app into specific zones.</span></span> <span data-ttu-id="2d3a6-286">L’utilisation d Bluetooth clavier et d’une souris USB vous aidera, ou vous pouvez utiliser le clavier tactile à l’écran et le pavé tactile.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-286">Using a Bluetooth or USB keyboard and mouse will help with this, or you can use the on-screen touch keyboard and touchpad.</span></span>

**<span data-ttu-id="2d3a6-287">Conseils power toys</span><span class="sxs-lookup"><span data-stu-id="2d3a6-287">Power toys tips</span></span>**
- <span data-ttu-id="2d3a6-288">Pour recevoir des notifications par courrier électronique des mises à jour de publication powerToys sur GitHub, cliquez sur le bouton « Inscription » en haut de la [page.](https://github.com/microsoft/PowerToys/releases)</span><span class="sxs-lookup"><span data-stu-id="2d3a6-288">To receive email notifications of PowerToys release updates on GitHub, click the “sign-up” button at the top of the [page](https://github.com/microsoft/PowerToys/releases).</span></span>
- <span data-ttu-id="2d3a6-289">Une fois PowerToys installé, vous pouvez recevoir des notifications Windows et/ou télécharger et installer les dernières mises à jour en configurant les **paramètres** PowerToys Télécharger automatiquement les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-289">Once PowerToys is installed, you can receive Windows notifications and/or download and install the latest updates by configuring the PowerToys settings **Download updates automatically** to on.</span></span>
- <span data-ttu-id="2d3a6-290">Pour obtenir les paramètres PowerToys, sélectionnez la **carat** haut exécutant les applications dans la barre des tâches, puis cliquez avec le bouton droit ou appuyez sur l’icône PowerToys jusqu’à ce que le menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-290">To get to the PowerToys settings, select the up carat **Running apps** on the taskbar, and then right click or press and hold the PowerToys icon until the menu appears.</span></span> <span data-ttu-id="2d3a6-291">Sélectionnez « Paramètres ».</span><span class="sxs-lookup"><span data-stu-id="2d3a6-291">Select “Settings”.</span></span>
- <span data-ttu-id="2d3a6-292">En bas de la page des paramètres PowerToys, activer automatiquement le téléchargement **des** mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-292">At the bottom of the PowerToys settings page, turn **Download updates automatically** to on.</span></span>
- <span data-ttu-id="2d3a6-293">Lorsqu’une mise à jour a été publiée, une notification Windows s’affiche, vous donnant la possibilité de savoir quand installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-293">When an update has been released, a Windows notification will appear giving you the option of when to install the update.</span></span>


### <a name="edge-chromium-browser"></a><span data-ttu-id="2d3a6-294">Navigateur Edge Chromium</span><span class="sxs-lookup"><span data-stu-id="2d3a6-294">Edge Chromium browser</span></span>

<span data-ttu-id="2d3a6-295">Téléchargez et installez le nouveau <a href="https://www.microsoft.com/en-us/edge?form=MY01BL&OCID=MY01BL" target="_blank"> navigateur Edge Chromium. </a></span><span class="sxs-lookup"><span data-stu-id="2d3a6-295">Download and install the new <a href="https://www.microsoft.com/en-us/edge?form=MY01BL&OCID=MY01BL" target="_blank">Edge Chromium browser</a>.</span></span>


### <a name="surface-hub-hardware-diagnostic-tool"></a><span data-ttu-id="2d3a6-296">Outil de diagnostic du matériel Du Surface Hub</span><span class="sxs-lookup"><span data-stu-id="2d3a6-296">Surface Hub Hardware Diagnostic tool</span></span>

<span data-ttu-id="2d3a6-297">L’outil de diagnostic du matériel Surface <a href="https://www.microsoft.com/p/surface-hub-hardware-diagnostic/9nblggh51f2g" target="_blank"> Hub </a> disponible gratuitement à partir du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-297">The <a href="https://www.microsoft.com/p/surface-hub-hardware-diagnostic/9nblggh51f2g" target="_blank"> Surface Hub Hardware Diagnostic tool</a> available for free from the Microsoft Store.</span></span> <span data-ttu-id="2d3a6-298">L’outil est conçu pour vous aider à vous assurer que votre Surface Hub s’exécute au mieux.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-298">The tool is designed to help you make sure your Surface Hub is performing at its best.</span></span> <span data-ttu-id="2d3a6-299">Il contient des tests pour déterminer si votre microprogramme est à jour et configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-299">It contains tests to determine if your firmware is up to date and configured correctly.</span></span> <span data-ttu-id="2d3a6-300">Les tests interactifs vous permettent de confirmer que les fonctionnalités essentielles fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-300">Interactive tests allow you to confirm essential functionality is working as expected.</span></span> <span data-ttu-id="2d3a6-301">Si des problèmes surviennent, les résultats peuvent être enregistrés et partagés avec l’équipe du Support Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-301">If problems are encountered, results can be saved and shared with the Surface Hub Support Team.</span></span> <span data-ttu-id="2d3a6-302">Cliquez sur le lien pour l’installer à partir du Microsoft Store, puis épinglez l’application à votre barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-302">Click on the link to install it from the Microsoft Store, and then pin the application to your taskbar.</span></span>

## <a name="additional-settings"></a><span data-ttu-id="2d3a6-303">Paramètres supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2d3a6-303">Additional settings</span></span>

### <a name="pen-tail-select-to-launch-whiteboard"></a><span data-ttu-id="2d3a6-304">Stylet tail select to launch Whiteboard</span><span class="sxs-lookup"><span data-stu-id="2d3a6-304">Pen tail select to launch Whiteboard</span></span>

1. <span data-ttu-id="2d3a6-305">Recherchez **stylet** et **sélectionnez Stylet & paramètres Windows Ink.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-305">Search for **Pen** and select **Pen & Windows Ink settings**.</span></span>

2. <span data-ttu-id="2d3a6-306">Dans la partie inférieure de la page, sous les **raccourcis stylet,** définissez **Sélectionner** une fois sur **Tableau blanc Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-306">Near the bottom of the page, under **Pen shortcuts** set **Select once** to **Microsoft Whiteboard**.</span></span> 

### <a name="power-management"></a><span data-ttu-id="2d3a6-307">Gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="2d3a6-307">Power management</span></span>

<span data-ttu-id="2d3a6-308">Plusieurs paramètres d’alimentation sont disponibles pour obtenir la meilleure expérience possible à l’aide de Windows 10 Professionnel ou Entreprise sur Surface Hub 2.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-308">There are several power settings available to get the best experience using Windows 10 Pro or Enterprise on Surface Hub 2.</span></span> <span data-ttu-id="2d3a6-309">Cela inclut les délai d’affichage d’écran et de pc et la façon dont ils interagissent avec la détection de présence humaine intégrée (Doppler), l’économiseur d’écran et la protection par mot de passe, puis, le cas échéant, comment passer les paramètres d’alimentation de stratégie de groupe destinés aux utilisateurs d’ordinateurs portables/de bureau.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-309">This includes screen and pc timeouts and how they interact with the built-in human presence detection (Doppler), the screen saver and password protection, and then if appropriate how to by-pass group policy power settings intended for laptop / desktop users.</span></span>

<span data-ttu-id="2d3a6-310">Windows 10 Professionnel ou Entreprise sur Surface Hub 2 empêche l’écran de passer en veille par les actions tactiles, de souris et de clavier, ainsi que par la détection d’occupation humaine intégrée (Doppler).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-310">Windows 10 Pro or Enterprise on Surface Hub 2 keeps the screen from going to sleep by touch, mouse, and keyboard actions, as well as the built-in human occupancy detection (Doppler).</span></span> <span data-ttu-id="2d3a6-311">La détection de l’occupation humaine est activée par défaut, mais si vous le souhaitez, elle peut être désactivée dans UEFI en basculeant l’option d’appareil dans l’outil De configuration UEFI Surface dans le cadre de la migration initiale ou en construisant et en appliquant un package de configuration UEFI ultérieur.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-311">Human occupancy detection is enabled by default, but if desired it can be disabled in UEFI by toggling the device option in the Surface UEFI Configurator tool either as part of the initial migration, or by building and applying a later UEFI configuration package.</span></span> 

**<span data-ttu-id="2d3a6-312">Gestion de l’alimentation : paramètres de veille d’écran et de PC</span><span class="sxs-lookup"><span data-stu-id="2d3a6-312">Power Management: Screen and PC sleep settings</span></span>**

1. <span data-ttu-id="2d3a6-313">Sélectionnez **Démarrer**  >  **l’alimentation**  >  **système**  >  **des paramètres & veille.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-313">Select **Start** > **Settings** > **System** > **Power & sleep**.</span></span>

2. <span data-ttu-id="2d3a6-314">Définissez le curseur en mode d’alimentation **sur Les meilleures performances.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-314">Set the power mode slider to **Best performance**.</span></span>

3. <span data-ttu-id="2d3a6-315">Configurez les valeurs d’écran et de veille selon vos préférences, tout en maintenant compte de la détection de présence Doppler qui s’affiche lorsque des mouvements sont détectés.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-315">Configure screen and sleep values to your preference while also accounting for Doppler presence detection that wakes up the device when movement is detected.</span></span> <span data-ttu-id="2d3a6-316">Par conséquent, il est recommandé de définir Screen to **Turn off after 2 hours** et le PC à Turn off après **4 heures.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-316">Accordingly, as a best practice, it's recommended to set Screen to **Turn off after 2 hours** and the PC to **Turn off after 4 hours.**</span></span>

**<span data-ttu-id="2d3a6-317">Gestion de l’alimentation : économiseur d’écran</span><span class="sxs-lookup"><span data-stu-id="2d3a6-317">Power Management: Screen saver</span></span>**

1. <span data-ttu-id="2d3a6-318">Recherchez les **paramètres de l’écran de** verrouillage et ouvrez **l’écran de verrouillage.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-318">Search for **Lock Screen** and open **Lock screen settings**.</span></span>

2. <span data-ttu-id="2d3a6-319">Configurez les **paramètres de délai d’affichage de** l’écran et de l’économiseur **d’écran** à votre préférence.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-319">Configure **Screen timeout settings** and **Screen saver settings** to your preference.</span></span> <span data-ttu-id="2d3a6-320">Les valeurs par défaut recommandées sont les :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-320">Recommended default values are:</span></span>

   - <span data-ttu-id="2d3a6-321">Économiseur d’écran dans (Aucun) ou un économiseur d’écran de votre choix.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-321">Screen saver to (None) or a screen saver of your choice.</span></span>
   - <span data-ttu-id="2d3a6-322">Délai d’attente de 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-322">Wait time to 15 minutes.</span></span>
   - <span data-ttu-id="2d3a6-323">À la reprise, affichez l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-323">On resume, display logon screen.</span></span>


**<span data-ttu-id="2d3a6-324">Gestion de l’alimentation : stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2d3a6-324">Power Management: Group Policy</span></span>**

<span data-ttu-id="2d3a6-325">Avant d’effectuer la procédure suivante, consultez votre service informatique pour obtenir votre approbation afin d’exclure un appareil Surface Hub 2S de la stratégie globale de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-325">Before performing the following procedure, check with your IT department for approval to exclude a Surface Hub 2S device from global power management policy.</span></span> <span data-ttu-id="2d3a6-326">Certains paramètres de gestion de l’alimentation peuvent désactiver la fonction de détection de présence.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-326">Some power management settings can disable the presence detection function.</span></span>

1. <span data-ttu-id="2d3a6-327">Recherchez **le Centre logiciel et** ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-327">Search for **Software Center** and open it.</span></span>

2. <span data-ttu-id="2d3a6-328">Sélectionnez **options.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-328">Select **Options**.</span></span>

3. <span data-ttu-id="2d3a6-329">Développez la **gestion de l’alimentation** et sélectionnez Ne pas appliquer les **paramètres d’alimentation de mon service informatique à cet ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-329">Expand the **Power management**  and select **Do not apply power settings from my IT department to this computer**.</span></span>

   ![Paramètres logiciels](images/soft-cntr.png)

### <a name="storage-sense"></a><span data-ttu-id="2d3a6-331">Assistant Stockage</span><span class="sxs-lookup"><span data-stu-id="2d3a6-331">Storage Sense</span></span>

<span data-ttu-id="2d3a6-332">Le Surface Hub 2 dispose d’un SSD de 128 Go pour le stockage local. Il est donc nécessaire d’envisager l’utilisation de mesures d’enregistrement de stockage lors d’une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-332">The Surface Hub 2 has a 128GB SSD for local storage, so it is necessary to consider the use of storage saving measures during normal usage.</span></span>  <span data-ttu-id="2d3a6-333">Pour configurer l’Sens du stockage :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-333">To configure Storage Sense:</span></span>

1.  <span data-ttu-id="2d3a6-334">Recherchez **les paramètres de stockage,** qui se trouvent sous **Paramètres système.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-334">Search for **storage settings**, which is found under **System settings**.</span></span>

2.  <span data-ttu-id="2d3a6-335">Sous **Paramètres,** **sélectionnez Activer le sens du stockage** pour ouvrir la page **Paramètres** de stockage.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-335">Under **Settings**, select **Turn on storage sense** to open the **Storage** settings page.</span></span>

3.  <span data-ttu-id="2d3a6-336">Activer l’Sense de **stockage.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-336">Turn Storage Sense to **On**.</span></span>

4.  <span data-ttu-id="2d3a6-337">Sélectionnez **Configurer l’Sens** du stockage ou exécutez-le maintenant et configurez les paramètres pour conserver les fichiers en ligne autant que possible (en raison de l’espace disque limité).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-337">Select **Configure Storage Sense or run it now** and configure settings to keep files online as much as possible (due to limited drive space).</span></span>

<span data-ttu-id="2d3a6-338">Paramètres recommandés :</span><span class="sxs-lookup"><span data-stu-id="2d3a6-338">Recommended settings:</span></span>

- <span data-ttu-id="2d3a6-339">Exécuter l’Sens du stockage = Tous les jours.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-339">Run Storage Sense = Every Day.</span></span>
- <span data-ttu-id="2d3a6-340">Supprimer les fichiers temporaires que mes applications n’utilisent pas = Tous les 14 jours (au moins).</span><span class="sxs-lookup"><span data-stu-id="2d3a6-340">Delete temporary files that my apps aren't using = Every 14 days (at least).</span></span>
- <span data-ttu-id="2d3a6-341">Supprimez des fichiers dans mon dossier Téléchargements s’ils y sont depuis plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-341">Delete files in my Downloads folder if they have been there for over = 30 days.</span></span>
- <span data-ttu-id="2d3a6-342">OneDrive : le contenu devient en ligne uniquement s’il n’est pas ouvert pendant plus de = 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-342">OneDrive: Content will become online-only if not opened for more than = 30 days.</span></span>

### <a name="tablet-mode"></a><span data-ttu-id="2d3a6-343">Mode tablette</span><span class="sxs-lookup"><span data-stu-id="2d3a6-343">Tablet mode</span></span>

<span data-ttu-id="2d3a6-344">Activer le mode tablette si vous le souhaitez pour des besoins d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-344">Turn on Tablet mode if desired for accessibility needs.</span></span>


### <a name="sound-settings"></a><span data-ttu-id="2d3a6-345">Paramètres sonores</span><span class="sxs-lookup"><span data-stu-id="2d3a6-345">Sound settings</span></span>

1. <span data-ttu-id="2d3a6-346">Recherchez **les paramètres sons et** ouvrez cette page.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-346">Search for **Sounds settings** and open this page.</span></span>

2. <span data-ttu-id="2d3a6-347">Sélectionnez **panneau de contrôle sonore** sur la droite et sélectionnez **l’onglet Sons.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-347">Select **Sound Control Panel** on the right and select the **Sounds** tab.</span></span>

3. <span data-ttu-id="2d3a6-348">Sous **Les événements de programme** **définissent Device Connect** et Device **Disconnect** sur **None**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-348">Under **Program Events** set **Device Connect** and **Device Disconnect** to **None**.</span></span>

### <a name="silence-notifications"></a><span data-ttu-id="2d3a6-349">Notifications de silence</span><span class="sxs-lookup"><span data-stu-id="2d3a6-349">Silence notifications</span></span>

1. <span data-ttu-id="2d3a6-350">Recherchez **l’assistance focus** et ouvrez cette page.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-350">Search for **Focus assist** and open this page.</span></span>

2. <span data-ttu-id="2d3a6-351">Sélectionnez **Alarmes uniquement.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-351">Select **Alarms Only**.</span></span> <span data-ttu-id="2d3a6-352">Cela permet d’éviter les volants de notification constants.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-352">This will avoid constant notification flyouts.</span></span>

### <a name="disk-cleanup"></a><span data-ttu-id="2d3a6-353">Nettoyage de disque</span><span class="sxs-lookup"><span data-stu-id="2d3a6-353">Disk Cleanup</span></span>

1. <span data-ttu-id="2d3a6-354">Recherchez **nettoyage de disque et** ouvrez cette application.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-354">Search for **Disk Cleanup** and open this app.</span></span>

2. <span data-ttu-id="2d3a6-355">Sous **Fichiers à supprimer,** sélectionnez les fichiers à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-355">Under **Files to delete**, select the files you wish to delete.</span></span> 

3. <span data-ttu-id="2d3a6-356">Sélectionnez également **Nettoyer les fichiers système.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-356">Also select **Clean up system files**.</span></span>

## <a name="complete-and-verify"></a><span data-ttu-id="2d3a6-357">Terminer et vérifier</span><span class="sxs-lookup"><span data-stu-id="2d3a6-357">Complete and verify</span></span>

1. <span data-ttu-id="2d3a6-358">Recherchez et installez toutes les mises à jour Windows.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-358">Scan for and install all Windows Updates.</span></span>

2. <span data-ttu-id="2d3a6-359">Mettre à jour la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-359">Update Group Policy.</span></span>

   1. <span data-ttu-id="2d3a6-360">À une invite de commandes avec élévation de niveau élevé, entrez **gpupdate /force /boot /wait:0**.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-360">At an elevated command prompt, enter **gpupdate /force /boot /wait:0**.</span></span>
   
3. <span data-ttu-id="2d3a6-361">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-361">Restart the device.</span></span>

4. <span data-ttu-id="2d3a6-362">Vérifiez les applications de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-362">Verify taskbar apps.</span></span>

   - <span data-ttu-id="2d3a6-363">Se connecter à l’application</span><span class="sxs-lookup"><span data-stu-id="2d3a6-363">Connect App</span></span>
   - <span data-ttu-id="2d3a6-364">Icône Verrouiller</span><span class="sxs-lookup"><span data-stu-id="2d3a6-364">Lock Icon</span></span>
   - <span data-ttu-id="2d3a6-365">Capture d'écran et Croquis</span><span class="sxs-lookup"><span data-stu-id="2d3a6-365">Snip & Sketch</span></span>
   - <span data-ttu-id="2d3a6-366">Teams (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="2d3a6-366">Teams (if applicable)</span></span>
   - <span data-ttu-id="2d3a6-367">Applications Office (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="2d3a6-367">Office Apps (if applicable)</span></span>
   - <span data-ttu-id="2d3a6-368">Application Surface</span><span class="sxs-lookup"><span data-stu-id="2d3a6-368">Surface App</span></span>
   - <span data-ttu-id="2d3a6-369">Tableau blanc</span><span class="sxs-lookup"><span data-stu-id="2d3a6-369">Whiteboard</span></span>
    
5. <span data-ttu-id="2d3a6-370">Vérifier la détection de présence.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-370">Verify presence detection.</span></span>

   - <span data-ttu-id="2d3a6-371">La détection de présence sera une icône verte dans le bac du système.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-371">Presence detection will be a green icon in the system tray.</span></span>
    
6. <span data-ttu-id="2d3a6-372">Vérifiez que la projecting sur ce PC est activée avec l’application Connect.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-372">Verify projecting to this PC is enabled with the Connect App.</span></span> <span data-ttu-id="2d3a6-373">Après avoir configuré  **Project sur les paramètres** de ce PC, exécutez l’application Se connecter au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-373">After configuring  **Project to this PC** settings, run the Connect App at least once.</span></span> <span data-ttu-id="2d3a6-374">(Par la suite, l’application De connexion n’a pas besoin d’être en cours d’exécution pour projeter sur le Surface Hub.)</span><span class="sxs-lookup"><span data-stu-id="2d3a6-374">(Subsequently, the Connect App does not need to be running in order to project to Surface Hub.)</span></span>

7. <span data-ttu-id="2d3a6-375">Vérifiez les paramètres d’alimentation et de veille.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-375">Verify power and sleep settings.</span></span>

    - <span data-ttu-id="2d3a6-376">Économiseur d’écran : 15 minutes, définie sur (aucun), Mystify ou Blank ; vérifiez que la case à cocher nécessitant un mot de passe est cocher.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-376">Screen Saver: 15 minutes, set to (none), Mystify or Blank; ensure the check box for requiring password is selected.</span></span>
    - <span data-ttu-id="2d3a6-377">Écran : **désactiver après 2 heures.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-377">Screen: **Turn off after 2 hours**.</span></span>
    - <span data-ttu-id="2d3a6-378">PC : **désactiver après 4 heures.**</span><span class="sxs-lookup"><span data-stu-id="2d3a6-378">PC:  **Turn off after 4 hours**.</span></span>
    
8. <span data-ttu-id="2d3a6-379">Vérifiez que Windows Hello fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-379">Verify Windows Hello is working.</span></span>

9. <span data-ttu-id="2d3a6-380">Vérifiez que la synchronisation de vos paramètres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-380">Verify sync your settings is disabled.</span></span>

10. <span data-ttu-id="2d3a6-381">Vérifiez les applications de démarrage.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-381">Verify startup apps.</span></span>

> [!TIP]
> <span data-ttu-id="2d3a6-382">Après avoir installé et configuré Windows 10, le Surface Hub 2S peut être géré comme n’importe quel autre appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d3a6-382">After installing and configuring Windows 10, the Surface Hub 2S can be managed just like any other Windows 10 device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d3a6-383">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="2d3a6-383">Related topics</span></span>

<a href="surface-hub-2s-migrate-os.md" target="_blank"> <span data-ttu-id="2d3a6-384">Migrer vers Windows10 Professionnel ou Entreprise sur Surface Hub2</span><span class="sxs-lookup"><span data-stu-id="2d3a6-384">Migrate to Windows 10 Pro or Enterprise on Surface Hub 2</span></span></a>
