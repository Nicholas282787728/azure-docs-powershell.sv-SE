---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715617"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="ea167-103">Så här avinstallerar du Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="ea167-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="ea167-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="ea167-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="ea167-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="ea167-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="ea167-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.</span><span class="sxs-lookup"><span data-stu-id="ea167-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="ea167-107">Avinstallera Az-modulen</span><span class="sxs-lookup"><span data-stu-id="ea167-107">Uninstall the Az module</span></span>

<span data-ttu-id="ea167-108">Om du har Az-modulen installerad på datorn och vill avinstallera den finns det två alternativ.</span><span class="sxs-lookup"><span data-stu-id="ea167-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="ea167-109">Vilken metod du ska använda beror på hur du installerade Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="ea167-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="ea167-110">Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa MSI-stegen för avinstallation.</span><span class="sxs-lookup"><span data-stu-id="ea167-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="ea167-111">Alternativ 1: Avinstallera Az PowerShell-modulen från MSI</span><span class="sxs-lookup"><span data-stu-id="ea167-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="ea167-112">Om du har installerat Az PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea167-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="ea167-113">Plattform</span><span class="sxs-lookup"><span data-stu-id="ea167-113">Platform</span></span>         |                      <span data-ttu-id="ea167-114">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="ea167-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="ea167-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ea167-115">Windows 10</span></span>               | <span data-ttu-id="ea167-116">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="ea167-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="ea167-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea167-117">Windows 7</span></span> </br><span data-ttu-id="ea167-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea167-118">Windows 8</span></span> | <span data-ttu-id="ea167-119">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="ea167-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="ea167-120">På den här skärmen bör du se **Azure PowerShell** i listan över program.</span><span class="sxs-lookup"><span data-stu-id="ea167-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="ea167-121">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="ea167-121">This is the app to uninstall.</span></span> <span data-ttu-id="ea167-122">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="ea167-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="ea167-123">Alternativ 2: Avinstallera Az PowerShell-modulen från PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="ea167-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="ea167-124">Om du vill avinstallera Az-modulerna kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="ea167-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="ea167-125">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="ea167-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="ea167-126">Om du vill ta bort Az PowerShell-modulen helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="ea167-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="ea167-127">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="ea167-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="ea167-128">Om du vill kontrollera vilka versioner av Az PowerShell-modulen som är installerade kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="ea167-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="ea167-129">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="ea167-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="ea167-130">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="ea167-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="ea167-131">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än **Process** eller **Nuvarande användare**.</span><span class="sxs-lookup"><span data-stu-id="ea167-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="ea167-132">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="ea167-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="ea167-133">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Az PowerShell-modulen och dess undermoduler.</span><span class="sxs-lookup"><span data-stu-id="ea167-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="ea167-134">När skriptet körs visas **Namn**, **Version** och **Tillstånd** för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="ea167-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="ea167-135">Om du enbart vill köra skriptet för att se vad som skulle tas bort utan att ta bort något använder du parametern `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="ea167-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="ea167-136">Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="ea167-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="ea167-137">Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.</span><span class="sxs-lookup"><span data-stu-id="ea167-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="ea167-138">Kör följande exempel för varje version av Az PowerShell-modulen som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="ea167-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="ea167-139">För att göra det enklare för dig avinstallerar följande skript alla versioner av Az **förutom** den senaste.</span><span class="sxs-lookup"><span data-stu-id="ea167-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="ea167-140">Avinstallera AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="ea167-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="ea167-141">Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns två alternativ.</span><span class="sxs-lookup"><span data-stu-id="ea167-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="ea167-142">Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="ea167-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="ea167-143">Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa MSI-stegen för avinstallation.</span><span class="sxs-lookup"><span data-stu-id="ea167-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="ea167-144">Alternativ 1: Avinstallera AzureRM PowerShell-modulen från MSI</span><span class="sxs-lookup"><span data-stu-id="ea167-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="ea167-145">Om du har installerat AzureRM PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea167-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="ea167-146">Plattform</span><span class="sxs-lookup"><span data-stu-id="ea167-146">Platform</span></span>         |                      <span data-ttu-id="ea167-147">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="ea167-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="ea167-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ea167-148">Windows 10</span></span>               | <span data-ttu-id="ea167-149">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="ea167-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="ea167-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea167-150">Windows 7</span></span> </br><span data-ttu-id="ea167-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ea167-151">Windows 8</span></span> | <span data-ttu-id="ea167-152">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="ea167-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="ea167-153">På den här skärmen bör du se **Azure PowerShell** eller **Microsoft Azure PowerShell – månad, år** i listan över program.</span><span class="sxs-lookup"><span data-stu-id="ea167-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="ea167-154">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="ea167-154">This is the app to uninstall.</span></span> <span data-ttu-id="ea167-155">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="ea167-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="ea167-156">Alternativ 2: Avinstallera AzureRM PowerShell-modulen från PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="ea167-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="ea167-157">Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med cmdleten [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av modulen `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="ea167-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="ea167-158">För att kunna använda `Az.Accounts`-modulen behöver du ha Az-modulen installerad.</span><span class="sxs-lookup"><span data-stu-id="ea167-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="ea167-159">Det finns inte stöd för att ha både AzureRM-modulen och Az-modulen installerade samtidigt. Däremot kan Az-modulen användas för omedelbar avinstallation av AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="ea167-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="ea167-160">Du kan installera Az-modulen och kringgå AzureRM-modulvarningen med följande kommando om du inte redan har Az-modulen installerad:</span><span class="sxs-lookup"><span data-stu-id="ea167-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="ea167-161">När Az-modulen har installerats tar följande kommando bort _alla_ AzureRM-moduler från datorn.</span><span class="sxs-lookup"><span data-stu-id="ea167-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="ea167-162">Det kräver dock administratörsbehörigheter.</span><span class="sxs-lookup"><span data-stu-id="ea167-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
