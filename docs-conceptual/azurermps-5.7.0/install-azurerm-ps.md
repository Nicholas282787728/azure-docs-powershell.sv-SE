---
title: Installera Azure PowerShell på Windows med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: a868a62bd7bb2f39775a3b7878e2c8484c50438d
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274185"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="9afb1-103">Installera Azure PowerShell på Windows med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="9afb1-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="9afb1-104">Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9afb1-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="9afb1-105">PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="9afb1-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="9afb1-106">Anvisningar för hur du installerar Azure PowerShell på andra plattformar finns i [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="9afb1-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="9afb1-107">Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9afb1-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="9afb1-108">Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.</span><span class="sxs-lookup"><span data-stu-id="9afb1-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="9afb1-109">Krav</span><span class="sxs-lookup"><span data-stu-id="9afb1-109">Requirements</span></span>

<span data-ttu-id="9afb1-110">Du behöver PowerShellGet version 1.1.2.0 eller senare för att installera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9afb1-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="9afb1-111">Kör följande kommando för att kontrollera om det är tillgängligt på ditt system:</span><span class="sxs-lookup"><span data-stu-id="9afb1-111">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="9afb1-112">Nu bör du se utdata som ser ut ungefär så här:</span><span class="sxs-lookup"><span data-stu-id="9afb1-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="9afb1-113">Kör följande kommando om du behöver uppdatera din installation av PowerShellGet:</span><span class="sxs-lookup"><span data-stu-id="9afb1-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="9afb1-114">Följ anvisningarna i tabellen nedan för ditt system om du inte har PowerShellGet installerat.</span><span class="sxs-lookup"><span data-stu-id="9afb1-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="9afb1-115">Scenario</span><span class="sxs-lookup"><span data-stu-id="9afb1-115">Scenario</span></span>|<span data-ttu-id="9afb1-116">Installationsinstruktioner</span><span class="sxs-lookup"><span data-stu-id="9afb1-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="9afb1-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9afb1-117">Windows 10</span></span><br/><span data-ttu-id="9afb1-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9afb1-118">Windows Server 2016</span></span>|<span data-ttu-id="9afb1-119">Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet</span><span class="sxs-lookup"><span data-stu-id="9afb1-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="9afb1-120">Uppgradera till PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="9afb1-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="9afb1-121">Installera den senaste versionen av WMF</span><span class="sxs-lookup"><span data-stu-id="9afb1-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="9afb1-122">Kör följande kommando:</span><span class="sxs-lookup"><span data-stu-id="9afb1-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="9afb1-123">Windows med PowerShell 3 eller PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="9afb1-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="9afb1-124"><il>[Hämta PackageManagement-modulerna](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="9afb1-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="9afb1-125">Kör följande kommando:</span><span class="sxs-lookup"><span data-stu-id="9afb1-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="9afb1-126">För att kunna använda PowerShellGet, krävs en körningsprincip som låter dig köra skript.</span><span class="sxs-lookup"><span data-stu-id="9afb1-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="9afb1-127">Mer information om PowerShell-körningsprincipen finns i [Om körningsprinciper](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="9afb1-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="9afb1-128">Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9afb1-128">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="9afb1-129">Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9afb1-129">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="9afb1-130">Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="9afb1-130">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="9afb1-131">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="9afb1-131">Install the Azure PowerShell module</span></span>

<span data-ttu-id="9afb1-132">Du behöver ha utökade behörigheter för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="9afb1-132">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="9afb1-133">Kör följande kommando i en upphöjd session för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9afb1-133">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="9afb1-134">Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.</span><span class="sxs-lookup"><span data-stu-id="9afb1-134">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="9afb1-135">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9afb1-135">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9afb1-136">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="9afb1-136">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9afb1-137">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="9afb1-137">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="9afb1-138">Modulen `AzureRM` är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="9afb1-138">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9afb1-139">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="9afb1-139">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="9afb1-140">Logga in</span><span class="sxs-lookup"><span data-stu-id="9afb1-140">Sign in</span></span>

<span data-ttu-id="9afb1-141">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9afb1-141">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="9afb1-142">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="9afb1-142">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9afb1-143">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="9afb1-143">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="9afb1-144">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9afb1-144">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="9afb1-145">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="9afb1-145">Update the Azure PowerShell module</span></span>

<span data-ttu-id="9afb1-146">Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="9afb1-146">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="9afb1-147">Det här kommandot avinstallerar __inte__ tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="9afb1-147">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="9afb1-148">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.</span><span class="sxs-lookup"><span data-stu-id="9afb1-148">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="9afb1-149">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9afb1-149">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="9afb1-150">Det är möjligt att installera flera versioner av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9afb1-150">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="9afb1-151">Du kan behöva mer än en version om du arbetar med lokala Azure Stack-resurser, kör en äldre version av Windows så att du inte kan uppdatera till PowerShell 5.0 eller använder den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="9afb1-151">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="9afb1-152">Ange argumentet `-RequiredVersion` när du installerar för att installera en äldre version.</span><span class="sxs-lookup"><span data-stu-id="9afb1-152">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="9afb1-153">När du läser in Azure PowerShell-modulen läses den senaste versionen in som standard.</span><span class="sxs-lookup"><span data-stu-id="9afb1-153">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="9afb1-154">Ange argumentet `-RequiredVersion` för att läsa in en annan version.</span><span class="sxs-lookup"><span data-stu-id="9afb1-154">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="9afb1-155">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="9afb1-155">Provide feedback</span></span>

<span data-ttu-id="9afb1-156">Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9afb1-156">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="9afb1-157">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="9afb1-157">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9afb1-158">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="9afb1-158">Next Steps</span></span>

<span data-ttu-id="9afb1-159">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.</span><span class="sxs-lookup"><span data-stu-id="9afb1-159">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>