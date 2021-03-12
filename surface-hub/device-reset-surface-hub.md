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
# <a name="reset-or-recover-a-surface-hub"></a>Réinitialiser ou récupérer un Surface Hub

Cet article explique comment réinitialiser ou récupérer un Microsoft Surface Hub.  

[La réinitialisation du Surface Hub](#reset-a-surface-hub) renvoie son système d’exploitation à la dernière mise à jour cumulative de Windows et supprime tous les fichiers utilisateur locaux et les informations de configuration. Les informations supprimées sont les suivantes :

- Le compte d’appareil
- Informations de compte pour les administrateurs locaux de l’appareil
- Informations de joint-joint de domaine ou azure ad-join
- Informations d’inscription de la Gestion des périphériques mobiles (MDM)
- Informations de configuration définies à l’aide de LAM ou de l’application Paramètres

[La récupération d’un Surface Hub à partir du cloud](#recover-a-surface-hub-from-the-cloud) supprime également ces informations. En outre, le Surface Hub télécharge une nouvelle image de système d’exploitation et l’installe. Vous pouvez spécifier si le processus de récupération conserve les autres informations stockées sur le Surface Hub. La même image de système d’exploitation est utilisée par l’outil de récupération [Surface Hub](surface-hub-recovery-tool.md) si vous avez besoin de récupérer un Surface Hub pour lequel aucune de ces options ne peut être utilisée.

## <a name="reset-a-surface-hub"></a>Réinitialiser un Surface Hub

Vous de devez peut-être réinitialiser votre Surface Hub pour des raisons telles que les suivantes :

- Vous redéfinissez l’appareil pour un nouvel espace de réunion et souhaitez le reconfigurer.
- Vous souhaitez modifier la façon dont vous gérez localement l’appareil.
- Le nom d’utilisateur ou le mot de passe du compte d’appareil ou du compte Administrateur a été perdu.
- Une fois que vous avez installé une mise à jour, les performances de l’appareil diminuent.

Pendant le processus de réinitialisation, si un écran vide s’affiche pendant de longues périodes, veuillez patienter et ne pas prendre d’action.

> [!WARNING]
> Le processus de réinitialisation de l’appareil peut prendre jusqu’à six heures. Ne dés désactiver ni débrancher le Surface Hub tant que le processus n’est pas terminé. Si vous interrompez le processus, l’appareil devient inopérable. L’appareil nécessite un service de garantie pour devenir opérationnel à nouveau.

1. Sur votre Surface Hub, ouvrez **Paramètres**.

   ![Image that shows Settings app for Surface Hub.](images/sh-settings.png)

2. Sélectionnez **Mettre à jour & sécurité**.

   ![Image that shows Update & Security group in Settings app for Surface Hub.](images/sh-settings-update-security.png)

3. Sélectionnez **Récupération,** puis, sous **Réinitialiser l’appareil,** **sélectionnez Démarrer.**

   > [!IMPORTANT]
   > Assurez-vous que votre clé BitLocker est disponible avant de réinitialiser l’appareil, car vous y serez invité ultérieurement. Pour plus d’informations, voir [Enregistrer votre clé BitLocker.](save-bitlocker-key-surface-hub.md) Lorsque le Hub redémarre sur la partition de récupération, il vous invite à entrer la clé BitLocker. Ignorer cette invite entraîne l’échec de la réinitialisation.
   
   ![Image qui illustre l’option Réinitialiser l’appareil dans l’application Paramètres du Surface Hub.](images/sh-settings-reset-device.png)

   Une fois le processus de réinitialisation terminé, le Surface Hub redémarre le programme [de première](first-run-program-surface-hub.md) opération. Si le processus de réinitialisation rencontre un problème, il rétablit le Surface Hub à l’image du système d’exploitation existant, puis affiche l’écran d’accueil.

<span id="cloud-recovery" />

## <a name="recover-a-surface-hub-from-the-cloud"></a>Récupérer un Surface Hub à partir du cloud

Si, pour une raison quelconque, le Surface Hub devient inutilisable, vous pouvez toujours le récupérer à partir du cloud sans l’aide du Support Microsoft. Le Surface Hub peut télécharger une nouvelle image de système d’exploitation à partir du cloud et utiliser cette image pour réinstaller son système d’exploitation.

Vous de devez peut-être utiliser ce type de processus de récupération dans les circonstances suivantes :

- [Le Surface Hub ou ses comptes associés sont entrés dans un état instable](#recover-a-surface-hub-in-a-bad-state)
- [Le Surface Hub est verrouillé](#recover-a-locked-surface-hub)

>[!IMPORTANT]
>La **récupération à partir du processus cloud** nécessite une connexion câblé qui fournit une connectivité Internet ouverte (pas de proxy ou d’autres invites d’authentification).

### <a name="recover-a-surface-hub-in-a-bad-state"></a>Récupérer un Surface Hub se trouvant dans un état incorrect

Si le compte d’appareil passe dans un état instable ou si le compte d’administrateur rencontre des problèmes, vous pouvez utiliser l’application Paramètres pour démarrer le processus de récupération cloud. Vous devez utiliser le processus [](#reset-a-surface-hub) de récupération cloud uniquement lorsque le processus de réinitialisation de l’appareil ne corrige pas le problème.

1. Sur votre Surface Hub, sélectionnez Mise à jour des **paramètres** &gt; **& de** &gt; **sécurité.**

2. Sous **Récupérer à partir du cloud, sélectionnez** **Redémarrer maintenant.**

   ![récupérer à partir du cloud](images/recover-from-the-cloud.png)

### <a name="recover-a-locked-surface-hub"></a>Récupérer un Surface Hub verrouillé

À de rares occasions, un SurfaceHub peut rencontrer une erreur lors du nettoyage des données utilisateur et d’application à la fin d’une session. Lorsque cela se produit, l’appareil redémarre automatiquement et tente à nouveau l’opération. Toutefois, si cette opération échoue à plusieurs reprises, l’appareil se verrouille automatiquement pour protéger les données utilisateur. Pour le déverrouiller, vous devez [réinitialiser](#reset-a-surface-hub) l’appareil ou, si cela ne fonctionne pas, le récupérer à partir du cloud.

1. Recherchez le commutateur d’alimentation en bas du Surface Hub. Le commutateur d’alimentation est à côté de la connexion de cordon d’alimentation. Pour plus d’informations sur le commutateur d’alimentation, voir le Guide de préparation du [site Surface Hub (PDF).](surface-hub-site-readiness-guide.md)

2. Pendant que le Surface Hub affiche l’écran d’accueil, utilisez le commutateur d’alimentation pour désactiver le Surface Hub.

3. Utilisez le commutateur d’alimentation pour activer de nouveau le Surface Hub. L’appareil démarre et affiche l’écran du logo Surface Hub. Lorsque vous voyez des points de rotation sous le logo Surface Hub, utilisez le commutateur d’alimentation pour le désactiver à nouveau.  

4. Répétez l’étape 3 trois fois ou jusqu’à ce que le Surface Hub affiche le message « Préparation de la réparation automatique ». Une fois ce message affiché, le Surface Hub affiche l’écran Windows RE.

 
5. Sélectionnez **Réinitialiser pour réinstaller Windows**. 
![réinitialiser pour réinstaller](images/recover-from-cloud.png)

8. Sélectionnez **Téléchargement cloud.** 

   ![Téléchargement dans le cloud](images/recover-cloud-download.png)

>[!IMPORTANT]
>Si vous obtenez un message d’erreur indiquant **Impossible de télécharger,** sélectionnez **Annuler** et réessayez.

9. Sélectionnez **Nettoyer entièrement le lecteur.**  
![ récupérer et nettoyer entièrement le lecteur](images/recover-fully-clean-drive.png)

10. You will be asked **Are you ready to reset this device?**. Sélectionnez **Réinitialiser**. 
![récupérer et confirmer la réinitialisation](images/recover-confirm-reset.png)

11. Le téléchargement commence et le processus de récupération indique **la réinitialisation de cet appareil.** 
![récupération affichée en cours](images/recover-in-progress.png)

## <a name="contact-support"></a>Contacter le support

Si vous avez des questions ou avez besoin d’aide, vous pouvez [créer une demande de support.](https://support.microsoft.com/supportforbusiness/productselection)


## <a name="related-topics"></a>Rubriques associées

[Gérer Microsoft Surface Hub](manage-surface-hub.md)

[Guide de l’administrateur Microsoft Surface Hub](surface-hub-administrators-guide.md)
