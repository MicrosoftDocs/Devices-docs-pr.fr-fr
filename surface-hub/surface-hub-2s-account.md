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
ms.date: 02/18/2021
ms.localizationpriority: Medium
ms.openlocfilehash: 3afd4115ff4bd22a84f9a5fb86ceb6805c347f8a
ms.sourcegitcommit: 7e1b351024e33926901ddbdc562ba12aea0b4196
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "11385222"
---
# <a name="create-surface-hub-2s-device-account"></a>Créer un compte d’appareil SurfaceHub2S

La création d’un compte d’appareil Surface Hub (également appelé boîte aux lettres de salle) permet au Surface Hub 2S de recevoir, d’approuver ou de refuser des demandes de réunion et de participer à des réunions. Configurez le compte d’appareil lors de la configuration OOBE (Out-of-Box Experience). Si nécessaire, vous pouvez le modifier ultérieurement (sans passer par la configuration OOBE).

Vous pouvez créer le compte à partir du Centre d’administration Microsoft 365 en combinaison avec Windows PowerShell : 

- **Créez un compte via le Centre d’administration.** Pour répondre à la configuration minimale requise, vous pouvez configurer tout ce dont vous avez besoin pour le compte directement à partir du Centre d’administration [Microsoft 365.](https://admin.microsoft.com/AdminPortal) Certaines fonctionnalités telles que le partage de tableaux blancs directement à partir de l’application tableau blanc nécessitent l’utilisation de PowerShell pour configurer ActiveSync ; voir [Activer ActiveSync si l’utilisation de l’application de messagerie est requise](#enable-activesync-if-use-of-email-app-is-required) sur cette page.

- **Créez un compte via PowerShell.** Vous pouvez utiliser des scripts PowerShell pour faciliter la création de plusieurs comptes d’appareil et configurer rapidement des fonctionnalités spécifiques, notamment :
    - Traitement du calendrier pour chaque compte d’appareil Surface Hub.
    - Réponses automatiques personnalisées aux demandes de planification.
    - Si la stratégie de boîte aux lettres ActiveSync par défaut a déjà été modifiée par une autre personne ou par un autre processus, vous devez probablement créer et affecter une nouvelle stratégie de boîte aux lettres ActiveSync.

> [!TIP]
> Vous pouvez vérifier la configuration du compte en exécutant le [script de vérification de compte ci-dessous.](#account-verification-script)

> [!NOTE]  
> Le compte d’appareil Surface Hub ne prend pas en charge les fournisseurs d’identité fédérés tiers et doit être un compte Active Directory ou Azure Active Directory standard.

## <a name="create-account-via-admin-center"></a>Créer un compte via le Centre d’administration

1. Dans le Centre d’administration Microsoft **** 365, sélectionnez Ressources et choisissez Salles **& équipement,** puis **sélectionnez + Ajouter une ressource.**

2. Fournissez un nom et une adresse de messagerie pour le compte d’appareil. Laissez les paramètres restants inchangés dans l’état par défaut.

   ![Fournir un nom et une adresse e-mail](images/sh2-account2.png)

   ![Laisser les paramètres restants inchangés dans l’état par défaut](images/sh2-account3.png)

3. Définissez le mot de passe du compte d’appareil. Pour définir le mot de passe, **sélectionnez Utilisateurs,** puis **Utilisateurs actifs.** À présent, recherchez l’utilisateur nouvellement créé pour définir le mot de passe. Veillez à ne **pas sélectionner l’option** Faire en sorte que cet utilisateur change son mot de passe lors **de sa première signature.**

   ![Définir le mot de passe du compte d’appareil](images/sh2-account4.png)

4. Affectez la salle avec une licence Office 365. Il est recommandé d’attribuer la licence **** salle de réunion Office 365, qui active automatiquement le compte pour Microsoft Teams et Skype Entreprise.

   ![Attribuer une licence Office 365](images/sh2-account5.png)


> [!NOTE]  
> Si vous utilisez Skype Entreprise, vous devez finaliser l’installation via PowerShell - Calendrier Skype Entreprise : définir le traitement automatique du calendrier [pour](#set-calendar-auto-processing-skype-for-business-only) ce compte. 

## <a name="create-account-via-powershell"></a>Créer un compte via PowerShell

 L’utilisation de PowerShell pour automatiser rapidement des tâches sur Surface Hub ne nécessite pas nécessairement une expertise PowerShell. Assurez-vous que vous avez rempli les conditions préalables à l’installation avant d’utiliser les scripts appropriés sur cette page.

### <a name="prerequisites-for-using-powershell-to-manage-surface-hub"></a>Conditions préalables à l’utilisation de PowerShell pour gérer le Surface Hub 

1. Lancez PowerShell avec des privilèges de compte élevés **(exécuter**en tant qu’administrateur) et assurez-vous que votre système est configuré pour exécuter des scripts PowerShell. Pour en savoir plus, consultez la procédure [à propos des stratégies d’exécution.](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?) 
2. [Installez le module Azure PowerShell.](https://docs.microsoft.com/powershell/azure/install-az-ps)


### <a name="connect-to-exchange-online-powershell"></a>Se connecter à Exchange Online PowerShell

```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement
Connect-ExchangeOnline -UserPrincipalName admin@contoso.com -ShowProgress $true
```

### <a name="create-mailbox"></a>Créer une boîte aux lettres

```powershell
New-Mailbox -MicrosoftOnlineServicesID 'SurfaceHub01@contoso.com' -Alias SurfaceHub01 -Name "Surface Hub 01" -Room -EnableRoomMailboxAccount $true -RoomMailboxPassword (ConvertTo-SecureString -String 'Pass@word1' -AsPlainText -Force)
```

### <a name="set-calendar-auto-processing-skype-for-business-only"></a>Définir le traitement automatique du calendrier (Skype Entreprise uniquement)

```powershell
Set-CalendarProcessing -Identity 'SurfaceHub01@contoso.com' -AutomateProcessing AutoAccept -AddOrganizerToSubject $false -AllowConflicts $false -DeleteComments $false -DeleteSubject $false -RemovePrivateProperty $false
Set-CalendarProcessing -Identity 'SurfaceHub01@contoso.com' -AddAdditionalResponse $true -AdditionalResponse "This is a Microsoft Surface Hub. Please make sure this meeting is a Microsoft Teams meeting!"
```

### <a name="enable-activesync-if-use-of-email-app-is-required"></a>Activer ActiveSync si l’utilisation de l’application de messagerie est requise

 La stratégie ActiveSync par défaut fonctionne si elle reste inchangée. Sinon, créez une stratégie et affectez-la.

```powershell
New-MobileDeviceMailboxPolicy -Name:"SurfaceHub" -PasswordEnabled:$false
#Assign Policy to Hub:
Set-CASMailbox -Identity SurfaceHub01@contoso.com -ActiveSyncMailboxPolicy "SurfaceHub"
```

### <a name="connect-to-azure-ad"></a>Se connecter à AzureAD

```powershell
Connect-AzureAD
```

### <a name="assign-a-license"></a>Attribuer une licence

```powershell
Set-AzureADUser -ObjectId 'SurfaceHub01@contoso.com' -UsageLocation US
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense 
$License.SkuId = "c7df2760-2c81-4ef7-b578-5b5392b571df" 
$Licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses 
$Licenses.AddLicenses = $License 
Set-AzureADUserLicense -ObjectId 'SurfaceHub01@contoso.com' -AssignedLicenses $Licenses
```

### <a name="check-for-available-licenses"></a>Vérifier les licences disponibles

```powershell
Get-AzureADUser -Filter "userPrincipalName eq 'SurfaceHub01@contoso.com'" |fl *
#Meeting Room Standard SKU:
6070a4c8-34c6-4937-8dfb-39bbc6397a60
```

## <a name="account-verification-script"></a>Script de vérification de compte

Après avoir créé le compte d’appareil, vous pouvez exécuter le script de vérification suivant. Ce script valide un compte d’appareil créé précédemment et produit un rapport récapitulatif. Par exemple:

``` syntax
15 tests executed
0 failures
2 warnings
15 passed
```

Les détails relatifs aux paramètres spécifiques ne s’affichent pas.

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

## <a name="learn-more"></a>Si vous souhaitez en savoir plus

- [Créer des comptes SurfaceHub2S locaux avec PowerShell](surface-hub-2s-onprem-powershell.md)