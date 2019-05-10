---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048554"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="995cc-103">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="995cc-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="995cc-104">Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="995cc-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="995cc-105">De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.</span><span class="sxs-lookup"><span data-stu-id="995cc-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="995cc-106">För Az-modulen kan för närvarande inga andra installationsmetoder användas.</span><span class="sxs-lookup"><span data-stu-id="995cc-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="995cc-107">Krav</span><span class="sxs-lookup"><span data-stu-id="995cc-107">Requirements</span></span>

<span data-ttu-id="995cc-108">Azure PowerShell fungerar med PowerShell 5.1 eller senare i Windows, eller med PowerShell 6 på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="995cc-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="995cc-109">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="995cc-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="995cc-110">Om du har en inaktuell version eller behöver installera PowerShell kan du läsa [Installation av olika versioner av PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="995cc-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="995cc-111">Installationsinformation för din plattform är länkad från den sidan.</span><span class="sxs-lookup"><span data-stu-id="995cc-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="995cc-112">Om du använder PowerShell 5 i Windows måste du även ha .NET Framework 4.7.2 installerat.</span><span class="sxs-lookup"><span data-stu-id="995cc-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="995cc-113">Anvisningar för hur du uppdaterar eller installerar en ny version av .NET Framework finns i [installationsguiden till .NET Framework](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="995cc-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="995cc-114">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="995cc-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="995cc-115">Du kan ha både modulen AzureRM och modulen Az installerade samtidigt.</span><span class="sxs-lookup"><span data-stu-id="995cc-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="995cc-116">Om du har båda modulerna installerade __ska du inte aktivera__ -alias.</span><span class="sxs-lookup"><span data-stu-id="995cc-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="995cc-117">Om du aktiverar alias skapas konflikter mellan AzureRM-cmdletar och Az-kommandoalias, och detta kan orsaka oväntat beteende.</span><span class="sxs-lookup"><span data-stu-id="995cc-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="995cc-118">Vi rekommenderar att du avinstallerar AzureRM-modulen innan du installerar Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="995cc-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="995cc-119">Du kan avinstallera AzureRM eller aktivera alias när som helst.</span><span class="sxs-lookup"><span data-stu-id="995cc-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="995cc-120">Information om AzureRM-kommandoalias finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="995cc-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="995cc-121">Anvisningar om hur du avinstallerar finns i [Avinstallera AzureRM-modulen](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="995cc-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="995cc-122">Om du vill installera moduler med globalt omfång behöver du ha utökade privilegier för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="995cc-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="995cc-123">Du installerar Azure PowerShell genom att köra följande kommando i en upphöjd session (”Kör som administratör” på Windows eller med superanvändarprivilegier på macOS eller Linux):</span><span class="sxs-lookup"><span data-stu-id="995cc-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="995cc-124">Om du inte har åtkomst till administratörsprivilegier kan du installera för den aktuella användaren genom att lägga till argumentet `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="995cc-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="995cc-125">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="995cc-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="995cc-126">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="995cc-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="995cc-127">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="995cc-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="995cc-128">Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="995cc-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="995cc-129">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="995cc-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="995cc-130">Logga in</span><span class="sxs-lookup"><span data-stu-id="995cc-130">Sign in</span></span>

<span data-ttu-id="995cc-131">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="995cc-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="995cc-132">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="995cc-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="995cc-133">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="995cc-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="995cc-134">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="995cc-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="995cc-135">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="995cc-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="995cc-136">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="995cc-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="995cc-137">Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="995cc-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="995cc-138">Det här kommandot avinstallerar __inte__ äldre versioner.</span><span class="sxs-lookup"><span data-stu-id="995cc-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="995cc-139">Om du vill ta bort äldre versioner av Azure PowerShell från ditt system läser du [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="995cc-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="995cc-140">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="995cc-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="995cc-141">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="995cc-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="995cc-142">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="995cc-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="995cc-143">Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="995cc-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="995cc-144">Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="995cc-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="995cc-145">Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.</span><span class="sxs-lookup"><span data-stu-id="995cc-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="995cc-146">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="995cc-146">Provide feedback</span></span>

<span data-ttu-id="995cc-147">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="995cc-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="995cc-148">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="995cc-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="995cc-149">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="995cc-149">Next Steps</span></span>

<span data-ttu-id="995cc-150">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="995cc-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="995cc-151">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="995cc-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
