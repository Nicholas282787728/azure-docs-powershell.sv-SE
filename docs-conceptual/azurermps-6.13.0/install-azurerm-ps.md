---
title: Installera Azure PowerShell på Windows med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 198c9476b06c818fd3f7cb5ac3ac465497cac9cf
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216593"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="fc9f3-103">Installera Azure PowerShell på Windows med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fc9f3-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="fc9f3-104">Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="fc9f3-105">PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="fc9f3-106">Anvisningar för hur du installerar Azure PowerShell på andra plattformar finns i [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="fc9f3-107">Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="fc9f3-108">Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a><span data-ttu-id="fc9f3-109">Krav</span><span class="sxs-lookup"><span data-stu-id="fc9f3-109">Requirements</span></span>

<span data-ttu-id="fc9f3-110">Från och med PowerShell version 6.0 kräver Azure PowerShell version 5.0.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="fc9f3-111">Kör följande kommando för att kontrollera vilken version av PowerShell som körs på din dator:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="fc9f3-112">Läs informationen om att [uppgradera befintliga Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) om du har en inaktuell version.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc9f3-113">Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="fc9f3-114">Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="fc9f3-115">Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="fc9f3-116">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="fc9f3-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="fc9f3-117">Du behöver ha utökade behörigheter för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="fc9f3-118">Kör följande kommando i en upphöjd session för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="fc9f3-119">Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="fc9f3-120">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fc9f3-121">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="fc9f3-122">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="fc9f3-123">Modulen `AzureRM` är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="fc9f3-124">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="fc9f3-125">Logga in</span><span class="sxs-lookup"><span data-stu-id="fc9f3-125">Sign in</span></span>

<span data-ttu-id="fc9f3-126">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-126">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="fc9f3-127">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-127">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="fc9f3-128">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-128">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="fc9f3-129">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="fc9f3-130">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-130">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="fc9f3-131">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="fc9f3-131">Update the Azure PowerShell module</span></span>

<span data-ttu-id="fc9f3-132">Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-132">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="fc9f3-133">Det här kommandot avinstallerar __inte__ tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-133">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="fc9f3-134">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-134">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="fc9f3-135">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc9f3-135">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="fc9f3-136">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-136">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="fc9f3-137">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="fc9f3-137">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name AzureRM -ListAvailable | select Name,Version
```

<span data-ttu-id="fc9f3-138">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-138">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="fc9f3-139">Du kan behöva fler än en version om du arbetar med lokala Azure Stack-resurser, kör en äldre version av Windows eller använder den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-139">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="fc9f3-140">Ange argumentet `-RequiredVersion` när du installerar för att installera en äldre version.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-140">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="fc9f3-141">När du läser in Azure PowerShell-modulen läses den senaste versionen in som standard.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-141">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="fc9f3-142">Ange argumentet `-RequiredVersion` för att läsa in en annan version.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-142">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="fc9f3-143">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="fc9f3-143">Provide feedback</span></span>

<span data-ttu-id="fc9f3-144">Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="fc9f3-145">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="fc9f3-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fc9f3-146">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="fc9f3-146">Next Steps</span></span>

<span data-ttu-id="fc9f3-147">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
