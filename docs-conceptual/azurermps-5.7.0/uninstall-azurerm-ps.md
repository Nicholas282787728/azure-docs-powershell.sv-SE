---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037689"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="efeba-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="efeba-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="efeba-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="efeba-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="efeba-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="efeba-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="efeba-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="efeba-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="efeba-107">Avinstallera MSI eller installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="efeba-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="efeba-108">Om du har installerat Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen måste du avinstallera det via Windows-systemet istället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="efeba-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="efeba-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="efeba-109">Platform</span></span> | <span data-ttu-id="efeba-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="efeba-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="efeba-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="efeba-111">Windows 10</span></span> | <span data-ttu-id="efeba-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="efeba-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="efeba-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="efeba-113">Windows 7</span></span> </br><span data-ttu-id="efeba-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="efeba-114">Windows 8</span></span> | <span data-ttu-id="efeba-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="efeba-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="efeba-116">På den här skärmen bör du se ”Azure PowerShell” i listan över program och du kan avinstallera härifrån.</span><span class="sxs-lookup"><span data-stu-id="efeba-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="efeba-117">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="efeba-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="efeba-118">Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="efeba-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="efeba-119">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="efeba-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="efeba-120">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="efeba-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="efeba-121">Avinstallationen kan vara komplicerad om du har flera versioner av Azure PowerShell installerade.</span><span class="sxs-lookup"><span data-stu-id="efeba-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="efeba-122">Följande skript kan användas för att ta bort en enskild version av Azure PowerShell fullständigt.</span><span class="sxs-lookup"><span data-stu-id="efeba-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="efeba-123">Skriptet frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="efeba-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="efeba-124">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="efeba-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="efeba-125">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="efeba-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="efeba-126">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="efeba-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="efeba-127">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="efeba-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="efeba-128">Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="efeba-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="efeba-129">Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="efeba-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="efeba-130">Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.</span><span class="sxs-lookup"><span data-stu-id="efeba-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="efeba-131">I sådant fall visas en lista med de tillgängliga versionerna av beroendet.</span><span class="sxs-lookup"><span data-stu-id="efeba-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="efeba-132">Du kan sedan ta bort eventuella gamla versioner manuellt med `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="efeba-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="efeba-133">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="efeba-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="efeba-134">I syfte att underlätta för dig avinstallerar följande skript alla versioner av AzureRM __förutom__ den senaste.</span><span class="sxs-lookup"><span data-stu-id="efeba-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
