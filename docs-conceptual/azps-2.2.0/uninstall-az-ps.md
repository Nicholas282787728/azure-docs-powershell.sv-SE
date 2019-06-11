---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: eaabd8014368f7ea8f4c9504e58d920dad8a6518
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498632"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="dddf0-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="dddf0-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="dddf0-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="dddf0-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="dddf0-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="dddf0-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="dddf0-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.</span><span class="sxs-lookup"><span data-stu-id="dddf0-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="dddf0-107">Avinstallera Az-modulen</span><span class="sxs-lookup"><span data-stu-id="dddf0-107">Uninstall the Az module</span></span>

<span data-ttu-id="dddf0-108">Om du vill avinstallera Az-modulerna använder du cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="dddf0-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="dddf0-109">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="dddf0-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="dddf0-110">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="dddf0-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="dddf0-111">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="dddf0-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="dddf0-112">Om du vill kontrollera vilka versioner av Azure PowerShell som för närvarande är installerade så kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="dddf0-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="dddf0-113">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="dddf0-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="dddf0-114">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="dddf0-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="dddf0-115">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än `Process` eller `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="dddf0-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="dddf0-116">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="dddf0-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="dddf0-117">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dddf0-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="dddf0-118">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="dddf0-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="dddf0-119">Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="dddf0-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="dddf0-120">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="dddf0-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="dddf0-121">I syfte att underlätta för dig avinstallerar följande skript alla versioner av Az __utom__ den senaste.</span><span class="sxs-lookup"><span data-stu-id="dddf0-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="dddf0-122">Avinstallera AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="dddf0-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="dddf0-123">Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns det två alternativ där du inte behöver köra `Uninstall-AllModules`-skriptet ovan.</span><span class="sxs-lookup"><span data-stu-id="dddf0-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="dddf0-124">Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="dddf0-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="dddf0-125">Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa anvisningarna för avinstallation av MSI.</span><span class="sxs-lookup"><span data-stu-id="dddf0-125">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="dddf0-126">Avinstallera Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="dddf0-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="dddf0-127">Om du installerade Azure PowerShell AzureRM-modulerna med MSI-paketet måste du avinstallera via Windows-systemet i stället för via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dddf0-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="dddf0-128">Plattform</span><span class="sxs-lookup"><span data-stu-id="dddf0-128">Platform</span></span> | <span data-ttu-id="dddf0-129">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="dddf0-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="dddf0-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="dddf0-130">Windows 10</span></span> | <span data-ttu-id="dddf0-131">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="dddf0-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="dddf0-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dddf0-132">Windows 7</span></span> </br><span data-ttu-id="dddf0-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dddf0-133">Windows 8</span></span> | <span data-ttu-id="dddf0-134">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="dddf0-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="dddf0-135">På den här skärmen bör du se __Azure PowerShell__ i listan över program.</span><span class="sxs-lookup"><span data-stu-id="dddf0-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="dddf0-136">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="dddf0-136">This is the app to uninstall.</span></span> <span data-ttu-id="dddf0-137">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="dddf0-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="dddf0-138">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="dddf0-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="dddf0-139">Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med kommandot [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av `Az.Accounts`-modulen.</span><span class="sxs-lookup"><span data-stu-id="dddf0-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="dddf0-140">Då tas _alla_ AzureRM-moduler bort från datorn, men administratörsbehörighet krävs.</span><span class="sxs-lookup"><span data-stu-id="dddf0-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="dddf0-141">Om du inte kan köra kommandot `Uninstall-AzureRM` använder du skriptet [`Uninstall-AllModules` ](#uninstall-script) som finns i den här artikeln med följande anrop:</span><span class="sxs-lookup"><span data-stu-id="dddf0-141">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```