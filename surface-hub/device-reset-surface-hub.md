---
title: Réinitialiser ou récupérer un Surface Hub
description: Décrit les processus de réinitialisation et de récupération pour le Surface Hub et fournit des instructions.
ms.assetid: 44E82EEE-1905-464B-A758-C2A1463909FF
ms.reviewer: ''
manager: laurawi
keywords: réinitialiser le Surface Hub, récupérer
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 03/10/2021
ms.localizationpriority: medium
ms.openlocfilehash: 4b6797a83936b919aa43a7ae9fc8ae4dd720223a
ms.sourcegitcommit: f0c976664116c45605edf3d56c4f58119a246b93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "11406622"
---
# <a name="reset-or-recover-a-surface-hub"></a><span data-ttu-id="d1a32-104">Réinitialiser ou récupérer un Surface Hub</span><span class="sxs-lookup"><span data-stu-id="d1a32-104">Reset or recover a Surface Hub</span></span>

<span data-ttu-id="d1a32-105">Cet article explique comment réinitialiser ou récupérer un Microsoft Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-105">This article describes how to reset or recover a Microsoft Surface Hub.</span></span>  

<span data-ttu-id="d1a32-106">[La réinitialisation du Surface Hub](#reset-a-surface-hub) renvoie son système d’exploitation à la dernière mise à jour cumulative de Windows et supprime tous les fichiers utilisateur locaux et les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="d1a32-106">[Resetting the Surface Hub](#reset-a-surface-hub) returns its operating system to the last cumulative Windows update, and removes all local user files and configuration information.</span></span> <span data-ttu-id="d1a32-107">Les informations supprimées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1a32-107">The information that is removed includes the following:</span></span>

- <span data-ttu-id="d1a32-108">Le compte d’appareil</span><span class="sxs-lookup"><span data-stu-id="d1a32-108">The device account</span></span>
- <span data-ttu-id="d1a32-109">Informations de compte pour les administrateurs locaux de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d1a32-109">Account information for the device's local administrators</span></span>
- <span data-ttu-id="d1a32-110">Informations de joint-joint de domaine ou azure ad-join</span><span class="sxs-lookup"><span data-stu-id="d1a32-110">Domain-join or Azure AD-join information</span></span>
- <span data-ttu-id="d1a32-111">Informations d’inscription de la Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="d1a32-111">Mobile Device Management (MDM) enrollment information</span></span>
- <span data-ttu-id="d1a32-112">Informations de configuration définies à l’aide de LAM ou de l’application Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1a32-112">Configuration information that was set by using MDM or the Settings app</span></span>

<span data-ttu-id="d1a32-113">[La récupération d’un Surface Hub à partir du cloud](#recover-a-surface-hub-from-the-cloud) supprime également ces informations.</span><span class="sxs-lookup"><span data-stu-id="d1a32-113">[Recovering a Surface Hub from the cloud](#recover-a-surface-hub-from-the-cloud) also removes this information.</span></span> <span data-ttu-id="d1a32-114">En outre, le Surface Hub télécharge une nouvelle image de système d’exploitation et l’installe.</span><span class="sxs-lookup"><span data-stu-id="d1a32-114">In addition, the Surface Hub downloads a new operating system image and installs it.</span></span> <span data-ttu-id="d1a32-115">Vous pouvez spécifier si le processus de récupération conserve les autres informations stockées sur le Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-115">You can specify whether the recovery process preserves other information that is stored on the Surface Hub.</span></span> <span data-ttu-id="d1a32-116">La même image de système d’exploitation est utilisée par l’outil de récupération [Surface Hub](surface-hub-recovery-tool.md) si vous avez besoin de récupérer un Surface Hub pour lequel aucune de ces options ne peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d1a32-116">The same operating system image is used by the [Surface Hub Recovery Tool](surface-hub-recovery-tool.md) if you need to recover a Surface Hub for which neither of these options can be used.</span></span>

## <a name="reset-a-surface-hub"></a><span data-ttu-id="d1a32-117">Réinitialiser un Surface Hub</span><span class="sxs-lookup"><span data-stu-id="d1a32-117">Reset a Surface Hub</span></span>

<span data-ttu-id="d1a32-118">Vous de devez peut-être réinitialiser votre Surface Hub pour des raisons telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1a32-118">You may have to reset your Surface Hub for reasons such as the following:</span></span>

- <span data-ttu-id="d1a32-119">Vous redéfinissez l’appareil pour un nouvel espace de réunion et souhaitez le reconfigurer.</span><span class="sxs-lookup"><span data-stu-id="d1a32-119">You are re-purposing the device for a new meeting space and want to reconfigure it.</span></span>
- <span data-ttu-id="d1a32-120">Vous souhaitez modifier la façon dont vous gérez localement l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d1a32-120">You want to change how you locally manage the device.</span></span>
- <span data-ttu-id="d1a32-121">Le nom d’utilisateur ou le mot de passe du compte d’appareil ou du compte Administrateur a été perdu.</span><span class="sxs-lookup"><span data-stu-id="d1a32-121">The user name or password for the device account or the Administrator account has been lost.</span></span>
- <span data-ttu-id="d1a32-122">Une fois que vous avez installé une mise à jour, les performances de l’appareil diminuent.</span><span class="sxs-lookup"><span data-stu-id="d1a32-122">After you install an update, the performance of the device decreases.</span></span>

<span data-ttu-id="d1a32-123">Pendant le processus de réinitialisation, si un écran vide s’affiche pendant de longues périodes, veuillez patienter et ne pas prendre d’action.</span><span class="sxs-lookup"><span data-stu-id="d1a32-123">During the reset process, if you see a blank screen for long periods of time, please wait and do not take any action.</span></span>

> [!WARNING]
> <span data-ttu-id="d1a32-124">Le processus de réinitialisation de l’appareil peut prendre jusqu’à six heures.</span><span class="sxs-lookup"><span data-stu-id="d1a32-124">The device reset process may take up to six hours.</span></span> <span data-ttu-id="d1a32-125">Ne dés désactiver ni débrancher le Surface Hub tant que le processus n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="d1a32-125">Do not turn off or unplug the Surface Hub until the process has finished.</span></span> <span data-ttu-id="d1a32-126">Si vous interrompez le processus, l’appareil devient inopérable.</span><span class="sxs-lookup"><span data-stu-id="d1a32-126">If you interrupt the process, the device becomes inoperable.</span></span> <span data-ttu-id="d1a32-127">L’appareil nécessite un service de garantie pour devenir opérationnel à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d1a32-127">The device requires warranty service in order to become functional again.</span></span>

1. <span data-ttu-id="d1a32-128">Sur votre Surface Hub, ouvrez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="d1a32-128">On your Surface Hub, open **Settings**.</span></span>

   ![Image that shows Settings app for Surface Hub.](images/sh-settings.png)

2. <span data-ttu-id="d1a32-130">Sélectionnez **Mettre à jour & sécurité**.</span><span class="sxs-lookup"><span data-stu-id="d1a32-130">Select **Update & Security**.</span></span>

   ![Image that shows Update & Security group in Settings app for Surface Hub.](images/sh-settings-update-security.png)

3. <span data-ttu-id="d1a32-132">Sélectionnez **Récupération,** puis, sous **Réinitialiser l’appareil,** **sélectionnez Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="d1a32-132">Select **Recovery**, and then, under **Reset device**, select **Get started**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="d1a32-133">Assurez-vous que votre clé BitLocker est disponible avant de réinitialiser l’appareil, car vous y serez invité ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d1a32-133">Ensure that you have your BitLocker key available before resetting the device, as you will be prompted for it later.</span></span> <span data-ttu-id="d1a32-134">Pour plus d’informations, voir [Enregistrer votre clé BitLocker.](save-bitlocker-key-surface-hub.md)</span><span class="sxs-lookup"><span data-stu-id="d1a32-134">To learn more, see [Save your BitLocker key](save-bitlocker-key-surface-hub.md).</span></span> <span data-ttu-id="d1a32-135">Lorsque le Hub redémarre sur la partition de récupération, il vous invite à entrer la clé BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d1a32-135">When the Hub reboots to the recovery partition, it will prompt you to enter the BitLocker key.</span></span> <span data-ttu-id="d1a32-136">Ignorer cette invite entraîne l’échec de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="d1a32-136">Skipping that prompt will cause reset to fail.</span></span>
   
   ![Image qui illustre l’option Réinitialiser l’appareil dans l’application Paramètres du Surface Hub.](images/sh-settings-reset-device.png)

   <span data-ttu-id="d1a32-138">Une fois le processus de réinitialisation terminé, le Surface Hub redémarre le programme [de première](first-run-program-surface-hub.md) opération.</span><span class="sxs-lookup"><span data-stu-id="d1a32-138">After the reset process finishes, the Surface Hub starts the [first run program](first-run-program-surface-hub.md) again.</span></span> <span data-ttu-id="d1a32-139">Si le processus de réinitialisation rencontre un problème, il rétablit le Surface Hub à l’image du système d’exploitation existant, puis affiche l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="d1a32-139">If the reset process encounters a problem, it rolls the Surface Hub back to the previously-existing operating system image and then displays the Welcome screen.</span></span>

<span id="cloud-recovery" />

## <a name="recover-a-surface-hub-from-the-cloud"></a><span data-ttu-id="d1a32-140">Récupérer un Surface Hub à partir du cloud</span><span class="sxs-lookup"><span data-stu-id="d1a32-140">Recover a Surface Hub from the cloud</span></span>

<span data-ttu-id="d1a32-141">Si, pour une raison quelconque, le Surface Hub devient inutilisable, vous pouvez toujours le récupérer à partir du cloud sans l’aide du Support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1a32-141">If for some reason the Surface Hub becomes unusable, you can still recover it from the cloud without assistance from Microsoft Support.</span></span> <span data-ttu-id="d1a32-142">Le Surface Hub peut télécharger une nouvelle image de système d’exploitation à partir du cloud et utiliser cette image pour réinstaller son système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d1a32-142">The Surface Hub can download a fresh operating system image from the cloud, and use that image to reinstall its operating system.</span></span>

<span data-ttu-id="d1a32-143">Vous de devez peut-être utiliser ce type de processus de récupération dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1a32-143">You may have to use this type of recovery process under the following circumstances:</span></span>

- [<span data-ttu-id="d1a32-144">Le Surface Hub ou ses comptes associés sont entrés dans un état instable</span><span class="sxs-lookup"><span data-stu-id="d1a32-144">The Surface Hub or its related accounts have entered an unstable state</span></span>](#recover-a-surface-hub-in-a-bad-state)
- [<span data-ttu-id="d1a32-145">Le Surface Hub est verrouillé</span><span class="sxs-lookup"><span data-stu-id="d1a32-145">The Surface Hub is locked</span></span>](#recover-a-locked-surface-hub)

>[!IMPORTANT]
><span data-ttu-id="d1a32-146">La **récupération à partir du processus cloud** nécessite une connexion câblé qui fournit une connectivité Internet ouverte (pas de proxy ou d’autres invites d’authentification).</span><span class="sxs-lookup"><span data-stu-id="d1a32-146">The **Recover from the cloud** process requires a wired connection that provides open internet connectivity (no proxy or other authentication prompts).</span></span>

### <a name="recover-a-surface-hub-in-a-bad-state"></a><span data-ttu-id="d1a32-147">Récupérer un Surface Hub se trouvant dans un état incorrect</span><span class="sxs-lookup"><span data-stu-id="d1a32-147">Recover a Surface Hub in a bad state</span></span>

<span data-ttu-id="d1a32-148">Si le compte d’appareil passe dans un état instable ou si le compte d’administrateur rencontre des problèmes, vous pouvez utiliser l’application Paramètres pour démarrer le processus de récupération cloud.</span><span class="sxs-lookup"><span data-stu-id="d1a32-148">If the device account gets into an unstable state or if the administrator account encounters problems, you can use the Settings app to start the cloud recovery process.</span></span> <span data-ttu-id="d1a32-149">Vous devez utiliser le processus [](#reset-a-surface-hub) de récupération cloud uniquement lorsque le processus de réinitialisation de l’appareil ne corrige pas le problème.</span><span class="sxs-lookup"><span data-stu-id="d1a32-149">You should only use the cloud recovery process when the [device reset](#reset-a-surface-hub) process doesn't fix the problem.</span></span>

1. <span data-ttu-id="d1a32-150">Sur votre Surface Hub, sélectionnez Mise à jour des **paramètres** &gt; **& de** &gt; **sécurité.**</span><span class="sxs-lookup"><span data-stu-id="d1a32-150">On your Surface Hub, select **Settings** &gt; **Update & security** &gt; **Recovery**.</span></span>

2. <span data-ttu-id="d1a32-151">Sous **Récupérer à partir du cloud, sélectionnez** **Redémarrer maintenant.**</span><span class="sxs-lookup"><span data-stu-id="d1a32-151">Under **Recover from the cloud**, select **Restart now**.</span></span>

   ![récupérer à partir du cloud](images/recover-from-the-cloud.png)

### <a name="recover-a-locked-surface-hub"></a><span data-ttu-id="d1a32-153">Récupérer un Surface Hub verrouillé</span><span class="sxs-lookup"><span data-stu-id="d1a32-153">Recover a locked Surface Hub</span></span>

<span data-ttu-id="d1a32-154">À de rares occasions, un SurfaceHub peut rencontrer une erreur lors du nettoyage des données utilisateur et d’application à la fin d’une session.</span><span class="sxs-lookup"><span data-stu-id="d1a32-154">On rare occasions, a Surface Hub may encounter an error while cleaning up user and app data at the end of a session.</span></span> <span data-ttu-id="d1a32-155">Lorsque cela se produit, l’appareil redémarre automatiquement et tente à nouveau l’opération.</span><span class="sxs-lookup"><span data-stu-id="d1a32-155">When this happens, the device automatically restarts and tries the operation again.</span></span> <span data-ttu-id="d1a32-156">Toutefois, si cette opération échoue à plusieurs reprises, l’appareil se verrouille automatiquement pour protéger les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1a32-156">But if this operation fails repeatedly, the device automatically locks to protect user data.</span></span> <span data-ttu-id="d1a32-157">Pour le déverrouiller, vous devez [réinitialiser](#reset-a-surface-hub) l’appareil ou, si cela ne fonctionne pas, le récupérer à partir du cloud.</span><span class="sxs-lookup"><span data-stu-id="d1a32-157">To unlock it, you must [reset the device](#reset-a-surface-hub) or, if that doesn't work, recover it from the cloud.</span></span>

1. <span data-ttu-id="d1a32-158">Recherchez le commutateur d’alimentation en bas du Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-158">Locate the power switch on the bottom of Surface Hub.</span></span> <span data-ttu-id="d1a32-159">Le commutateur d’alimentation est à côté de la connexion de cordon d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d1a32-159">The power switch is next to the power cord connection.</span></span> <span data-ttu-id="d1a32-160">Pour plus d’informations sur le commutateur d’alimentation, voir le Guide de préparation du [site Surface Hub (PDF).](surface-hub-site-readiness-guide.md)</span><span class="sxs-lookup"><span data-stu-id="d1a32-160">For more information about the power switch, see the [Surface Hub Site Readiness Guide (PDF)](surface-hub-site-readiness-guide.md).</span></span>

2. <span data-ttu-id="d1a32-161">Pendant que le Surface Hub affiche l’écran d’accueil, utilisez le commutateur d’alimentation pour désactiver le Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-161">While the Surface Hub displays the Welcome screen, use the power switch to turn off the Surface Hub.</span></span>

3. <span data-ttu-id="d1a32-162">Utilisez le commutateur d’alimentation pour activer de nouveau le Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-162">Use the power switch to turn the Surface Hub back on.</span></span> <span data-ttu-id="d1a32-163">L’appareil démarre et affiche l’écran du logo Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="d1a32-163">The device starts and displays the Surface Hub Logo screen.</span></span> <span data-ttu-id="d1a32-164">Lorsque vous voyez des points de rotation sous le logo Surface Hub, utilisez le commutateur d’alimentation pour le désactiver à nouveau.</span><span class="sxs-lookup"><span data-stu-id="d1a32-164">When you see spinning dots under the Surface Hub Logo, use the power switch to turn the Surface Hub off again.</span></span>  

4. <span data-ttu-id="d1a32-165">Répétez l’étape 3 trois fois ou jusqu’à ce que le Surface Hub affiche le message « Préparation de la réparation automatique ».</span><span class="sxs-lookup"><span data-stu-id="d1a32-165">Repeat step 3 three times, or until the Surface Hub displays the "Preparing Automatic Repair" message.</span></span> <span data-ttu-id="d1a32-166">Une fois ce message affiché, le Surface Hub affiche l’écran Windows RE.</span><span class="sxs-lookup"><span data-stu-id="d1a32-166">After it displays this message, the Surface Hub displays the Windows RE screen.</span></span>

 
5. <span data-ttu-id="d1a32-167">Sélectionnez **Réinitialiser pour réinstaller Windows**.</span><span class="sxs-lookup"><span data-stu-id="d1a32-167">Select **Reset to re-install Windows**.</span></span> 
![réinitialiser pour réinstaller](images/recover-from-cloud.png)

8. <span data-ttu-id="d1a32-169">Sélectionnez **Téléchargement cloud.**</span><span class="sxs-lookup"><span data-stu-id="d1a32-169">Select **Cloud download.**</span></span> 

   ![Téléchargement dans le cloud](images/recover-cloud-download.png)

>[!IMPORTANT]
><span data-ttu-id="d1a32-171">Si vous obtenez un message d’erreur indiquant **Impossible de télécharger,** sélectionnez **Annuler** et réessayez.</span><span class="sxs-lookup"><span data-stu-id="d1a32-171">If you get an error message indicating **Unable to Download**, select **Cancel** and try again.</span></span>

9. <span data-ttu-id="d1a32-172">Sélectionnez **Nettoyer entièrement le lecteur.**  
![ récupérer et nettoyer entièrement le lecteur</span><span class="sxs-lookup"><span data-stu-id="d1a32-172">Select **Fully clean the drive.** 
![recover and fully clean drive</span></span>](images/recover-fully-clean-drive.png)

10. <span data-ttu-id="d1a32-173">You will be asked **Are you ready to reset this device?**.</span><span class="sxs-lookup"><span data-stu-id="d1a32-173">You will be asked **Are you ready to reset this device?**.</span></span> <span data-ttu-id="d1a32-174">Sélectionnez **Réinitialiser**.</span><span class="sxs-lookup"><span data-stu-id="d1a32-174">Select **Reset**.</span></span> 
![récupérer et confirmer la réinitialisation](images/recover-confirm-reset.png)

11. <span data-ttu-id="d1a32-176">Le téléchargement commence et le processus de récupération indique **la réinitialisation de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d1a32-176">The download begins and the recovery process indicates **Resetting this device**.</span></span> 
![récupération affichée en cours](images/recover-in-progress.png)

## <a name="contact-support"></a><span data-ttu-id="d1a32-178">Contacter le support</span><span class="sxs-lookup"><span data-stu-id="d1a32-178">Contact Support</span></span>

<span data-ttu-id="d1a32-179">Si vous avez des questions ou avez besoin d’aide, vous pouvez [créer une demande de support.](https://support.microsoft.com/supportforbusiness/productselection)</span><span class="sxs-lookup"><span data-stu-id="d1a32-179">If you have questions or need help, you can [create a support request](https://support.microsoft.com/supportforbusiness/productselection).</span></span>


## <a name="related-topics"></a><span data-ttu-id="d1a32-180">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="d1a32-180">Related topics</span></span>

[<span data-ttu-id="d1a32-181">Gérer Microsoft Surface Hub</span><span class="sxs-lookup"><span data-stu-id="d1a32-181">Manage Microsoft Surface Hub</span></span>](manage-surface-hub.md)

[<span data-ttu-id="d1a32-182">Guide de l’administrateur Microsoft Surface Hub</span><span class="sxs-lookup"><span data-stu-id="d1a32-182">Microsoft Surface Hub administrator's guide</span></span>](surface-hub-administrators-guide.md)
