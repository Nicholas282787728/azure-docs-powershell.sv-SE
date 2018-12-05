---
title: Installera Azure PowerShell ”Az” med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet på Windows, macOS och Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588187"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="76321-103">Installera modulen Azure PowerShell ”Az”</span><span class="sxs-lookup"><span data-stu-id="76321-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="76321-104">Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="76321-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="76321-105">De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.</span><span class="sxs-lookup"><span data-stu-id="76321-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="76321-106">För förhandsversionen av Az stöds inga andra installationsmetoder.</span><span class="sxs-lookup"><span data-stu-id="76321-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="76321-107">Krav</span><span class="sxs-lookup"><span data-stu-id="76321-107">Requirements</span></span>

<span data-ttu-id="76321-108">Azure PowerShell fungerar med PowerShell 5.x på Windows eller PowerShell 6.x på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="76321-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="76321-109">Kör följande kommando för att kontrollera vilken version av PowerShell som körs på din dator:</span><span class="sxs-lookup"><span data-stu-id="76321-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="76321-110">Om du har en inaktuell version eller behöver installera PowerShell kan du läsa [Installation av olika versioner av PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="76321-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="76321-111">Installationsinformation för din plattform är länkad från den sidan.</span><span class="sxs-lookup"><span data-stu-id="76321-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="76321-112">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="76321-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="76321-113">Du kan ha både modulen `AzureRM` och modulen `Az` installerade samtidigt.</span><span class="sxs-lookup"><span data-stu-id="76321-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="76321-114">Om du har båda modulerna installerade __ska du inte aktivera__ -alias.</span><span class="sxs-lookup"><span data-stu-id="76321-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="76321-115">Om du aktiverar alias skapas konflikter mellan `AzureRM`-cmdletar och `Az`-kommandoalias och detta kan orsaka oväntat beteende.</span><span class="sxs-lookup"><span data-stu-id="76321-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="76321-116">Vi rekommenderar att du avinstallerar `AzureRM` innan du installerar modulen `Az`.</span><span class="sxs-lookup"><span data-stu-id="76321-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="76321-117">Du kan alltid avinstallera `AzureRM` eller aktivera alias när som helst.</span><span class="sxs-lookup"><span data-stu-id="76321-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="76321-118">Anvisningar om hur du avinstallerar finns i [Avinstallera Azure PowerShell-modulen (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="76321-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="76321-119">Om du vill installera moduler med globalt omfång behöver du ha utökade privilegier för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="76321-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="76321-120">Du installerar Azure PowerShell genom att köra följande kommando i en upphöjd session (”Kör som administratör” på Windows eller med superanvändarprivilegier på macOS eller Linux):</span><span class="sxs-lookup"><span data-stu-id="76321-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="76321-121">Om du inte har åtkomst till administratörsprivilegier kan du installera för den aktuella användaren genom att lägga till argumentet `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="76321-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="76321-122">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="76321-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="76321-123">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="76321-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="76321-124">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="76321-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="76321-125">Modulen `Az` är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="76321-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="76321-126">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="76321-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="76321-127">Logga in</span><span class="sxs-lookup"><span data-stu-id="76321-127">Sign in</span></span>

<span data-ttu-id="76321-128">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="76321-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="76321-129">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="76321-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="76321-130">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="76321-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="76321-131">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="76321-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="76321-132">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="76321-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="76321-133">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="76321-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="76321-134">Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="76321-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="76321-135">Det här kommandot avinstallerar __inte__ tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="76321-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="76321-136">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.</span><span class="sxs-lookup"><span data-stu-id="76321-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="76321-137">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76321-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="76321-138">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76321-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="76321-139">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="76321-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="76321-140">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76321-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="76321-141">Du kan läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion` med `Install-Module` eller `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="76321-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="76321-142">Om du har flera versioner av modulen installerade läses den senaste versionen in som standard.</span><span class="sxs-lookup"><span data-stu-id="76321-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="76321-143">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="76321-143">Provide feedback</span></span>

<span data-ttu-id="76321-144">Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="76321-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="76321-145">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="76321-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="76321-146">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="76321-146">Next Steps</span></span>

<span data-ttu-id="76321-147">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.</span><span class="sxs-lookup"><span data-stu-id="76321-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
