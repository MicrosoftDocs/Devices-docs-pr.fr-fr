---
title: Se connecter à Surface Hub avec MicrosoftAuthenticator
description: Utilisez MicrosoftAuthenticator sur votre appareil mobile pour vous connecter à Surface Hub.
ms.prod: surface-hub
ms.sitesec: library
author: dansimp
ms.author: dansimp
ms.topic: article
ms.date: 08/28/2017
ms.reviewer: ''
manager: laurawi
localizationpriority: medium
ms.openlocfilehash: f8a2bf8ddb75ca6dd3ff89e16fe0d37e099be29d
ms.sourcegitcommit: 85f5a2e67b34fe073ec588ed441ebee239ab0ac6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400735"
---
# <a name="sign-in-to-surface-hub-with-microsoft-authenticator"></a><span data-ttu-id="0b433-103">Se connecter à Surface Hub avec MicrosoftAuthenticator</span><span class="sxs-lookup"><span data-stu-id="0b433-103">Sign in to Surface Hub with Microsoft Authenticator</span></span>

<span data-ttu-id="0b433-104">Les membres de votre organisation peuvent se connecter à un Surface Hub sans mot de passe à l’aide de l’application MicrosoftAuthenticator, disponible sur iOS et Android.</span><span class="sxs-lookup"><span data-stu-id="0b433-104">People in your organization can sign in to a Surface Hub  without a password using the Microsoft Authenticator app, available on Android and iOS.</span></span>

## <a name="organization-prerequisites"></a><span data-ttu-id="0b433-105">Conditions préalables pour l’organisation</span><span class="sxs-lookup"><span data-stu-id="0b433-105">Organization prerequisites</span></span>

<span data-ttu-id="0b433-106">Pour permettre aux utilisateurs de votre organisation de se connecter à Surface Hub avec leurs téléphones et autres appareils au lieu d’un mot de passe, vous devez vous assurer que votre organisation remplit ces conditions préalables:</span><span class="sxs-lookup"><span data-stu-id="0b433-106">To let people in your organization sign in to Surface Hub with their phones and other devices instead of a password, you’ll need to make sure that your organization meets these prerequisites:</span></span> 

- <span data-ttu-id="0b433-107">Votre organisation doit être une organisation hybride ou Cloud uniquement, appuyée sur Azure ActiveDirectory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="0b433-107">Your organization must be a hybrid or cloud-only organization, backed by Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="0b433-108">Pour plus d’informations, voir [Qu'est-ce que Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-whatis).</span><span class="sxs-lookup"><span data-stu-id="0b433-108">For more information, see [What is Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-whatis)</span></span>

- <span data-ttu-id="0b433-109">Assurez-vous de disposer au moins un abonnement Office365E3.</span><span class="sxs-lookup"><span data-stu-id="0b433-109">Make sure you have at minimum an Office 365 E3 subscription.</span></span> 

- <span data-ttu-id="0b433-110">[Configurer l'authentification multifacteur](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings).</span><span class="sxs-lookup"><span data-stu-id="0b433-110">[Configure Multi-Factor Authentication](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings).</span></span> <span data-ttu-id="0b433-111">Vérifiez que **Notification via application mobile** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0b433-111">Make sure **Notification through mobile app** is selected.</span></span> 

    ![Options de l'authentification multifacteur](images/mfa-options.png)

- <span data-ttu-id="0b433-113">Activer l’hébergement de contenu sur les services Azure AD tels qu’Office, SharePoint, etc.</span><span class="sxs-lookup"><span data-stu-id="0b433-113">Enable content hosting on Azure AD services such as Office, SharePoint, etc.</span></span> 

- <span data-ttu-id="0b433-114">Le Surface Hub doit exécuter Windows10, version1703 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0b433-114">Surface Hub must be running Windows 10, version 1703 or later.</span></span>

- <span data-ttu-id="0b433-115">Le Surface Hub est configuré avec un compte local ou de domaine joint.</span><span class="sxs-lookup"><span data-stu-id="0b433-115">Surface Hub is set up with either a local or domain-joined account.</span></span>

## <a name="individual-prerequisites"></a><span data-ttu-id="0b433-116">Conditions préalables des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0b433-116">Individual prerequisites</span></span>

- <span data-ttu-id="0b433-117">Un téléphone Android avec la version 6.0 ou ultérieure, ou un iPhone ou un iPad avec iOS9 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0b433-117">An Android phone running 6.0 or later, or an iPhone or iPad running iOS9 or later</span></span> 

- <span data-ttu-id="0b433-118">La version la plus récente de l’application MicrosoftAuthenticator issue du magasin d’applications approprié</span><span class="sxs-lookup"><span data-stu-id="0b433-118">The most recent version of the Microsoft Authenticator app from the appropriate app store</span></span>

    >[!NOTE]
    ><span data-ttu-id="0b433-119">Sur iOS, la version de l’application doit être égale ou ultérieure à5.4.0.</span><span class="sxs-lookup"><span data-stu-id="0b433-119">On iOS, the app version must be 5.4.0 or higher.</span></span>
    >
    ><span data-ttu-id="0b433-120">L’application MicrosoftAuthenticator sur les téléphones qui exécutent un système d’exploitation Windows ne peut pas être utilisée pour se connecter à Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="0b433-120">The Microsoft Authenticator app on phones running a Windows operating system can't be used to sign in to Surface Hub.</span></span>

- <span data-ttu-id="0b433-121">Code secret ou écran de verrouillage activé sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="0b433-121">Passcode or screen lock on your device is enabled</span></span>

## <a name="how-to-set-up-the-microsoft-authenticator-app"></a><span data-ttu-id="0b433-122">Comment utiliser l’application Microsoft Authenticator</span><span class="sxs-lookup"><span data-stu-id="0b433-122">How to set up the Microsoft Authenticator app</span></span>

>[!NOTE]
><span data-ttu-id="0b433-123">Si le Portail d’entreprise est installé sur votre appareil Android, désinstallez-le avant de configurer MicrosoftAuthenticator.</span><span class="sxs-lookup"><span data-stu-id="0b433-123">If Company Portal is installed on your Android device, uninstall it before you set up Microsoft Authenticator.</span></span> <span data-ttu-id="0b433-124">Quand vous aurez configuré l'application, vous pourrez réinstaller le Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0b433-124">After you set up the app, you can reinstall Company Portal.</span></span>
>
><span data-ttu-id="0b433-125">Si vous avez déjà configuré MicrosoftAuthenticator sur votre téléphone et inscrit votre appareil, accédez aux instructions de connexion.</span><span class="sxs-lookup"><span data-stu-id="0b433-125">If you have already set up Microsoft Authenticator on your phone and registered your device, go to the sign-in instructions.</span></span>

1. <span data-ttu-id="0b433-126">Ajoutez votre compte professionnel ou scolaire à MicrosoftAuthenticator pour Multi-Factor Authentication.</span><span class="sxs-lookup"><span data-stu-id="0b433-126">Add your work or school account to Microsoft Authenticator for Multi-Factor Authentication.</span></span> <span data-ttu-id="0b433-127">Vous aurez besoin d’un code QR fourni par votre service informatique.</span><span class="sxs-lookup"><span data-stu-id="0b433-127">You will need a QR code provided by your IT department.</span></span> <span data-ttu-id="0b433-128">Pour plus d’aide, consultez [Prise en main de l’application MicrosoftAuthenticator](https://docs.microsoft.com/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to).</span><span class="sxs-lookup"><span data-stu-id="0b433-128">For help, see [Get started with the Microsoft Authenticator app](https://docs.microsoft.com/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to).</span></span>
2. <span data-ttu-id="0b433-129">Accédez à **Paramètres** et enregistrez votre appareil.</span><span class="sxs-lookup"><span data-stu-id="0b433-129">Go to **Settings** and register your device.</span></span>
3. <span data-ttu-id="0b433-130">Revenez à la page des comptes et choisissez **Activer la connexion par téléphone** dans le menu déroulant du compte.</span><span class="sxs-lookup"><span data-stu-id="0b433-130">Return to the accounts page and choose **Enable phone sign-in** from the account dropdown menu.</span></span>

## <a name="how-to-sign-in-to-surface-hub-during-a-meeting"></a><span data-ttu-id="0b433-131">Comment se connecter à Surface Hub pendant une réunion</span><span class="sxs-lookup"><span data-stu-id="0b433-131">How to sign in to Surface Hub during a meeting</span></span>

1. <span data-ttu-id="0b433-132">Une fois que vous avez configuré une réunion, accédez au Surface Hub et sélectionnez **Se connecter pour voir vos réunions et vos fichiers**.</span><span class="sxs-lookup"><span data-stu-id="0b433-132">After you’ve set up a meeting, go to the Surface Hub and select **Sign in to see your meetings and files**.</span></span>

    >[!NOTE]
    ><span data-ttu-id="0b433-133">Si vous ne savez pas comment programmer une réunion sur un Surface Hub, voir [Programmer une réunion sur Surface Hub](https://support.microsoft.com/help/17325/surfacehub-schedulemeeting).</span><span class="sxs-lookup"><span data-stu-id="0b433-133">If you’re not sure how to schedule a meeting on a Surface Hub, see [Schedule a meeting on Surface Hub](https://support.microsoft.com/help/17325/surfacehub-schedulemeeting).</span></span>

    ![Capture d’écran de l'option de connexion sur Surface Hub](images/sign-in.png)

2. <span data-ttu-id="0b433-135">Vous verrez une liste des personnes invitées à la réunion.</span><span class="sxs-lookup"><span data-stu-id="0b433-135">You’ll see a list of the people invited to the meeting.</span></span> <span data-ttu-id="0b433-136">Sélectionnez vous-même (ou la personne qui souhaite se connecter – assurez-vous que cette personne a effectué les étapes de configuration de son appareil avant la réunion), puis sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="0b433-136">Select yourself (or the person who wants to sign in – make sure this person has gone through the steps to set up their device before your meeting), and then select **Continue**.</span></span>

    ![Capture d’écran de la liste des participants à une réunion](images/attendees.png)

    <span data-ttu-id="0b433-138">Vous verrez un code sur le Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="0b433-138">You'll see a code on the Surface Hub.</span></span>

    ![Capture d’écran du code pour approuver la connexion](images/approve-signin.png)

3. <span data-ttu-id="0b433-140">Pour approuver la connexion, ouvrez l’application Authenticator, entrez le code à quatre chiffres qui s’affiche sur le Surface Hub et sélectionnez **Approuver**.</span><span class="sxs-lookup"><span data-stu-id="0b433-140">To approve the sign-in, open the Authenticator app, enter the four-digit code that’s displayed on the Surface Hub, and select **Approve**.</span></span> <span data-ttu-id="0b433-141">Vous devrez entrer le code PIN ou utiliser votre empreinte digitale pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="0b433-141">You will then be asked to enter the PIN or use your fingerprint to complete the sign in.</span></span> 

    ![Capture d’écran de l’écran Approuver la connexion dans MicrosoftAuthenticator](images/approve-signin2.png)

<span data-ttu-id="0b433-143">Vous pouvez désormais accéder à tous les fichiers par l'intermédiaire de l’application OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0b433-143">You can now access all files through the OneDrive app.</span></span>
