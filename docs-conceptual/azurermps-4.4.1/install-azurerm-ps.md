---
title: Installera och konfigurera Azure PowerShell | Microsoft Docs
description: Installera och konfigurera Azure PowerShell för första gången.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3f4b05352ef5e5c7f32495d002a78aadd3e056e1
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523299"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="07164-103">Installera Azure PowerShell på Windows med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="07164-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="07164-104">I den här artikeln beskrivs stegen för att installera Azure PowerShell-modulerna för PowerShell 5.x för Windows med PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="07164-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="07164-105">PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="07164-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="07164-106">Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07164-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="07164-107">Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.</span><span class="sxs-lookup"><span data-stu-id="07164-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07164-108">AzureRM-modulen stöds inte för macOS eller Linux.</span><span class="sxs-lookup"><span data-stu-id="07164-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="07164-109">[Installera Az-modulen](/powershell/azure/install-az-ps) för att använda Azure PowerShell-cmdletar på dessa plattformar.</span><span class="sxs-lookup"><span data-stu-id="07164-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="07164-110">Steg 1: Installera PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="07164-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="07164-111">Du måste ha modulen PowerShellGet för att kunna installera objekt från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="07164-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="07164-112">Kontrollera att du har rätt version av PowerShellGet och att datorn uppfyller övriga systemkrav.</span><span class="sxs-lookup"><span data-stu-id="07164-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="07164-113">Kör följande kommando för att se om du har PowerShellGet installerat på datorn.</span><span class="sxs-lookup"><span data-stu-id="07164-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="07164-114">Nu bör du se utdata som ser ut ungefär så här:</span><span class="sxs-lookup"><span data-stu-id="07164-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="07164-115">Du behöver PowerShellGet version 1.1.2.0 eller senare.</span><span class="sxs-lookup"><span data-stu-id="07164-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="07164-116">Om du vill uppdatera PowerShellGet använder du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="07164-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="07164-117">Om du inte har installerat PowerShellGet kan du läsa avsnittet [Hämta PowerShellGet](#how-to-get-powershellget) i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="07164-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="07164-118">För att kunna använda PowerShellGet, krävs en körningsprincip som låter dig köra skript.</span><span class="sxs-lookup"><span data-stu-id="07164-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="07164-119">Mer information om PowerShell-körningsprincipen finns i [Om körningsprinciper](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="07164-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="07164-120">Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="07164-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="07164-121">Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core.</span><span class="sxs-lookup"><span data-stu-id="07164-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="07164-122">Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="07164-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="07164-123">Steg 2: Installera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07164-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="07164-124">För installation av Azure PowerShell från PowerShell-galleriet krävs utökade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="07164-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="07164-125">Kör följande kommando från en utökad PowerShell-session:</span><span class="sxs-lookup"><span data-stu-id="07164-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="07164-126">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="07164-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="07164-127">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="07164-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="07164-128">Svara Ja, eller Ja till alla om du vill fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="07164-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="07164-129">Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.</span><span class="sxs-lookup"><span data-stu-id="07164-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="07164-130">Modulen AzureRM är en sammanslagen modul för Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="07164-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="07164-131">När du installerar AzureRM-modulen, kommer alla övriga Azure PowerShell-moduler som inte har installerats att laddas ner och installeras från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="07164-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="07164-132">Om du har en tidigare version av Azure PowerShell installerad så kan du få ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="07164-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="07164-133">För att lösa problemet kan du se avsnittet [uppdatera till en ny version av Azure PowerShell](#update-azps) i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="07164-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="07164-134">Steg 3: Läs in AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="07164-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="07164-135">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="07164-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="07164-136">Du bör göra det här i en normal (icke-förhöjd) PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="07164-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="07164-137">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="07164-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="07164-138">Efterföljande moment</span><span class="sxs-lookup"><span data-stu-id="07164-138">Next Steps</span></span>

<span data-ttu-id="07164-139">Mer information om hur du använder Azure PowerShell finns i följande artiklar:</span><span class="sxs-lookup"><span data-stu-id="07164-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="07164-140">Kom igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07164-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="07164-141">Rapportera problem och feedback</span><span class="sxs-lookup"><span data-stu-id="07164-141">Reporting issues and feedback</span></span>

<span data-ttu-id="07164-142">Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-powershell/issues)-delen av vårt GitHub-repo.</span><span class="sxs-lookup"><span data-stu-id="07164-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="07164-143">Om du vill ge feedback från kommandoraden, använder du cmdleten `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="07164-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="07164-144">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="07164-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="07164-145">Hämta PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="07164-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="07164-146">OS-version</span><span class="sxs-lookup"><span data-stu-id="07164-146">OS Version</span></span>|<span data-ttu-id="07164-147">Installationsinstruktioner</span><span class="sxs-lookup"><span data-stu-id="07164-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="07164-148">Jag har Windows 10 eller Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="07164-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="07164-149">Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet</span><span class="sxs-lookup"><span data-stu-id="07164-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="07164-150">Jag vill uppgradera till PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="07164-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="07164-151">Installera den senaste versionen av WMF</span><span class="sxs-lookup"><span data-stu-id="07164-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="07164-152">Kontrollera Azure PowerShell-versionen</span><span class="sxs-lookup"><span data-stu-id="07164-152">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="07164-153">Det finns stöd för flera versioner av Azure PowerShell, men vi rekommenderar att du uppgraderar till den senaste versionen så snart som möjligt.</span><span class="sxs-lookup"><span data-stu-id="07164-153">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="07164-154">Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-InstalledModule AzureRM` från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="07164-154">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="07164-155">Stöd för klassiska distributionsmetoder</span><span class="sxs-lookup"><span data-stu-id="07164-155">Support for classic deployment methods</span></span>

<span data-ttu-id="07164-156">Om du har distributioner som använder den klassiska distributionsmodellen så kan du installera Service Management-versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07164-156">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="07164-157">Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="07164-157">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="07164-158">Azure- och AzureRM-moduler delar gemensamma beroenden.</span><span class="sxs-lookup"><span data-stu-id="07164-158">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="07164-159">Om du använder både Azure- och AzureRM-moduler, bör du installera samma version av varje paket.</span><span class="sxs-lookup"><span data-stu-id="07164-159">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="07164-160">Uppdatera till en ny version av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07164-160">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="07164-161">Om du har en tidigare version av Azure PowerShell installerad som innehåller tjänsthanteringsmodulen, kan följande felmeddelande komma upp:</span><span class="sxs-lookup"><span data-stu-id="07164-161">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="07164-162">Precis som felmeddelandet säger så behöver du använda parametern -AllowClobber för att installera modulen.</span><span class="sxs-lookup"><span data-stu-id="07164-162">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="07164-163">Ange följande kommando:</span><span class="sxs-lookup"><span data-stu-id="07164-163">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="07164-164">Mer information finns i hjälpavsnittet för [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="07164-164">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="07164-165">Installera modulversioner sida vid sida</span><span class="sxs-lookup"><span data-stu-id="07164-165">Installing module versions side by side</span></span>

<span data-ttu-id="07164-166">PowerShellGet är den enda installationsmetoden som stöder installation av flera versioner.</span><span class="sxs-lookup"><span data-stu-id="07164-166">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="07164-167">Du kan till exempel ha skript som är skrivna med en tidigare version av Azure PowerShell som du inte har tid eller resurser att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="07164-167">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="07164-168">Följande kommandon visar hur du installerar flera versioner av Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07164-168">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="07164-169">Endast en version av modulen kan läsas in i en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="07164-169">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="07164-170">Du måste öppna ett nytt PowerShell-fönster och använda `Import-Module` för att importera en specifik version av AzureRM-cmdletarna:</span><span class="sxs-lookup"><span data-stu-id="07164-170">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="07164-171">Version 2.1.0 och 1.2.6 är de första modulversionerna som är avsedda att installeras och användas sida vid sida.</span><span class="sxs-lookup"><span data-stu-id="07164-171">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="07164-172">När du laddar en tidigare version av Azure PowerShell, laddas inkompatibla versioner av modulen **AzureRM.Profile** .</span><span class="sxs-lookup"><span data-stu-id="07164-172">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="07164-173">Det gör att cmdletarna ber dig logga in när du kör en av dem.</span><span class="sxs-lookup"><span data-stu-id="07164-173">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="07164-174">Andra installationsmetoder</span><span class="sxs-lookup"><span data-stu-id="07164-174">Other installation methods</span></span>

<span data-ttu-id="07164-175">Information om hur du installerar med hjälp av installationsprogrammet för webbplattform eller MSI-paketet finns [Andra installationsmetoder](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="07164-175">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
