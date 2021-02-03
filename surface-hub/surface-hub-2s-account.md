---
title: Créer un compte d’appareil SurfaceHub2S
description: Cette page décrit la procédure de création du compte d’appareil Surface Hub 2S.
keywords: séparer les valeurs par des virgules
ms.prod: surface-hub
ms.sitesec: library
author: greg-lindsay
ms.author: greglin
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 02/01/2021
ms.localizationpriority: Medium
ms.openlocfilehash: 76ac960be2ab30a30b4e29618f350a13a284f52a
ms.sourcegitcommit: 5cfac94c220c8a8d4620c6a7fa75ae2fae089c7f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "11312020"
---
# <span data-ttu-id="bc2e2-104">Créer un compte d’appareil SurfaceHub2S</span><span class="sxs-lookup"><span data-stu-id="bc2e2-104">Create Surface Hub 2S device account</span></span>

<span data-ttu-id="bc2e2-105">La création d’un compte d’appareil Surface Hub (également appelé boîte aux lettres de salle) permet au Surface Hub 2S de recevoir, d’approuver ou de refuser des demandes de réunion et de participer à des réunions.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-105">Creating a Surface Hub device account (also known as a Room mailbox) allows Surface Hub 2S to receive, approve, or decline meeting requests and join meetings.</span></span> <span data-ttu-id="bc2e2-106">Configurez le compte d’appareil lors de la configuration OOBE (Out-of-Box Experience).</span><span class="sxs-lookup"><span data-stu-id="bc2e2-106">Configure the device account during Out-of-Box Experience (OOBE) setup.</span></span> <span data-ttu-id="bc2e2-107">Si nécessaire, vous pouvez le modifier ultérieurement (sans passer par la configuration OOBE).</span><span class="sxs-lookup"><span data-stu-id="bc2e2-107">If needed, you can change it later (without going through OOBE setup).</span></span>

<span data-ttu-id="bc2e2-108">Vous pouvez créer le compte à partir du Centre d’administration Microsoft 365 en combinaison avec Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="bc2e2-108">You can create the account from  Microsoft 365 Admin center in combination with Windows PowerShell:</span></span> 

- <span data-ttu-id="bc2e2-109">**Créez un compte via le Centre d’administration.**</span><span class="sxs-lookup"><span data-stu-id="bc2e2-109">**Create account via Admin center**.</span></span> <span data-ttu-id="bc2e2-110">Pour répondre à la configuration minimale requise, vous pouvez configurer tout ce dont vous avez besoin pour le compte directement à partir du Centre d’administration [Microsoft 365.](https://admin.microsoft.com/AdminPortal)</span><span class="sxs-lookup"><span data-stu-id="bc2e2-110">To meet minimum requirements, you can configure everything you need for the account directly from the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal).</span></span> <span data-ttu-id="bc2e2-111">Certaines fonctionnalités telles que le partage de tableaux blancs directement à partir de l’application tableau blanc nécessitent l’utilisation de PowerShell pour configurer ActiveSync ; voir [Activer ActiveSync si l’utilisation de l’application de messagerie est requise](#enable-activesync-if-use-of-email-app-is-required) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-111">Some features like sharing whiteboards directly from the whiteboard app require using PowerShell to configure ActiveSync; see [Enable ActiveSync if use of email app is required](#enable-activesync-if-use-of-email-app-is-required) on this page.</span></span>

- <span data-ttu-id="bc2e2-112">**Créez un compte via PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="bc2e2-112">**Create account via PowerShell**.</span></span> <span data-ttu-id="bc2e2-113">Vous pouvez utiliser des scripts PowerShell pour faciliter la création de plusieurs comptes d’appareil et configurer rapidement des fonctionnalités spécifiques, notamment :</span><span class="sxs-lookup"><span data-stu-id="bc2e2-113">You can use PowerShell scripts to facilitate creation of multiple device accounts and quickly configure specific features including:</span></span>
    - <span data-ttu-id="bc2e2-114">Traitement du calendrier pour chaque compte d’appareil Surface Hub.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-114">Calendar processing for every Surface Hub device account.</span></span>
    - <span data-ttu-id="bc2e2-115">Réponses automatiques personnalisées aux demandes de planification.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-115">Custom auto replies to scheduling requests.</span></span>
    - <span data-ttu-id="bc2e2-116">Si la stratégie de boîte aux lettres ActiveSync par défaut a déjà été modifiée par une autre personne ou par un autre processus, vous devez probablement créer et affecter une nouvelle stratégie de boîte aux lettres ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-116">If the default ActiveSync mailbox policy has already been modified by someone else or by another process, you will likely have to create and assign a new ActiveSync mailbox policy.</span></span>

> [!TIP]
> <span data-ttu-id="bc2e2-117">Vous pouvez vérifier la configuration du compte en exécutant le [script de vérification de compte ci-dessous.](#account-verification-script)</span><span class="sxs-lookup"><span data-stu-id="bc2e2-117">You can check account setup by running the [Account verification script](#account-verification-script) below.</span></span>

> [!NOTE]  
> <span data-ttu-id="bc2e2-118">Le compte d’appareil Surface Hub ne prend pas en charge les fournisseurs d’identité fédérés tiers et doit être un compte Active Directory ou Azure Active Directory standard.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-118">The Surface Hub device account doesn’t support third-party Federated Identity Providers (FIPs) and must be a standard Active Directory or Azure Active Directory account.</span></span>

## <span data-ttu-id="bc2e2-119">Créer un compte via le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="bc2e2-119">Create account via admin center</span></span>

1. <span data-ttu-id="bc2e2-120">Dans le Centre d’administration Microsoft \*\*\*\* 365, sélectionnez Ressources et choisissez Salles **& équipement,** puis **sélectionnez + Ajouter une ressource.**</span><span class="sxs-lookup"><span data-stu-id="bc2e2-120">In the Microsoft 365 admin center, go to **Resources** and choose **Rooms & Equipment** and then select **+ Add resource**.</span></span>

2. <span data-ttu-id="bc2e2-121">Fournissez un nom et une adresse de messagerie pour le compte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-121">Provide a name and email address for the device account.</span></span> <span data-ttu-id="bc2e2-122">Laissez les paramètres restants inchangés dans l’état par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-122">Leave remaining settings unchanged in the default state.</span></span>

   ![Fournir un nom et une adresse de messagerie](images/sh2-account2.png)

   ![Laisser les paramètres restants inchangés dans l’état par défaut](images/sh2-account3.png)

3. <span data-ttu-id="bc2e2-125">Définissez le mot de passe du compte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-125">Set the password for the device account.</span></span> <span data-ttu-id="bc2e2-126">Pour définir le mot de passe, **sélectionnez Utilisateurs,** puis **Utilisateurs actifs.**</span><span class="sxs-lookup"><span data-stu-id="bc2e2-126">To set the password, choose **Users** and then select **Active Users**.</span></span> <span data-ttu-id="bc2e2-127">À présent, recherchez l’utilisateur nouvellement créé pour définir le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-127">Now search for the newly created user to set the password.</span></span> <span data-ttu-id="bc2e2-128">Veillez à ne **pas sélectionner l’option** Faire en sorte que cet utilisateur change son mot de passe lors **de sa première signature.**</span><span class="sxs-lookup"><span data-stu-id="bc2e2-128">Ensure that you **do not** select the option **Make this user change their password when they first sign in.**</span></span>

   ![Définir le mot de passe du compte d’appareil](images/sh2-account4.png)

4. <span data-ttu-id="bc2e2-130">Affectez la salle avec une licence Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-130">Assign the room with an Office 365 license.</span></span> <span data-ttu-id="bc2e2-131">Il est recommandé d’attribuer la licence \*\*\*\* salle de réunion Office 365, qui active automatiquement le compte pour Microsoft Teams et Skype Entreprise.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-131">It’s recommended to assign the Office 365 **Meeting Room** license, which automatically enables the account for Microsoft Teams and Skype for Business.</span></span>

   ![Attribuer une licence Office 365](images/sh2-account5.png)


> [!NOTE]  
> <span data-ttu-id="bc2e2-133">Si vous utilisez Skype Entreprise, vous devez finaliser l’installation via PowerShell - Calendrier Skype Entreprise : définir le traitement automatique du calendrier [pour](#set-calendar-auto-processing-skype-for-business-only) ce compte.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-133">If using Skype for Business, you will need to finalize setup via PowerShell -- Skype for Business Calendar: Set [Calendar Autoprocessing](#set-calendar-auto-processing-skype-for-business-only) for this account.</span></span> 

## <span data-ttu-id="bc2e2-134">Créer un compte via PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc2e2-134">Create account via PowerShell</span></span>

 <span data-ttu-id="bc2e2-135">L’utilisation de PowerShell pour automatiser rapidement des tâches sur Surface Hub ne nécessite pas nécessairement une expertise PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-135">Using PowerShell to rapidly automate tasks on Surface Hub does not necessarily require PowerShell expertise.</span></span> <span data-ttu-id="bc2e2-136">Assurez-vous que vous avez rempli les conditions préalables à l’installation avant d’utiliser les scripts appropriés sur cette page.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-136">Ensure you have completed the setup prerequisites before using the appropriate scripts on this page.</span></span>

### <span data-ttu-id="bc2e2-137">Conditions préalables à l’utilisation de PowerShell pour gérer le Surface Hub</span><span class="sxs-lookup"><span data-stu-id="bc2e2-137">Prerequisites for using PowerShell to manage Surface Hub</span></span> 

1. <span data-ttu-id="bc2e2-138">Lancez PowerShell avec des privilèges de compte élevés **(exécuter**en tant qu’administrateur) et assurez-vous que votre système est configuré pour exécuter des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-138">Launch PowerShell with elevated account privileges (**Run as Administrator**) and ensure your system is configured to run PowerShell scripts.</span></span> <span data-ttu-id="bc2e2-139">Pour en savoir plus, consultez la procédure [à propos des stratégies d’exécution.](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?)</span><span class="sxs-lookup"><span data-stu-id="bc2e2-139">To learn more, refer to [About Execution Policies](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?).</span></span> 
2. <span data-ttu-id="bc2e2-140">[Installez le module Azure PowerShell.](https://docs.microsoft.com/powershell/azure/install-az-ps)</span><span class="sxs-lookup"><span data-stu-id="bc2e2-140">[Install Azure PowerShell module](https://docs.microsoft.com/powershell/azure/install-az-ps).</span></span>


### <span data-ttu-id="bc2e2-141">Se connecter à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc2e2-141">Connect to Exchange Online PowerShell</span></span>

```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName admin@contoso.com -ShowProgress $true
```

### <span data-ttu-id="bc2e2-142">Créer une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="bc2e2-142">Create mailbox</span></span>

```powershell
New-Mailbox -MicrosoftOnlineServicesID 'SurfaceHub01@contoso.com' -Alias SurfaceHub01 -Name "Surface Hub 01" -Room -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString -String 'Pass@word1' -AsPlainText -Force)
```

### <span data-ttu-id="bc2e2-143">Définir le traitement automatique du calendrier (Skype Entreprise uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc2e2-143">Set Calendar auto-processing (Skype for Business only)</span></span>

```powershell
Set-CalendarProcessing -Identity 'SurfaceHub01@contoso.com' -AutomateProcessing AutoAccept -AddOrganizerToSubject $false -AllowConflicts $false -DeleteComments $false -DeleteSubject $false -RemovePrivateProperty $false
Set-CalendarProcessing -Identity 'SurfaceHub01@contoso.com' -AddAdditionalResponse $true -AdditionalResponse "This is a Microsoft Surface Hub. Please make sure this meeting is a Microsoft Teams meeting!"
```

### <span data-ttu-id="bc2e2-144">Activer ActiveSync si l’utilisation de l’application de messagerie est requise</span><span class="sxs-lookup"><span data-stu-id="bc2e2-144">Enable ActiveSync if use of email app is required</span></span>

 <span data-ttu-id="bc2e2-145">La stratégie ActiveSync par défaut fonctionne si elle reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-145">The default ActiveSync Policy will work if unchanged.</span></span> <span data-ttu-id="bc2e2-146">Sinon, créez Une nouvelle stratégie et affectez-la.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-146">Otherwise createStupid a new Policy and assign.</span></span>

```powershell
New-MobileDeviceMailboxPolicy -Name:"SurfaceHub" -PasswordEnabled:$false
#Assign Policy to Hub:
Set-CASMailbox -Identity SurfaceHub01@contoso.com -ActiveSyncMailboxPolicy "SurfaceHub"
```

### <span data-ttu-id="bc2e2-147">Se connecter à AzureAD</span><span class="sxs-lookup"><span data-stu-id="bc2e2-147">Connect to Azure AD</span></span>

```powershell
Connect-AzureAD
```

### <span data-ttu-id="bc2e2-148">Attribuer une licence</span><span class="sxs-lookup"><span data-stu-id="bc2e2-148">Assign a license</span></span>

```powershell
Set-AzureADUser -ObjectId 'SurfaceHub01@contoso.com' -UsageLocation US
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense 
$License.SkuId = "c7df2760-2c81-4ef7-b578-5b5392b571df" 
$Licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses 
$Licenses.AddLicenses = $License 
Set-AzureADUserLicense -ObjectId 'SurfaceHub01@contoso.com' -AssignedLicenses $Licenses
```

### <span data-ttu-id="bc2e2-149">Vérifier les licences disponibles</span><span class="sxs-lookup"><span data-stu-id="bc2e2-149">Check for available licenses</span></span>

```powershell
Get-AzureADUser -Filter "userPrincipalName eq 'SurfaceHub01@contoso.com'" |fl *
#Meeting Room Standard SKU:
6070a4c8-34c6-4937-8dfb-39bbc6397a60
```

## <span data-ttu-id="bc2e2-150">Script de vérification de compte</span><span class="sxs-lookup"><span data-stu-id="bc2e2-150">Account verification script</span></span>

<span data-ttu-id="bc2e2-151">Après avoir créé le compte d’appareil, vous pouvez exécuter le script de vérification suivant.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-151">After creating the device account, you can run the following verification script.</span></span> <span data-ttu-id="bc2e2-152">Ce script valide un compte d’appareil créé précédemment et produit un rapport récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-152">This script validates a previously-created device account and produces a summary report.</span></span> <span data-ttu-id="bc2e2-153">Par exemple:</span><span class="sxs-lookup"><span data-stu-id="bc2e2-153">For example:</span></span>

``` syntax
15 tests executed
0 failures
2 warnings
15 passed
```

<span data-ttu-id="bc2e2-154">Les détails relatifs aux paramètres spécifiques ne s’affichent pas.</span><span class="sxs-lookup"><span data-stu-id="bc2e2-154">Details of specific settings will not be shown.</span></span>

```PowerShell
# SHAccountValidate.ps1

$Error.Clear()
$ErrorActionPreference = "Stop"


# Cleans up set state such as remote powershell sessions
function Cleanup()
{
    if ($sessEx)
    {
        Remove-PSSession $sessEx
    }
    if ($sessSfb)
    {
        Remove-PSSession $sessSfb
    }
}

function PrintError($strMsg)
{
    Write-Host $strMsg -foregroundcolor "red"
}

function PrintSuccess($strMsg)
{
    Write-Host $strMsg -foregroundcolor "green"
}

function PrintAction($strMsg)
{
    Write-Host $strMsg -ForegroundColor Cyan
}


# Cleans up and prints an error message
function CleanupAndFail($strMsg)
{
    if ($strMsg)
    {
        PrintError($strMsg);
    }
    Cleanup
    exit 1
}

# Exits if there is an error set and prints the given message
function ExitIfError($strMsg)
{
    if ($Error)
    {
        CleanupAndFail($strMsg);
    }
}

$strUpn = Read-Host "What is the email address of the account you wish to validate?"
if (!$strUpn.Contains('@'))
{
    CleanupAndFail "$strUpn is not a valid email address"
}
$strExServer = Read-Host "What is your exchange server? (leave blank for online tenants)"
if ($strExServer.Equals(""))
{
    $fExIsOnline = $true
}
else
{
    $fExIsOnline = $false
}
$credEx = Get-Credential -Message "Please provide exchange user credentials"

$strRegistrarPool = Read-Host ("What is the Skype for Business registrar pool for $strUpn" + "? (leave blank for online tenants)")
$fSfbIsOnline = $strRegistrarPool.Equals("")

$fHasOnPrem = $true
if ($fSfbIsOnline -and $fExIsOnline)
{
    do
    {
        $strHasOnPrem = (Read-Host "Do you have an on-premises Active Directory (Y/N) (No if your domain services are hosted entirely online)").ToUpper()
    } while ($strHasOnPrem -ne "Y" -and $strHasOnPrem -ne "N")
    $fHasOnPrem = $strHasOnPrem.Equals("Y")
}

$fHasOnline = $false
if ($fSfbIsOnline -or $fExIsOnline)
{
    $fHasOnline = $true
}

if ($fSfbIsOnline)
{
    try {
        Import-Module SkypeOnlineConnector
    }
    catch
    {
        CleanupAndFail "To verify Skype for Business in online tenants you need the Lync Online Connector module from https://www.microsoft.com/download/details.aspx?id=39366"
    }
}
else
{
    $credSfb = (Get-Credential -Message "Please enter Skype for Business admin credentials")
}

if ($fHasOnline)
{
    $credSfb = $credEx
    try {
        Import-Module MSOnline
    }
    catch
    {
        CleanupAndFail "To verify accounts in online tenants you need the Azure Active Directory module for PowerShell from https://go.microsoft.com/fwlink/p/?linkid=236297"
    }
}

PrintAction "Connecting to Exchange Powershell Session..."
[System.Management.Automation.Runspaces.AuthenticationMechanism] $authType = [System.Management.Automation.Runspaces.AuthenticationMechanism]::Kerberos
if ($fExIsOnline)
{
    $authType = [System.Management.Automation.Runspaces.AuthenticationMechanism]::Basic
}
try
{
    $sessEx = $null
    if ($fExIsOnline)
    {
        $sessEx = New-PSSession -ConfigurationName microsoft.exchange -Credential $credEx -AllowRedirection -Authentication $authType -ConnectionUri "https://outlook.office365.com/powershell-liveid/" -WarningAction SilentlyContinue
    }
    else
    {
        $sessEx = New-PSSession -ConfigurationName microsoft.exchange -Credential $credEx -AllowRedirection -Authentication $authType -ConnectionUri https://$strExServer/powershell -WarningAction SilentlyContinue
    }
}
catch
{
}

if (!$sessEx)
{
    CleanupAndFail "Connecting to Exchange Powershell failed, please validate your server is accessible and credentials are correct"
}

PrintSuccess "Connected to Exchange Powershell Session"

PrintAction "Connecting to Skype for Business Powershell Session..."

if ($fSfbIsOnline)
{
    $sessSfb = New-CsOnlineSession -Credential $credSfb
}
else
{
    $sessSfb = New-PSSession -Credential $credSfb -ConnectionURI "https://$strRegistrarPool/OcsPowershell" -AllowRedirection -WarningAction SilentlyContinue
}

if (!$sessSfb)
{
    CleanupAndFail "Connecting to Skype for Business Powershell failed, please validate your server is accessible and credentials are correct"
}

PrintSuccess "Connected to Skype for Business Powershell"

if ($fHasOnline)
{
    $credMsol = $null
    if ($fExIsOnline)
    {
        $credMsol = $credEx
    }
    elseif ($fSfbIsOnline)
    {
        $credMsol = $credSfb
    }
    else
    {
        CleanupAndFail "Internal error - could not determine MS Online credentials"
    }
    try
    {
        PrintAction "Connecting to Azure Active Directory Services..."
        Connect-MsolService -Credential $credMsol
        PrintSuccess "Connected to Azure Active Directory Services"
    }
    catch
    {
        # This really shouldn't happen unless there is a network error
        CleanupAndFail "Failed to connect to MSOnline"
    }
}


PrintAction "Importing remote sessions into the local session..."
try
{
    $importEx = Import-PSSession $sessEx -AllowClobber -WarningAction SilentlyContinue -DisableNameChecking
    $importSfb = Import-PSSession $sessSfb -AllowClobber -WarningAction SilentlyContinue -DisableNameChecking
}
catch
{
}
if (!$importEx -or !$importSfb)
{
    CleanupAndFail "Import failed"
}
PrintSuccess "Import successful"


$mailbox = $null
try
{
    $mailbox = Get-Mailbox -Identity $strUpn
}
catch
{
}

if (!$mailbox)
{
    CleanupAndFail "Account exists check failed. Unable to find the mailbox for $strUpn - please make sure the Exchange account exists on $strExServer"
}

$exchange = $null
if (!$fExIsOnline)
{
    $exchange = Get-ExchangeServer
    if (!$exchange -or !$exchange.IsE14OrLater)
    {
        CleanupAndFail "A compatible exchange server version was not found. Please use at least exchange 2010."
    }
}


$strAlias = $mailbox.UserPrincipalName
$strDisplayName = $mailbox.DisplayName

$strLinkedAccount = $strLinkedDomain = $strLinkedUser = $strLinkedServer = $null
$credLinkedDomain = $Null
if (!$fExIsOnline -and ![System.String]::IsNullOrEmpty($mailbox.LinkedMasterAccount) -and !$mailbox.LinkedMasterAccount.EndsWith("\SELF"))
{
    $strLinkedAccount = $mailbox.LinkedMasterAccount
    $strLinkedDomain = $strLinkedAccount.substring(0,$strLinkedAccount.IndexOf('\'))
    $strLinkedUser = $strLinkedAccount.substring($strLinkedAccount.IndexOf('\') + 1)
    $strLinkedServer = Read-Host "What is the domain controller for the $strLinkedDomain"
    $credLinkedDomain = (Get-Credential -Message "Please provide credentials for $strLinkedDomain")
}







Write-Host
Write-Host
Write-Host
PrintAction "Performing verification checks on $strDisplayName..."
$Global:iTotalFailures = 0
$global:iTotalWarnings = 0
$Global:iTotalPasses = 0

function Validate()
{
    Param(
        [string]$Test,
        [bool]  $Condition,
        [string]$FailureMsg,
        [switch]$WarningOnly
    )

    Write-Host -NoNewline -ForegroundColor White $Test.PadRight(100,'.')
    if ($Condition)
    {
        Write-Host -ForegroundColor Green "Passed"
        $global:iTotalPasses++
    }
    else
    {
        if ($WarningOnly)
        {
            Write-Host -ForegroundColor Yellow ("Warning: "+$FailureMsg)
            $global:iTotalWarnings++
        }
        else
        {
            Write-Host -ForegroundColor Red ("Failed: "+$FailureMsg)
            $global:iTotalFailures++
        }
    }
}
```

## <span data-ttu-id="bc2e2-155">Si vous souhaitez en savoir plus</span><span class="sxs-lookup"><span data-stu-id="bc2e2-155">Learn more</span></span>

- [<span data-ttu-id="bc2e2-156">Créer des comptes SurfaceHub2S locaux avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc2e2-156">Create Surface Hub 2S on-premises accounts with PowerShell</span></span>](surface-hub-2s-onprem-powershell.md)