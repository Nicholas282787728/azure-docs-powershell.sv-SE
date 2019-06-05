---
title: Andra sätt att installera Azure PowerShell | Microsoft Docs
description: Så här installerar du Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: d41e7ce2faac6a82b63ed173b5b64b85b56577c0
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/11/2019
ms.locfileid: "65535077"
---
# <a name="other-installation-methods"></a><span data-ttu-id="29bd5-103">Andra installationsmetoder</span><span class="sxs-lookup"><span data-stu-id="29bd5-103">Other installation methods</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="29bd5-104">Azure PowerShell har flera olika installationsmetoder.</span><span class="sxs-lookup"><span data-stu-id="29bd5-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="29bd5-105">Vi rekommenderar att du använder PowerShellGet med PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="29bd5-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="29bd5-106">Azure PowerShell kan installeras på Windows med installationsprogram för webbplattformen (WebPI) eller med hjälp av MSI-filen som är tillgänglig från GitHub.</span><span class="sxs-lookup"><span data-stu-id="29bd5-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="29bd5-107">Installera på Windows med hjälp av installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="29bd5-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="29bd5-108">Att installera den senaste versionen av Azure PowerShell från WebPI går till på samma sätt som det gjorde för tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="29bd5-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="29bd5-109">Hämta [Azure PowerShell WebPI-paketet](http://aka.ms/webpi-azps) och starta installationen.</span><span class="sxs-lookup"><span data-stu-id="29bd5-109">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="29bd5-110">Om du tidigare har installerat Azure-moduler från PowerShell-galleriet så kommer installationsprogrammet automatiskt att ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="29bd5-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="29bd5-111">Detta förenklar din miljö genom att se till att endast en version av Azure PowerShell är installerad.</span><span class="sxs-lookup"><span data-stu-id="29bd5-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="29bd5-112">Det finns dock scenarier där du kan behöva flera versioner installerade på samma gång.</span><span class="sxs-lookup"><span data-stu-id="29bd5-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="29bd5-113">PowerShell-galleriets moduler installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="29bd5-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="29bd5-114">WebPI-installationsprogrammet däremot installerar Azure moduler i `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="29bd5-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="29bd5-115">Om ett fel inträffar under installationen kan du ta bort Azure\*-mapparna manuellt i din `$env:ProgramFiles\WindowsPowerShell\Modules`-mapp och försöka installera igen.</span><span class="sxs-lookup"><span data-stu-id="29bd5-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="29bd5-116">När installationen är färdig bör din `$env:PSModulePath`-inställning inkludera de kataloger som innehåller Azure PowerShell-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="29bd5-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="29bd5-117">Följande kommando kan användas för att kontrollera att Azure PowerShell är korrekt installerad.</span><span class="sxs-lookup"><span data-stu-id="29bd5-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="29bd5-118">Det finns ett känt problem som kan uppstå när du installerar från WebPI.</span><span class="sxs-lookup"><span data-stu-id="29bd5-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="29bd5-119">Om datorn kräver en omstart på grund av systemuppdateringar eller andra installationer kan det göra att uppdateringarna för `$env:PSModulePath` inte inkluderar sökvägen där Azure PowerShell är installerat.</span><span class="sxs-lookup"><span data-stu-id="29bd5-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="29bd5-120">När du försöker läsa in eller köra cmdletar efter installationen kan du få följande felmeddelande:</span><span class="sxs-lookup"><span data-stu-id="29bd5-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="29bd5-121">Det här felet kan korrigeras genom att starta om datorn eller importera modulen med den fullständigt kvalificerade sökvägen.</span><span class="sxs-lookup"><span data-stu-id="29bd5-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="29bd5-122">Exempel:</span><span class="sxs-lookup"><span data-stu-id="29bd5-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="29bd5-123">Installera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="29bd5-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="29bd5-124">Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="29bd5-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="29bd5-125">Om du har installerat tidigare versioner av Azure-moduler så kommer installationsprogrammet automatiskt att ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="29bd5-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="29bd5-126">MSI-paketet installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules` men skapar inte versionsspecifika mappar.</span><span class="sxs-lookup"><span data-stu-id="29bd5-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

