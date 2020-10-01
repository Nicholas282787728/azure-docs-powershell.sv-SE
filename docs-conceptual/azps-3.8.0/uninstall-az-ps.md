---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20859d6135676a3a4fb1e9f5d66909d157b38ac6
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/26/2020
ms.locfileid: "91381385"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d5287-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="d5287-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="d5287-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="d5287-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d5287-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d5287-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="d5287-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.</span><span class="sxs-lookup"><span data-stu-id="d5287-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="d5287-107">Avinstallera Az PowerShell-modulen från MSI</span><span class="sxs-lookup"><span data-stu-id="d5287-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="d5287-108">Om du har installerat Az PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5287-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="d5287-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="d5287-109">Platform</span></span>         |                      <span data-ttu-id="d5287-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="d5287-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="d5287-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5287-111">Windows 10</span></span>               | <span data-ttu-id="d5287-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="d5287-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="d5287-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5287-113">Windows 7</span></span> </br><span data-ttu-id="d5287-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5287-114">Windows 8</span></span> | <span data-ttu-id="d5287-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="d5287-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d5287-116">På den här skärmen bör du se **Azure PowerShell** i listan över program.</span><span class="sxs-lookup"><span data-stu-id="d5287-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="d5287-117">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="d5287-117">This is the app to uninstall.</span></span> <span data-ttu-id="d5287-118">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="d5287-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="d5287-119">Avinstallera Az PowerShell-modulen från PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d5287-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="d5287-120">Om du vill avinstallera Az-modulerna kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="d5287-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d5287-121">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="d5287-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d5287-122">Om du vill ta bort Az PowerShell-modulen helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="d5287-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d5287-123">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="d5287-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d5287-124">Om du vill kontrollera vilka versioner av Az PowerShell-modulen som är installerade kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="d5287-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="d5287-125">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="d5287-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d5287-126">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="d5287-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="d5287-127">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än **Process** eller **Nuvarande användare**.</span><span class="sxs-lookup"><span data-stu-id="d5287-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="d5287-128">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="d5287-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d5287-129">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Az PowerShell-modulen och dess undermoduler.</span><span class="sxs-lookup"><span data-stu-id="d5287-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="d5287-130">När skriptet körs visas **Namn**, **Version** och **Tillstånd** för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="d5287-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="d5287-131">Om du enbart vill köra skriptet för att se vad som skulle tas bort utan att ta bort något använder du parametern `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="d5287-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="d5287-132">Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="d5287-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="d5287-133">Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.</span><span class="sxs-lookup"><span data-stu-id="d5287-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="d5287-134">Kör följande exempel för varje version av Az PowerShell-modulen som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="d5287-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="d5287-135">För att göra det enklare för dig avinstallerar följande skript alla versioner av Az **förutom** den senaste.</span><span class="sxs-lookup"><span data-stu-id="d5287-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="d5287-136">Avinstallera AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="d5287-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="d5287-137">Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns två alternativ.</span><span class="sxs-lookup"><span data-stu-id="d5287-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="d5287-138">Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="d5287-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="d5287-139">Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa anvisningarna för avinstallation av MSI.</span><span class="sxs-lookup"><span data-stu-id="d5287-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="d5287-140">Avinstallera AzureRM PowerShell-modulen från MSI</span><span class="sxs-lookup"><span data-stu-id="d5287-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="d5287-141">Om du har installerat AzureRM PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5287-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="d5287-142">Plattform</span><span class="sxs-lookup"><span data-stu-id="d5287-142">Platform</span></span>         |                      <span data-ttu-id="d5287-143">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="d5287-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="d5287-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5287-144">Windows 10</span></span>               | <span data-ttu-id="d5287-145">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="d5287-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="d5287-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5287-146">Windows 7</span></span> </br><span data-ttu-id="d5287-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5287-147">Windows 8</span></span> | <span data-ttu-id="d5287-148">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="d5287-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d5287-149">På den här skärmen bör du se **Azure PowerShell** eller **Microsoft Azure PowerShell – månad, år** i listan över program.</span><span class="sxs-lookup"><span data-stu-id="d5287-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="d5287-150">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="d5287-150">This is the app to uninstall.</span></span> <span data-ttu-id="d5287-151">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="d5287-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="d5287-152">Avinstallera AzureRM PowerShell-modulen från PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d5287-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="d5287-153">Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med cmdleten [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av modulen `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="d5287-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="d5287-154">Följande exempel tar bort _alla_ AzureRM-moduler från datorn.</span><span class="sxs-lookup"><span data-stu-id="d5287-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="d5287-155">Det kräver dock administratörsbehörigheter.</span><span class="sxs-lookup"><span data-stu-id="d5287-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
