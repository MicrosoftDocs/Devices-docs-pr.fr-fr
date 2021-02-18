---
title: Réinitialisation et récupération pour Surface Hub 2S
description: Découvrez comment récupérer et réinitialiser surface Hub 2S.
keywords: séparer les valeurs par des virgules
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 12/05/2019
ms.localizationpriority: Medium
ms.openlocfilehash: 64ceee291d3d3e067f581707d9431fa92398c785
ms.sourcegitcommit: ecb4909c091e69b7bdb1faacfc8c34b480dc884b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11342974"
---
# <span data-ttu-id="1fdbe-104">Réinitialisation et récupération pour Surface Hub 2S</span><span class="sxs-lookup"><span data-stu-id="1fdbe-104">Reset and recovery for Surface Hub 2S</span></span>

<span data-ttu-id="1fdbe-105">Si vous rencontrez des problèmes avec Surface Hub 2S, vous pouvez rétablir les paramètres d’usine ou restaurer l’appareil à l’aide d’un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-105">If you encounter problems with Surface Hub 2S, you can reset the device to factory settings or restore by using a USB drive.</span></span>

<span data-ttu-id="1fdbe-106">Pour commencer, connectez-vous au Surface Hub 2S avec les informations d’identification d’administrateur, ouvrez l’application **Paramètres,** sélectionnez Mettre à jour & **sécurité,** puis sélectionnez **Récupération.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-106">To begin, sign in to Surface Hub 2S with admin credentials, open the **Settings** app, select **Update & security**, and then select **Recovery**.</span></span>

## <span data-ttu-id="1fdbe-107">Réinitialisez l’appareil</span><span class="sxs-lookup"><span data-stu-id="1fdbe-107">Reset the device</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="1fdbe-108">Assurez-vous que votre clé BitLocker est disponible avant de réinitialiser l’appareil, car vous y serez invité ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-108">Ensure that you have your BitLocker key available before resetting the device, as you will be prompted for it later.</span></span> <span data-ttu-id="1fdbe-109">Pour plus d’informations, voir [Enregistrer votre clé BitLocker.](save-bitlocker-key-surface-hub.md)</span><span class="sxs-lookup"><span data-stu-id="1fdbe-109">To learn more, see [Save your BitLocker key](save-bitlocker-key-surface-hub.md).</span></span>

1. <span data-ttu-id="1fdbe-110">Pour réinitialiser l’appareil, **sélectionnez Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-110">To reset the device, select **Get Started**.</span></span>

2. <span data-ttu-id="1fdbe-111">Lorsque la fenêtre **Prêt à réinitialiser cet appareil** s’affiche, sélectionnez **Réinitialiser.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-111">When the **Ready to reset this device** window appears, select **Reset**.</span></span> 
  
   > [!IMPORTANT]
   > <span data-ttu-id="1fdbe-112">Lorsque le Hub redémarre sur la partition de récupération, il vous invite à entrer la clé BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-112">When the Hub reboots to the recovery partition, it will prompt you to enter the BitLocker key.</span></span> <span data-ttu-id="1fdbe-113">Ignorer cette invite entraîne l’échec de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-113">Skipping that prompt will cause reset to fail.</span></span> <span data-ttu-id="1fdbe-114">Une fois que vous avez entré la clé BitLocker, le Hub réinstalle le système d’exploitation à partir de la partition de récupération.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-114">Once you enter the BitLocker key the Hub reinstalls the operating system from the recovery partition.</span></span> <span data-ttu-id="1fdbe-115">Cela peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-115">This may take up to one hour to complete.</span></span>
  
3. <span data-ttu-id="1fdbe-116">Pour reconfigurer l’appareil, exécutez le programme d’installation pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-116">To reconfigure the device, run the first-time Setup program.</span></span>

4. <span data-ttu-id="1fdbe-117">Si vous gérez l’appareil à l’aide de Microsoft Intune ou d’une autre solution de gestion des appareils mobiles, retirez et supprimez l’enregistrement précédent, puis ré-inscrivez le nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-117">If you manage the device using Microsoft Intune or another mobile device management solution, retire and delete the previous record, and then re-enroll the new device.</span></span> <span data-ttu-id="1fdbe-118">Pour plus d’informations, voir Supprimer des appareils à l’aide de l’effacement, de la suppression ou de la [désinscrire manuellement de l’appareil.](https://docs.microsoft.com/intune/devices-wipe)</span><span class="sxs-lookup"><span data-stu-id="1fdbe-118">For more information, see [Remove devices by using wipe, retire, or manually unenrolling the device](https://docs.microsoft.com/intune/devices-wipe).</span></span>

   > [!div class="mx-imgBorder"]
   > ![*Réinitialiser et récupérer pour Surface Hub 2S*](images/sh2-reset.png)
   <br/>*<span data-ttu-id="1fdbe-120">Figure1.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-120">Figure 1.</span></span> <span data-ttu-id="1fdbe-121">Réinitialisation et récupération pour Surface Hub 2S</span><span class="sxs-lookup"><span data-stu-id="1fdbe-121">Reset and recovery for Surface Hub 2S</span></span>* 

## <span data-ttu-id="1fdbe-122">Récupérer le Surface Hub 2S à l’aide d’un lecteur de récupération USB</span><span class="sxs-lookup"><span data-stu-id="1fdbe-122">Recover Surface Hub 2S by using a USB recovery drive</span></span>

<span data-ttu-id="1fdbe-123">Nouveauté du Surface Hub 2S, vous pouvez désormais réinstaller l’appareil à l’aide d’une image de récupération.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-123">New in Surface Hub 2S, you can now reinstall the device by using a recovery image.</span></span>

### <span data-ttu-id="1fdbe-124">Récupération à partir d’un lecteur USB</span><span class="sxs-lookup"><span data-stu-id="1fdbe-124">Recovery from a USB drive</span></span>

<span data-ttu-id="1fdbe-125">À l’aide du Surface Hub 2S, vous pouvez réinstaller l’appareil à l’aide d’une image de récupération.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-125">Using Surface Hub 2S, you can reinstall the device by using a recovery image.</span></span> <span data-ttu-id="1fdbe-126">En faisant cela, vous pouvez réinstaller l’appareil aux paramètres d’usine si vous avez perdu la clé BitLocker ou si vous n’avez plus d’informations d’identification d’administrateur pour l’application Paramètres.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-126">By doing this, you can reinstall the device to the factory settings if you lost the BitLocker key, or if you no longer have admin credentials to the Settings app.</span></span>

>[!NOTE]
><span data-ttu-id="1fdbe-127">Utilisez un lecteur USB 3.0 avec 8 Go ou 16 Go de stockage, au format FAT32.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-127">Use a USB 3.0 drive with 8 GB or 16 GB of storage, formatted as FAT32.</span></span>

1. <span data-ttu-id="1fdbe-128">À partir d’un PC distinct, téléchargez l’image de récupération de fichier .zip à partir du site web [Surface Recovery,](https://support.microsoft.com/surfacerecoveryimage?devicetype=surfacehub2s) puis revenir à ces instructions.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-128">From a separate PC, download the .zip file recovery image from the [Surface Recovery website](https://support.microsoft.com/surfacerecoveryimage?devicetype=surfacehub2s) and then return to these instructions.</span></span> 

1. <span data-ttu-id="1fdbe-129">Dans la zone de recherche de la barre \*\*\*\* des tâches, entrez le lecteur de **récupération,** puis sélectionnez Créer un lecteur de récupération ou un lecteur de récupération **dans** les résultats.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-129">In the search box on the taskbar, enter **recovery drive**, and then select **Create a recovery drive** or **Recovery Drive** from the results.</span></span> <span data-ttu-id="1fdbe-130">Vous devrez peut-être entrer un mot de passe d’administrateur ou confirmer votre choix.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-130">You may need to enter an admin password or confirm your choice.</span></span>

1. <span data-ttu-id="1fdbe-131">Dans la **zone Contrôle de compte d’utilisateur,** sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-131">In the **User Account Control** box, select **Yes**.</span></span>

1. <span data-ttu-id="1fdbe-132">Veillez à effacer les fichiers système **de la back up dans la** case à cocher du lecteur de récupération, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-132">Make sure to clear the **Back up system files to the recovery drive** check box and then select **Next**.</span></span>

1. <span data-ttu-id="1fdbe-133">Sélectionnez votre lecteur USB, puis **sélectionnez Suivant > Créer.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-133">Select your USB drive, and then select **Next > Create**.</span></span>  <span data-ttu-id="1fdbe-134">Certains utilitaires doivent être copiés sur le lecteur de récupération, ce qui peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-134">Some utilities need to be copied to the recovery drive, so this might take a few minutes.</span></span>

1. <span data-ttu-id="1fdbe-135">Lorsque le lecteur de récupération est prêt, sélectionnez **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-135">When the recovery drive is ready, select **Finish**.</span></span>

1. <span data-ttu-id="1fdbe-136">Double-cliquez sur le fichier .zip d’image de récupération que vous avez précédemment téléchargé pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-136">Double-click the recovery image .zip file that you previously downloaded to open it.</span></span>

1. <span data-ttu-id="1fdbe-137">Sélectionnez tous les fichiers du dossier image de récupération, copiez-les à la racine de votre lecteur USB, puis sélectionnez Choisir de remplacer les fichiers dans **la destination.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-137">Select all the files from the recovery image folder, copy them to the root of your USB drive, and then select **Choose to replace the files in the destination**.</span></span>

1. <span data-ttu-id="1fdbe-138">Une fois la copie des fichiers terminée, sélectionnez l’icône Supprimer le matériel et **éjecter** le média en toute sécurité dans la barre des tâches, puis supprimez votre lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-138">Once the files have finished copying, select the **Safely Remove Hardware and Eject Media** icon on the taskbar, and remove your USB drive.</span></span>

1. <span data-ttu-id="1fdbe-139">Connectez le lecteur USB à n’importe quel port USB-C ou USB-A sur le Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-139">Connect the USB drive to any USB-C or USB-A port on the Surface Hub 2S.</span></span>

1. <span data-ttu-id="1fdbe-140">Désactiver le Hub, puis suivre les étapes suivantes pour démarrer à partir du lecteur USB :</span><span class="sxs-lookup"><span data-stu-id="1fdbe-140">Turn off the Hub and then take these steps to boot from the USB drive:</span></span>

   1. <span data-ttu-id="1fdbe-141">Tout en appuyant sur le bouton Descendre le volume, appuyez sur le bouton d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-141">While pressing the Volume down button, press the Power button.</span></span>
   1. <span data-ttu-id="1fdbe-142">Continuez à appuyer sur les deux boutons jusqu’à ce que le logo Windows s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-142">Keep pressing both buttons until you see the Windows logo.</span></span>
   1. <span data-ttu-id="1fdbe-143">Relâchez le bouton d’alimentation, mais maintenez le bouton Descendre le volume jusqu’à ce que l’interface utilisateur d’installation commence.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-143">Release the Power button but continue to hold the Volume down button until the Install UI begins.</span></span>

      ![*Utiliser les boutons Baisser le volume et Alimentation pour lancer la récupération*](images/sh2-keypad.png)
      <br>*<span data-ttu-id="1fdbe-145">Figure2.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-145">Figure 2.</span></span> <span data-ttu-id="1fdbe-146">Boutons Volume et Alimentation</span><span class="sxs-lookup"><span data-stu-id="1fdbe-146">Volume and Power buttons</span></span>*

1. <span data-ttu-id="1fdbe-147">Dans l’écran de sélection de la langue, sélectionnez la langue d’affichage de votre Surface Hub 2S.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-147">On the language selection screen, select the display language for your Surface Hub 2S.</span></span>

1. <span data-ttu-id="1fdbe-148">Sélectionnez **Récupérer à partir d’un lecteur** et **nettoyez entièrement le lecteur,** puis sélectionnez **Récupérer.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-148">Select **Recover from a drive** and **Fully clean the drive**, and then select **Recover**.</span></span> <span data-ttu-id="1fdbe-149">Si vous êtes invité à obtenir une clé BitLocker, **sélectionnez Ignorer ce lecteur.**</span><span class="sxs-lookup"><span data-stu-id="1fdbe-149">If you're prompted for a BitLocker key, select **Skip this drive**.</span></span> <span data-ttu-id="1fdbe-150">Surface Hub 2S redémarre plusieurs fois et prend environ 30 minutes pour terminer le processus de récupération.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-150">Surface Hub 2S reboots several times and takes approximately 30 minutes to complete the recovery process.</span></span>

<span data-ttu-id="1fdbe-151">Lorsque l’écran de configuration s’affiche pour la première fois, supprimez le lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="1fdbe-151">When the first-time setup screen appears, remove the USB drive.</span></span>

## <span data-ttu-id="1fdbe-152">Contacter le support</span><span class="sxs-lookup"><span data-stu-id="1fdbe-152">Contact Support</span></span>

<span data-ttu-id="1fdbe-153">Si vous avez des questions ou avez besoin d’aide, vous pouvez [créer une demande de support.](https://support.microsoft.com/supportforbusiness/productselection)</span><span class="sxs-lookup"><span data-stu-id="1fdbe-153">If you have questions or need help, you can [create a support request](https://support.microsoft.com/supportforbusiness/productselection).</span></span>
