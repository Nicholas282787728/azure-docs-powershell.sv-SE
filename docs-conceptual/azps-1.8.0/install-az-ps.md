---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365748"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="50cad-103">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="50cad-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="50cad-104">Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="50cad-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="50cad-105">De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.</span><span class="sxs-lookup"><span data-stu-id="50cad-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="50cad-106">För Az-modulen kan för närvarande inga andra installationsmetoder användas.</span><span class="sxs-lookup"><span data-stu-id="50cad-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cad-107">Krav</span><span class="sxs-lookup"><span data-stu-id="50cad-107">Requirements</span></span>

<span data-ttu-id="50cad-108">Azure PowerShell fungerar med PowerShell 5.1 och senare i Windows och med PowerShell Core 6.x och senare på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="50cad-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="50cad-109">Om du är osäker på om du har PowerShell, eller macOS eller Linux, [installerar du senaste versionen av PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="50cad-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="50cad-110">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="50cad-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="50cad-111">Köra Azure PowerShell på PowerShell 5.1 på Windows:</span><span class="sxs-lookup"><span data-stu-id="50cad-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="50cad-112">Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="50cad-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="50cad-113">Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.</span><span class="sxs-lookup"><span data-stu-id="50cad-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="50cad-114">Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="50cad-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="50cad-115">Det finns inga ytterligare krav för Azure PowerShell när du använder PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="50cad-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="50cad-116">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="50cad-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="50cad-117">Du kan ha både modulen AzureRM och modulen Az installerade samtidigt.</span><span class="sxs-lookup"><span data-stu-id="50cad-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="50cad-118">Om du har båda modulerna installerade __ska du inte aktivera__ -alias.</span><span class="sxs-lookup"><span data-stu-id="50cad-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="50cad-119">Om du aktiverar alias skapas konflikter mellan AzureRM-cmdletar och Az-kommandoalias, och detta kan orsaka oväntat beteende.</span><span class="sxs-lookup"><span data-stu-id="50cad-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="50cad-120">Vi rekommenderar att du avinstallerar AzureRM-modulen innan du installerar Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="50cad-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="50cad-121">Du kan avinstallera AzureRM eller aktivera alias när som helst.</span><span class="sxs-lookup"><span data-stu-id="50cad-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="50cad-122">Information om AzureRM-kommandoalias finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="50cad-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="50cad-123">Anvisningar om hur du avinstallerar finns i [Avinstallera AzureRM-modulen](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="50cad-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="50cad-124">Om du vill installera moduler med globalt omfång behöver du ha utökade privilegier för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="50cad-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="50cad-125">Du installerar Azure PowerShell genom att köra följande kommando i en upphöjd session (”Kör som administratör” på Windows eller med superanvändarprivilegier på macOS eller Linux):</span><span class="sxs-lookup"><span data-stu-id="50cad-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="50cad-126">Om du inte har åtkomst till administratörsprivilegier kan du installera för den aktuella användaren genom att lägga till argumentet `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="50cad-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="50cad-127">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="50cad-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="50cad-128">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="50cad-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="50cad-129">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="50cad-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="50cad-130">Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="50cad-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="50cad-131">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="50cad-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="50cad-132">Logga in</span><span class="sxs-lookup"><span data-stu-id="50cad-132">Sign in</span></span>

<span data-ttu-id="50cad-133">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="50cad-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="50cad-134">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="50cad-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="50cad-135">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="50cad-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="50cad-136">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="50cad-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="50cad-137">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="50cad-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="50cad-138">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="50cad-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="50cad-139">På grund av hur Az-modulen är paketerad uppdaterar kommandot [Update-Module](/powershell/module/powershellget/update-module) inte installationen på rätt sätt.</span><span class="sxs-lookup"><span data-stu-id="50cad-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="50cad-140">Az är tekniskt sett en metamodul. Den omfattar alla undermoduler som innehåller cmdletar för att interagera med Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="50cad-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="50cad-141">Det innebär att om du vill uppdatera Azure PowerShell-modulen behöver du __installera om__, snarare än att bara __uppdatera__.</span><span class="sxs-lookup"><span data-stu-id="50cad-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="50cad-142">Det gör du på samma sätt som när du installerar, men du kan behöva lägga till argumentet `-Force`:</span><span class="sxs-lookup"><span data-stu-id="50cad-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="50cad-143">Det här kan skriva över installerade moduler, men du kan fortfarande ha äldre versioner kvar på datorn.</span><span class="sxs-lookup"><span data-stu-id="50cad-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="50cad-144">Om du vill ta bort äldre versioner av Azure PowerShell från ditt system läser du [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="50cad-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="50cad-145">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="50cad-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="50cad-146">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50cad-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="50cad-147">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="50cad-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="50cad-148">Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50cad-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="50cad-149">Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="50cad-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="50cad-150">Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.</span><span class="sxs-lookup"><span data-stu-id="50cad-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="50cad-151">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="50cad-151">Provide feedback</span></span>

<span data-ttu-id="50cad-152">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="50cad-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="50cad-153">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="50cad-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="50cad-154">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="50cad-154">Next Steps</span></span>

<span data-ttu-id="50cad-155">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="50cad-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="50cad-156">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="50cad-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
