---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068786"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="2ce98-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="2ce98-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="2ce98-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="2ce98-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="2ce98-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="2ce98-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="2ce98-106">Om du påträffar en bugg får du gärna [skicka in ett GitHub-ärende](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="2ce98-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="2ce98-107">Avinstallera Az-modulen</span><span class="sxs-lookup"><span data-stu-id="2ce98-107">Uninstall the Az module</span></span>

<span data-ttu-id="2ce98-108">Om du vill avinstallera Az-modulerna använder du cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="2ce98-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="2ce98-109">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="2ce98-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="2ce98-110">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="2ce98-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="2ce98-111">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="2ce98-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="2ce98-112">Om du vill kontrollera vilka versioner av Azure PowerShell som för närvarande är installerade så kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="2ce98-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="2ce98-113">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="2ce98-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="2ce98-114">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="2ce98-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="2ce98-115">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än `Process` eller `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="2ce98-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="2ce98-116">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="2ce98-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="2ce98-117">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ce98-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="2ce98-118">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="2ce98-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="2ce98-119">Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="2ce98-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="2ce98-120">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="2ce98-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="2ce98-121">I syfte att underlätta för dig avinstallerar följande skript alla versioner av Az __utom__ den senaste.</span><span class="sxs-lookup"><span data-stu-id="2ce98-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="2ce98-122">Avinstallera AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="2ce98-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="2ce98-123">Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns det två alternativ där du inte behöver köra `Uninstall-AllModules`-skriptet ovan.</span><span class="sxs-lookup"><span data-stu-id="2ce98-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="2ce98-124">Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="2ce98-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="2ce98-125">Om du inte är säker följer du först anvisningarna för att avinstallera en MSI.</span><span class="sxs-lookup"><span data-stu-id="2ce98-125">If you're not sure, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="2ce98-126">Avinstallera Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="2ce98-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="2ce98-127">Om du installerade Azure PowerShell AzureRM-modulerna med MSI-paketet måste du avinstallera via Windows-systemet i stället för via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ce98-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="2ce98-128">Plattform</span><span class="sxs-lookup"><span data-stu-id="2ce98-128">Platform</span></span> | <span data-ttu-id="2ce98-129">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="2ce98-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="2ce98-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2ce98-130">Windows 10</span></span> | <span data-ttu-id="2ce98-131">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="2ce98-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="2ce98-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ce98-132">Windows 7</span></span> </br><span data-ttu-id="2ce98-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ce98-133">Windows 8</span></span> | <span data-ttu-id="2ce98-134">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="2ce98-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2ce98-135">På den här skärmen bör du se __Azure PowerShell__ i listan över program.</span><span class="sxs-lookup"><span data-stu-id="2ce98-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="2ce98-136">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="2ce98-136">This is the app to uninstall.</span></span> <span data-ttu-id="2ce98-137">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="2ce98-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="2ce98-138">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="2ce98-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="2ce98-139">Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med kommandot [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av `Az.Accounts`-modulen.</span><span class="sxs-lookup"><span data-stu-id="2ce98-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="2ce98-140">Då tas _alla_ AzureRM-moduler bort från datorn, men administratörsbehörighet krävs.</span><span class="sxs-lookup"><span data-stu-id="2ce98-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="2ce98-141">Om du inte kan köra `Uninstall-AzureRM`-kommandot använder du det `Uninstall-AllModules`-skript som finns i den här artikeln i stället.</span><span class="sxs-lookup"><span data-stu-id="2ce98-141">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>