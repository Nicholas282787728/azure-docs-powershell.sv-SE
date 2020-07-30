---
title: Installera Azure PowerShell på Windows med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: bd9cbdd66c1a9a623461ca8b0291ac1cb61f1e54
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177483"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="c9d77-103">Installera Azure PowerShell på Windows med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="c9d77-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="c9d77-104">I den här artikeln beskrivs stegen för att installera Azure PowerShell-modulerna för PowerShell 5.x för Windows med PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c9d77-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="c9d77-105">PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="c9d77-106">Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9d77-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="c9d77-107">Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.</span><span class="sxs-lookup"><span data-stu-id="c9d77-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9d77-108">AzureRM-modulen stöds inte för macOS eller Linux.</span><span class="sxs-lookup"><span data-stu-id="c9d77-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="c9d77-109">[Installera Az-modulen](/powershell/azure/install-az-ps) för att använda Azure PowerShell-cmdletar på dessa plattformar.</span><span class="sxs-lookup"><span data-stu-id="c9d77-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d77-110">Krav</span><span class="sxs-lookup"><span data-stu-id="c9d77-110">Requirements</span></span>

<span data-ttu-id="c9d77-111">Du behöver PowerShellGet version 1.1.2.0 eller senare för att installera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9d77-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="c9d77-112">Kör följande kommando för att kontrollera om det är tillgängligt på ditt system:</span><span class="sxs-lookup"><span data-stu-id="c9d77-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="c9d77-113">Nu bör du se utdata som ser ut ungefär så här:</span><span class="sxs-lookup"><span data-stu-id="c9d77-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="c9d77-114">Kör följande kommando om du behöver uppdatera din installation av PowerShellGet:</span><span class="sxs-lookup"><span data-stu-id="c9d77-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="c9d77-115">Följ anvisningarna i tabellen nedan för ditt system om du inte har PowerShellGet installerat.</span><span class="sxs-lookup"><span data-stu-id="c9d77-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="c9d77-116">Scenario</span><span class="sxs-lookup"><span data-stu-id="c9d77-116">Scenario</span></span>|<span data-ttu-id="c9d77-117">Installationsinstruktioner</span><span class="sxs-lookup"><span data-stu-id="c9d77-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="c9d77-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c9d77-118">Windows 10</span></span><br/><span data-ttu-id="c9d77-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9d77-119">Windows Server 2016</span></span>|<span data-ttu-id="c9d77-120">Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet</span><span class="sxs-lookup"><span data-stu-id="c9d77-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="c9d77-121">Uppgradera till PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="c9d77-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="c9d77-122">Installera den senaste versionen av WMF</span><span class="sxs-lookup"><span data-stu-id="c9d77-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="c9d77-123">Kör följande kommando:</span><span class="sxs-lookup"><span data-stu-id="c9d77-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="c9d77-124">Windows med PowerShell 3 eller PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="c9d77-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="c9d77-125"><il>[Hämta PackageManagement-modulerna](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="c9d77-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="c9d77-126">Kör följande kommando:</span><span class="sxs-lookup"><span data-stu-id="c9d77-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="c9d77-127">För att kunna använda PowerShellGet, krävs en körningsprincip som låter dig köra skript.</span><span class="sxs-lookup"><span data-stu-id="c9d77-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="c9d77-128">Mer information om PowerShell-körningsprincipen finns i [Om körningsprinciper](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="c9d77-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="c9d77-129">Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c9d77-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="c9d77-130">Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core.</span><span class="sxs-lookup"><span data-stu-id="c9d77-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="c9d77-131">Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="c9d77-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="c9d77-132">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="c9d77-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="c9d77-133">Du behöver ha utökade behörigheter för att installera moduler från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="c9d77-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="c9d77-134">Kör följande kommando i en upphöjd session för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c9d77-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="c9d77-135">Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.</span><span class="sxs-lookup"><span data-stu-id="c9d77-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="c9d77-136">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c9d77-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c9d77-137">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="c9d77-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c9d77-138">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="c9d77-139">Modulen `AzureRM` är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c9d77-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c9d77-140">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="c9d77-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="c9d77-141">Logga in</span><span class="sxs-lookup"><span data-stu-id="c9d77-141">Sign in</span></span>

<span data-ttu-id="c9d77-142">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9d77-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="c9d77-143">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="c9d77-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c9d77-144">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="c9d77-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="c9d77-145">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="c9d77-146">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="c9d77-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="c9d77-147">Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="c9d77-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="c9d77-148">Det här kommandot avinstallerar __inte__ tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="c9d77-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="c9d77-149">Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.</span><span class="sxs-lookup"><span data-stu-id="c9d77-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="c9d77-150">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c9d77-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="c9d77-151">Det är möjligt att installera flera versioner av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9d77-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="c9d77-152">Du kan behöva mer än en version om du arbetar med lokala Azure Stack-resurser, kör en äldre version av Windows så att du inte kan uppdatera till PowerShell 5.0 eller använder den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="c9d77-153">Ange argumentet `-RequiredVersion` när du installerar för att installera en äldre version.</span><span class="sxs-lookup"><span data-stu-id="c9d77-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="c9d77-154">När du läser in Azure PowerShell-modulen läses den senaste versionen in som standard.</span><span class="sxs-lookup"><span data-stu-id="c9d77-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="c9d77-155">Ange argumentet `-RequiredVersion` för att läsa in en annan version.</span><span class="sxs-lookup"><span data-stu-id="c9d77-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="c9d77-156">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="c9d77-156">Provide feedback</span></span>

<span data-ttu-id="c9d77-157">Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c9d77-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="c9d77-158">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="c9d77-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c9d77-159">Efterföljande moment</span><span class="sxs-lookup"><span data-stu-id="c9d77-159">Next Steps</span></span>

<span data-ttu-id="c9d77-160">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.</span><span class="sxs-lookup"><span data-stu-id="c9d77-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
