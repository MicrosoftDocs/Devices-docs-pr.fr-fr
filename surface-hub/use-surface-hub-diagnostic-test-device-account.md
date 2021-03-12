---
title: Utilisation de l’outil de diagnostic du matériel SurfaceHub pour tester un compte d’appareil
description: Utilisation de l’outil de diagnostic du matériel SurfaceHub pour tester un compte d’appareil
ms.assetid: a87b7d41-d0a7-4acc-bfa6-b9070f99bc9c
keywords: Paramètres d’accessibilité, application Paramètres, Options d’ergonomie
ms.prod: surface-hub
ms.sitesec: library
author: v-miegge
ms.author: v-miegge
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 6661f2347d2f411ed11fe6057ede8ca2bab07c33
ms.sourcegitcommit: f0c976664116c45605edf3d56c4f58119a246b93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "11406667"
---
# <a name="using-the-surface-hub-hardware-diagnostic-tool-to-test-a-device-account"></a>Utilisation de l’outil de diagnostic du matériel SurfaceHub pour tester un compte d’appareil

## <a name="introduction"></a>Introduction

> [!NOTE]
> La section « Paramètres du compte » de l’outil de diagnostic du matériel Surface Hub ne collecte aucune information. Le courrier électronique et le mot de passe entrés en tant qu’entrées sont utilisés uniquement directement sur votre environnement et ne sont pas collectés ou transférés à qui que ce soit. Les informations de connexion persistent uniquement jusqu’à la fermeture de l’application ou la fin de la session en cours sur le Surface Hub.

> [!IMPORTANT]
> * Les privilèges d’administrateur ne sont pas requis pour exécuter cette application.
> * Les résultats du diagnostic doivent être abordés avec votre administrateur local avant d’ouvrir un appel de service avec Microsoft.

### <a name="surface-hub-hardware-diagnostic"></a>Diagnostic matériel du Surface Hub

Par défaut, l’application [de diagnostic de](https://www.microsoft.com/store/apps/9nblggh51f2g) matériel Surface Hub n’est pas installée dans les versions antérieures du système Surface Hub. L’application est disponible gratuitement à partir du Microsoft Store. Des privilèges d’administrateur sont requis pour installer l’application.

   ![Capture d’écran du diagnostic matériel](images/01-diagnostic.png)

## <a name="about-the-surface-hub-hardware-diagnostic-tool"></a>À propos de l’outil de diagnostic du matériel Surface Hub

L’outil de diagnostic du matériel du Surface Hub est un outil facile à parcourir qui permet à l’utilisateur de tester de nombreux composants matériels au sein de l’appareil Surface Hub. Cet outil peut également tester et vérifier un compte d’appareil Surface Hub. Cet article explique comment utiliser le test Paramètres du compte dans l’outil de diagnostic du matériel du Surface Hub.

> [!NOTE]
> Le compte d’appareil du Surface Hub doit être créé avant que les tests soient effectués. Le Guide de l’administrateur Surface Hub fournit des instructions et des scripts PowerShell pour vous aider à créer des comptes d’appareil locaux, en ligne (Office365) ou hybrides. Pour plus d’informations, voir la rubrique Créer et tester un compte d’appareil [(Surface Hub)](https://docs.microsoft.com/surface-hub/create-and-test-a-device-account-surface-hub) dans le guide.

### <a name="device-account-testing-process"></a>Processus de test du compte d’appareil

1. Accédez à **Toutes les applications,** puis recherchez l’application de diagnostic du matériel Surface Hub.

    ![Capture d’écran de Toutes les applications](images/02-all-apps.png)

1. Lorsque l’application démarre, la page **d’accueil** fournit une fenêtre de texte pour documenter la raison pour laquelle vous testez le Hub. Cette note peut être enregistrée sur USB avec les résultats de diagnostic à la fin du test. Une fois que vous avez entré une note, sélectionnez le **bouton** Continuer.

    >[!NOTE]
    >Lors de l’enregistrement des résultats de diagnostic, ne modifiez pas le chemin d’accès par défaut ou sélectionnez un sous-direction. Les fichiers peuvent être copiés ultérieurement via l’application Explorateur de fichiers.

    ![Capture d’écran de bienvenue](images/03-welcome.png)

1. L’écran suivant vous offre la possibilité de tester tout ou partie des composants Surface Hub. Pour commencer à tester le compte d’appareil, sélectionnez **l’icône Résultats des** tests.

    ![Capture d’écran des options de test](images/04-test-results-1.png)

    ![Capture d’écran des résultats des tests](images/05-test-results-2.png)

1. Sélectionnez **Paramètres du compte.**  

    ![Capture d’écran des paramètres du compte](images/06-account-settings.png)

    L’écran Paramètres du compte est utilisé pour tester votre compte d’appareil.

    ![Capture d’écran des détails des paramètres du compte](images/07-account-settings-details.png)

1. Entrez l’adresse e-mail de votre compte d’appareil. Le mot de passe est facultatif, mais il est recommandé. Sélectionnez le **bouton Tester le** compte lorsque vous êtes prêt à continuer.

    ![Capture d’écran du compte test](images/08-test-account.png)

1. Une fois les tests terminés, examinez les résultats pour les quatre zones de test. Chaque section peut être étendue ou réduire en sélectionnant le signe Plus ou Moins en de côté de chaque rubrique.

    **Network**

    ![Capture d’écran du réseau](images/09-network.png)

    **Environment**

    ![Capture d’écran de l’environnement](images/10-environment.png)

    **Certificats**

    ![Capture d’écran des certificats](images/11-certificates.png)

    **Modèle d’confiance**

    ![Capture d’écran du modèle d’confiance](images/12-trust-model.png)

## <a name="appendix"></a>Annexe

### <a name="field-messages-and-resolution"></a>Messages de champ et résolution

#### <a name="network"></a>Network

Champ |Opération réussie |Échec |Comment |Référence
|------|------|------|------|------|
Connectivité Internet |L’appareil a une connectivité Internet |L’appareil n’a pas de connectivité Internet |Vérifie la connectivité Internet, y compris la connexion proxy |
HTTP Version |1.1 |1.0 |Si HTTP 1.0 est trouvé, cela provoquera un problème avec WU et le Store |
Connectivité Internet directe |Aucun proxy n’est configuré sur un appareil configuré par proxy |Non applicable |Informationnel. Votre appareil se trouve-t-il derrière un proxy ? |
Adresse proxy | | |Si elle est configurée, renvoie l’adresse proxy. |
Authentification proxy |Le proxy ne nécessite pas d’authentification |Proxy requires Proxy Auth |Le résultat peut être faux positif si un utilisateur a déjà ouvert une session dans Edge et s’est authentifié via le proxy. |
Proxy Auth Types | | |Si l’authentification proxy est utilisée, renvoyer les méthodes d’authentification publiées par le proxy.  |

#### <a name="environment"></a>Environment

Champ |Opération réussie |Échec |Comment |Référence
|------|------|------|------|------|
Domaine SIP | | |Informationnel.  |
Environnement Skype |Skype Entreprise Online, Skype Entreprise OnPrem, Skype Entreprise hybride |Informationnel. |Type d’environnement détecté. Remarque : l’hybride ne peut être détecté que si le mot de passe est entré.
LyncDiscover FQDN | | |Informationnel. Affiche le résultat DNS LyncDiscover |
LyncDiscover URI | | |Informationnel. Affiche l’URL utilisée pour effectuer un LyncDiscover sur votre environnement.|
LyncDiscover |Connexion réussie |Échec de connexion |Réponse du service web LyncDiscover. |
Nom d’hôte du pool SIP | | |Informationnel. Afficher le nom du pool SIP découvert à partir de LyncDiscover |

#### <a name="certificates-in-premises-hybrid-only"></a>Certificats (hybride local uniquement)

Certificat LyncDiscover

Champ |Opération réussie |Échec |Comment |Référence
|------|------|------|------|------|
LyncDiscover Cert CN | | |Informationnel. Affiche le nom commun du cert LD |
LyncDiscover Cert CA | | |Informationnel. Affiche l’ac LD Cert |
LyncDiscover Cert Root CA | | |Informationnel. Affiche l’ac racine LD Cert, si disponible. |
LD Trust Status |Le certificat est approuvé. |Le certificat n’est pas approuvé, veuillez ajouter l’ac racine. |Vérifiez le certificat par rapport au magasin de certificats local. Renvoie un résultat positif si l’ordinateur fait confiance au certificat.|[Télécharger et déployer des certificats Skype Entreprise à l’aide de PowerShell](https://blogs.msdn.microsoft.com/surfacehub/2016/06/07/download-and-deploy-skype-for-business-certificates-using-powershell/) / [Éléments pris en charge pour les packages d’approvisionnement Surface Hub](https://docs.microsoft.com/surface-hub/provisioning-packages-for-surface-hub#supported-items-for-surface-hub-provisioning-packages)

SIP Pool Certification

Champ |Opération réussie |Échec |Comment |Référence
|------|------|------|------|------|
SIP Pool Cert CN | | |(CONTENTS) |
SIP Pool Cert CA | | |(CONTENTS) |
État d’confiance du pool SIP |Le certificat est approuvé. |Le certificat n’est pas approuvé, veuillez ajouter l’ac racine. |Vérifiez le certificat par rapport au magasin de certificats local et renvoyez un positif si les appareils font confiance au certificat. |
CA racine du cert du pool SIP | | |Informations. Affichez l’ac racine de cert du pool SIP, si disponible. |

#### <a name="trust-model-on-premises-hybrid-only"></a>Modèle de confiance (hybride local uniquement)

Champ |Opération réussie |Échec |Comment |Référence
|------|------|------|------|------|
État du modèle d’confiance |Aucun problème de modèle d’confiance détecté. |Le domaine SIP et le domaine serveur sont différents, ajoutez les domaines suivants. |Vérifiez le nom de domaine complet LD/ Nom du serveur LD/Nom du serveur du pool pour le problème de modèle d’confiance. 
Domain Name(s) | | |Renvoyer la liste des domaines qui doivent être ajoutés pour que SFB se connecte. |
