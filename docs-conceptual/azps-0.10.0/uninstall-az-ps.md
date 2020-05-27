---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 10/22/2019
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 1bf94f4c7a27328b60b7f9369888f688541ba4a7
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387198"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="6effd-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="6effd-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="6effd-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="6effd-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="6effd-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="6effd-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="6effd-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.</span><span class="sxs-lookup"><span data-stu-id="6effd-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="6effd-107">Avinstallera Azure PowerShell från MSI</span><span class="sxs-lookup"><span data-stu-id="6effd-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="6effd-108">Om du har installerat Azure PowerShell med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6effd-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="6effd-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="6effd-109">Platform</span></span> | <span data-ttu-id="6effd-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="6effd-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="6effd-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6effd-111">Windows 10</span></span> | <span data-ttu-id="6effd-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="6effd-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="6effd-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6effd-113">Windows 7</span></span> </br><span data-ttu-id="6effd-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6effd-114">Windows 8</span></span> | <span data-ttu-id="6effd-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="6effd-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="6effd-116">På den här skärmen bör du se __Azure PowerShell__ i listan över program.</span><span class="sxs-lookup"><span data-stu-id="6effd-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="6effd-117">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="6effd-117">This is the app to uninstall.</span></span> <span data-ttu-id="6effd-118">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="6effd-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="6effd-119">Avinstallera Azure PowerShell från PowerShell Get</span><span class="sxs-lookup"><span data-stu-id="6effd-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="6effd-120">Om du vill avinstallera Az-modulerna använder du cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="6effd-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="6effd-121">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="6effd-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="6effd-122">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="6effd-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="6effd-123">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="6effd-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="6effd-124">Om du vill kontrollera vilka versioner av Azure PowerShell som för närvarande är installerade så kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="6effd-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="6effd-125">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="6effd-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="6effd-126">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="6effd-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="6effd-127">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än `Process` eller `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="6effd-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="6effd-128">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="6effd-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="6effd-129">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6effd-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="6effd-130">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="6effd-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="6effd-131">Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="6effd-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="6effd-132">Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="6effd-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="6effd-133">Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.</span><span class="sxs-lookup"><span data-stu-id="6effd-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="6effd-134">I sådant fall visas en lista med de tillgängliga versionerna av beroendet.</span><span class="sxs-lookup"><span data-stu-id="6effd-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="6effd-135">Du kan sedan ta bort eventuella gamla versioner manuellt med `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="6effd-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="6effd-136">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="6effd-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="6effd-137">I syfte att underlätta för dig avinstallerar följande skript alla versioner av Az __utom__ den senaste.</span><span class="sxs-lookup"><span data-stu-id="6effd-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="6effd-138">Avinstallera AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="6effd-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="6effd-139">Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns det två alternativ där du inte behöver köra `Uninstall-AllModules`-skriptet ovan.</span><span class="sxs-lookup"><span data-stu-id="6effd-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="6effd-140">Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="6effd-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="6effd-141">Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa anvisningarna för avinstallation av MSI.</span><span class="sxs-lookup"><span data-stu-id="6effd-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="6effd-142">Avinstallera Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="6effd-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="6effd-143">Om du installerade Azure PowerShell AzureRM-modulerna med MSI-paketet måste du avinstallera via Windows-systemet i stället för via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6effd-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="6effd-144">Plattform</span><span class="sxs-lookup"><span data-stu-id="6effd-144">Platform</span></span> | <span data-ttu-id="6effd-145">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="6effd-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="6effd-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6effd-146">Windows 10</span></span> | <span data-ttu-id="6effd-147">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="6effd-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="6effd-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6effd-148">Windows 7</span></span> </br><span data-ttu-id="6effd-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6effd-149">Windows 8</span></span> | <span data-ttu-id="6effd-150">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="6effd-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="6effd-151">På den här skärmen bör du se __Azure PowerShell__ eller __Microsoft Azure PowerShell – månad, år__ i listan över program.</span><span class="sxs-lookup"><span data-stu-id="6effd-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="6effd-152">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="6effd-152">This is the app to uninstall.</span></span> <span data-ttu-id="6effd-153">Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.</span><span class="sxs-lookup"><span data-stu-id="6effd-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="6effd-154">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="6effd-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="6effd-155">Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med kommandot [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av `Az.Accounts`-modulen.</span><span class="sxs-lookup"><span data-stu-id="6effd-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="6effd-156">Då tas _alla_ AzureRM-moduler bort från datorn, men administratörsbehörighet krävs.</span><span class="sxs-lookup"><span data-stu-id="6effd-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
<span data-ttu-id="6effd-157">eller</span><span class="sxs-lookup"><span data-stu-id="6effd-157">or</span></span>
```powershell-interactive
Uninstall-Module AzureRm
```

<span data-ttu-id="6effd-158">Om du inte kan köra kommandot `Uninstall-AzureRM` använder du skriptet [`Uninstall-AllModules`](#uninstall-script) som finns i den här artikeln med följande anrop:</span><span class="sxs-lookup"><span data-stu-id="6effd-158">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
<span data-ttu-id="6effd-159">eller</span><span class="sxs-lookup"><span data-stu-id="6effd-159">or</span></span>
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
