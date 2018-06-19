---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323109"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="58c51-103">Installera Azure PowerShell med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="58c51-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="58c51-104">Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="58c51-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="58c51-105">Det här är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="58c51-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="58c51-106">Läs följande artikel om du vill använda Azure PowerShell på macOS eller Linux: [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="58c51-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="58c51-107">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="58c51-107">System requirements</span></span>

<span data-ttu-id="58c51-108">Azure PowerShell-version 6.1.0 kräver version 5.0 (eller senare) av PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58c51-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="58c51-109">Information om hur du uppgraderar till PowerShell 5.0 finns i [Uppgradera befintlig Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="58c51-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="58c51-110">PowerShellGet inkluderas automatiskt som en del av PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="58c51-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="58c51-111">Installera eller uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="58c51-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="58c51-112">För installation av Azure PowerShell från PowerShell-galleriet krävs utökade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="58c51-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="58c51-113">Kör följande kommando från en utökad PowerShell-session:</span><span class="sxs-lookup"><span data-stu-id="58c51-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="58c51-114">Med det här kommandot uppdateras eventuella befintliga installationer av Azure PowerShell på datorn.</span><span class="sxs-lookup"><span data-stu-id="58c51-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="58c51-115">Om du behöver ha mer än en version installerad kan du läsa svaret på frågan [Kan jag installera flera versioner av Azure PowerShell?](#multiple-versions) i avsnittet med vanliga frågor och svar.</span><span class="sxs-lookup"><span data-stu-id="58c51-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="58c51-116">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="58c51-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="58c51-117">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="58c51-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="58c51-118">Svara Ja, eller Ja till alla om du vill fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="58c51-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="58c51-119">Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.</span><span class="sxs-lookup"><span data-stu-id="58c51-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="58c51-120">Modulen AzureRM är en sammanslagen modul för Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="58c51-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="58c51-121">När du installerar AzureRM-modulen kommer alla övriga Azure PowerShell-moduler som inte har installerats att laddas ned och installeras från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="58c51-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="58c51-122">Läs in Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="58c51-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="58c51-123">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="58c51-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="58c51-124">Du bör göra det här i en normal (icke-förhöjd) PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="58c51-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="58c51-125">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="58c51-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="58c51-126">Rapportera problem och feedback</span><span class="sxs-lookup"><span data-stu-id="58c51-126">Reporting issues and feedback</span></span>

<span data-ttu-id="58c51-127">Om du stöter på några buggar med verktyget kan du [rapportera problemet på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="58c51-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="58c51-128">Om du vill ge feedback från kommandoraden, använder du cmdleten `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="58c51-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="58c51-129">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="58c51-129">Next Steps</span></span>

<span data-ttu-id="58c51-130">Mer information om hur du använder Azure PowerShell finns i följande artiklar:</span><span class="sxs-lookup"><span data-stu-id="58c51-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="58c51-131">Kom igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58c51-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="58c51-132">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="58c51-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="58c51-133">Hur gör jag för att kontrollera vilken version av Azure PowerShell jag har?</span><span class="sxs-lookup"><span data-stu-id="58c51-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="58c51-134">Det finns stöd för flera versioner av Azure PowerShell, men vi rekommenderar att du uppgraderar till den senaste versionen så snart som möjligt.</span><span class="sxs-lookup"><span data-stu-id="58c51-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="58c51-135">Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-Module AzureRM` från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="58c51-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="58c51-136">Kan jag använda Azure PowerShell för klassiska Azure-distributioner?</span><span class="sxs-lookup"><span data-stu-id="58c51-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="58c51-137">Om du har distributioner som använder den klassiska distributionsmodellen så kan du installera Service Management-versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58c51-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="58c51-138">Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="58c51-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="58c51-139">Azure- och AzureRM-moduler delar gemensamma beroenden.</span><span class="sxs-lookup"><span data-stu-id="58c51-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="58c51-140">Om du använder både Azure- och AzureRM-moduler, bör du installera samma version av varje paket.</span><span class="sxs-lookup"><span data-stu-id="58c51-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="58c51-141"><a name="multiple-versions"/>Kan jag installera flera versioner av Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="58c51-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="58c51-142">PowerShellGet är den enda installationsmetoden som stöder installation av flera versioner.</span><span class="sxs-lookup"><span data-stu-id="58c51-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="58c51-143">Om du vill installera flera versioner kan du lägga till parametern `-RequiredVersion` till cmdleten `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="58c51-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="58c51-144">Till exempel kan du installera både version 6.1.0 och 1.2.9:</span><span class="sxs-lookup"><span data-stu-id="58c51-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="58c51-145">Endast en version av modulen kan läsas in i en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="58c51-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="58c51-146">Du måste öppna ett nytt PowerShell-fönster och använda `Import-Module` för att importera en specifik version av Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="58c51-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="58c51-147">Version 2.1.0 och 1.2.6 är de första modulversionerna som är avsedda att installeras och användas sida vid sida.</span><span class="sxs-lookup"><span data-stu-id="58c51-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="58c51-148">När du laddar en tidigare version av Azure PowerShell, laddas inkompatibla versioner av modulen **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="58c51-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="58c51-149">Det gör att cmdletarna ber dig logga in när du kör en av dem.</span><span class="sxs-lookup"><span data-stu-id="58c51-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
