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
# Réinitialisation et récupération pour Surface Hub 2S

Si vous rencontrez des problèmes avec Surface Hub 2S, vous pouvez rétablir les paramètres d’usine ou restaurer l’appareil à l’aide d’un lecteur USB.

Pour commencer, connectez-vous au Surface Hub 2S avec les informations d’identification d’administrateur, ouvrez l’application **Paramètres,** sélectionnez Mettre à jour & **sécurité,** puis sélectionnez **Récupération.**

## Réinitialisez l’appareil

   > [!IMPORTANT]
   > Assurez-vous que votre clé BitLocker est disponible avant de réinitialiser l’appareil, car vous y serez invité ultérieurement. Pour plus d’informations, voir [Enregistrer votre clé BitLocker.](save-bitlocker-key-surface-hub.md)

1. Pour réinitialiser l’appareil, **sélectionnez Démarrer.**

2. Lorsque la fenêtre **Prêt à réinitialiser cet appareil** s’affiche, sélectionnez **Réinitialiser.** 
  
   > [!IMPORTANT]
   > Lorsque le Hub redémarre sur la partition de récupération, il vous invite à entrer la clé BitLocker. Ignorer cette invite entraîne l’échec de la réinitialisation. Une fois que vous avez entré la clé BitLocker, le Hub réinstalle le système d’exploitation à partir de la partition de récupération. Cela peut prendre jusqu’à une heure.
  
3. Pour reconfigurer l’appareil, exécutez le programme d’installation pour la première fois.

4. Si vous gérez l’appareil à l’aide de Microsoft Intune ou d’une autre solution de gestion des appareils mobiles, retirez et supprimez l’enregistrement précédent, puis ré-inscrivez le nouvel appareil. Pour plus d’informations, voir Supprimer des appareils à l’aide de l’effacement, de la suppression ou de la [désinscrire manuellement de l’appareil.](https://docs.microsoft.com/intune/devices-wipe)

   > [!div class="mx-imgBorder"]
   > ![*Réinitialiser et récupérer pour Surface Hub 2S*](images/sh2-reset.png)
   <br/>*Figure1. Réinitialisation et récupération pour Surface Hub 2S* 

## Récupérer le Surface Hub 2S à l’aide d’un lecteur de récupération USB

Nouveauté du Surface Hub 2S, vous pouvez désormais réinstaller l’appareil à l’aide d’une image de récupération.

### Récupération à partir d’un lecteur USB

À l’aide du Surface Hub 2S, vous pouvez réinstaller l’appareil à l’aide d’une image de récupération. En faisant cela, vous pouvez réinstaller l’appareil aux paramètres d’usine si vous avez perdu la clé BitLocker ou si vous n’avez plus d’informations d’identification d’administrateur pour l’application Paramètres.

>[!NOTE]
>Utilisez un lecteur USB 3.0 avec 8 Go ou 16 Go de stockage, au format FAT32.

1. À partir d’un PC distinct, téléchargez l’image de récupération de fichier .zip à partir du site web [Surface Recovery,](https://support.microsoft.com/surfacerecoveryimage?devicetype=surfacehub2s) puis revenir à ces instructions. 

1. Dans la zone de recherche de la barre **** des tâches, entrez le lecteur de **récupération,** puis sélectionnez Créer un lecteur de récupération ou un lecteur de récupération **dans** les résultats. Vous devrez peut-être entrer un mot de passe d’administrateur ou confirmer votre choix.

1. Dans la **zone Contrôle de compte d’utilisateur,** sélectionnez **Oui.**

1. Veillez à effacer les fichiers système **de la back up dans la** case à cocher du lecteur de récupération, puis sélectionnez **Suivant**.

1. Sélectionnez votre lecteur USB, puis **sélectionnez Suivant > Créer.**  Certains utilitaires doivent être copiés sur le lecteur de récupération, ce qui peut prendre quelques minutes.

1. Lorsque le lecteur de récupération est prêt, sélectionnez **Terminer.**

1. Double-cliquez sur le fichier .zip d’image de récupération que vous avez précédemment téléchargé pour l’ouvrir.

1. Sélectionnez tous les fichiers du dossier image de récupération, copiez-les à la racine de votre lecteur USB, puis sélectionnez Choisir de remplacer les fichiers dans **la destination.**

1. Une fois la copie des fichiers terminée, sélectionnez l’icône Supprimer le matériel et **éjecter** le média en toute sécurité dans la barre des tâches, puis supprimez votre lecteur USB.

1. Connectez le lecteur USB à n’importe quel port USB-C ou USB-A sur le Surface Hub 2S.

1. Désactiver le Hub, puis suivre les étapes suivantes pour démarrer à partir du lecteur USB :

   1. Tout en appuyant sur le bouton Descendre le volume, appuyez sur le bouton d’alimentation.
   1. Continuez à appuyer sur les deux boutons jusqu’à ce que le logo Windows s’affiche.
   1. Relâchez le bouton d’alimentation, mais maintenez le bouton Descendre le volume jusqu’à ce que l’interface utilisateur d’installation commence.

      ![*Utiliser les boutons Baisser le volume et Alimentation pour lancer la récupération*](images/sh2-keypad.png)
      <br>*Figure2. Boutons Volume et Alimentation*

1. Dans l’écran de sélection de la langue, sélectionnez la langue d’affichage de votre Surface Hub 2S.

1. Sélectionnez **Récupérer à partir d’un lecteur** et **nettoyez entièrement le lecteur,** puis sélectionnez **Récupérer.** Si vous êtes invité à obtenir une clé BitLocker, **sélectionnez Ignorer ce lecteur.** Surface Hub 2S redémarre plusieurs fois et prend environ 30 minutes pour terminer le processus de récupération.

Lorsque l’écran de configuration s’affiche pour la première fois, supprimez le lecteur USB.

## Contacter le support

Si vous avez des questions ou avez besoin d’aide, vous pouvez [créer une demande de support.](https://support.microsoft.com/supportforbusiness/productselection)
