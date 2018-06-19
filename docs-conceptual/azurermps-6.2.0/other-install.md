---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323330"
---
# <a name="other-installation-methods"></a><span data-ttu-id="f64e3-103">Andra installationsmetoder</span><span class="sxs-lookup"><span data-stu-id="f64e3-103">Other installation methods</span></span>

<span data-ttu-id="f64e3-104">Den här artikeln förklarar hur du installerar Azure PowerShell med hjälp av en hanterad tjänstidentitet eller installationsprogrammet för webbplattformen (WebPI).</span><span class="sxs-lookup"><span data-stu-id="f64e3-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="f64e3-105">Du kan även köra Azure PowerShell från en Docker-behållare.</span><span class="sxs-lookup"><span data-stu-id="f64e3-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="f64e3-106">Använd endast dessa installationsmetoder om de är nödvändiga för ditt system.</span><span class="sxs-lookup"><span data-stu-id="f64e3-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="f64e3-107">Det kanoniska sättet att installera Azure PowerShell är med PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f64e3-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="f64e3-108">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f64e3-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="f64e3-109">Information om hur du installerar i Linux- eller macOS-miljöer finns i [Installera Azure PowerShell på macOS eller Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="f64e3-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="f64e3-110">Installera eller uppdatera på Windows med hjälp av installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="f64e3-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="f64e3-111">Att installera den senaste versionen av Azure PowerShell från WebPI går till på samma sätt som det gjorde för tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="f64e3-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="f64e3-112">Hämta [Azure PowerShell WebPI-paketet](http://aka.ms/webpi-azps) och starta installationen.</span><span class="sxs-lookup"><span data-stu-id="f64e3-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="f64e3-113">Om du tidigare har installerat Azure-moduler från PowerShell-galleriet så kommer installationsprogrammet automatiskt att ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="f64e3-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="f64e3-114">Detta förenklar din miljö genom att se till att endast en version av Azure PowerShell är installerad.</span><span class="sxs-lookup"><span data-stu-id="f64e3-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="f64e3-115">Det finns dock scenarier där du kan behöva flera versioner installerade på samma gång.</span><span class="sxs-lookup"><span data-stu-id="f64e3-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="f64e3-116">PowerShell-galleriets moduler installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="f64e3-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="f64e3-117">WebPI-installationsprogrammet däremot installerar Azure moduler i `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="f64e3-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="f64e3-118">Om ett fel inträffar under installationen kan du ta bort `Azure*`-mapparna manuellt i din `$env:ProgramFiles\WindowsPowerShell\Modules`-mapp och försöka installera igen.</span><span class="sxs-lookup"><span data-stu-id="f64e3-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="f64e3-119">När installationen är färdig bör din `$env:PSModulePath`-inställning inkludera de kataloger som innehåller Azure PowerShell-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="f64e3-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f64e3-120">Följande kommando kan användas för att kontrollera att Azure PowerShell är korrekt installerat:</span><span class="sxs-lookup"><span data-stu-id="f64e3-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="f64e3-121">Det finns ett känt problem som kan uppstå när du installerar från WebPI.</span><span class="sxs-lookup"><span data-stu-id="f64e3-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="f64e3-122">Om datorn kräver en omstart på grund av systemuppdateringar eller andra installationer kan det göra att uppdateringarna för `$env:PSModulePath` inte inkluderar sökvägen där Azure PowerShell är installerat.</span><span class="sxs-lookup"><span data-stu-id="f64e3-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="f64e3-123">När du försöker läsa in eller köra cmdletar efter installationen kan du få följande felmeddelande:</span><span class="sxs-lookup"><span data-stu-id="f64e3-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="f64e3-124">Det här felet kan korrigeras genom att starta om datorn eller importera modulen med den fullständigt kvalificerade sökvägen.</span><span class="sxs-lookup"><span data-stu-id="f64e3-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="f64e3-125">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="f64e3-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="f64e3-126">Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="f64e3-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="f64e3-127">Om du har installerat tidigare versioner av Azure-moduler så kommer installationsprogrammet automatiskt att ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="f64e3-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="f64e3-128">MSI-paketet installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules` men skapar inte versionsspecifika mappar.</span><span class="sxs-lookup"><span data-stu-id="f64e3-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="f64e3-129">Kör i en Docker-behållare</span><span class="sxs-lookup"><span data-stu-id="f64e3-129">Run in a Docker container</span></span>

<span data-ttu-id="f64e3-130">Vi underhåller en uppsättning Docker-avbildningar som är förkonfigurerad med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f64e3-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="f64e3-131">Det finns två typer av behållare: de som kör traditionella PowerShell på Windows och en behållare som kör PowerShell Core på antingen Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="f64e3-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="f64e3-132">Miljö</span><span class="sxs-lookup"><span data-stu-id="f64e3-132">Environment</span></span> | <span data-ttu-id="f64e3-133">Docker-avbildning</span><span class="sxs-lookup"><span data-stu-id="f64e3-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="f64e3-134">PowerShell på Windows</span><span class="sxs-lookup"><span data-stu-id="f64e3-134">PowerShell on Windows</span></span> | [<span data-ttu-id="f64e3-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="f64e3-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="f64e3-136">PowerShell Core på Windows</span><span class="sxs-lookup"><span data-stu-id="f64e3-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="f64e3-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="f64e3-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="f64e3-138">PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="f64e3-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="f64e3-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="f64e3-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="f64e3-140">Använd `docker run -it $ImageName` för att hämta en interaktiv terminal och köra någon av dessa behållare.</span><span class="sxs-lookup"><span data-stu-id="f64e3-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="f64e3-141">Om du till exempel vill köra PowerShell Core på Linux-behållare använder du:</span><span class="sxs-lookup"><span data-stu-id="f64e3-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="f64e3-142">Om du vill köra en Windows-behållare i Docker måste OS-värden vara Windows och Docker måste konfigureras för att köra Windows-behållare.</span><span class="sxs-lookup"><span data-stu-id="f64e3-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="f64e3-143">Mer information om att växla mellan Windows- och Linux-miljöer i Docker finns i Docker-dokumentationen [Växla mellan Windows- och Linux-behållare](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="f64e3-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>