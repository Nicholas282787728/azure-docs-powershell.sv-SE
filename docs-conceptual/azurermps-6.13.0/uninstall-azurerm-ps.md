---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 17197b77e26ccf0e41b5faf3cbbde34338b28167
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037717"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="4f8f6-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="4f8f6-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="4f8f6-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="4f8f6-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="4f8f6-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="4f8f6-106">Om du påträffar en bugg får du gärna [skicka in ett GitHub-ärende](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4f8f6-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="4f8f6-107">Avinstallera Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="4f8f6-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="4f8f6-108">Om du har installerat Azure PowerShell med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="4f8f6-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="4f8f6-109">Platform</span></span> | <span data-ttu-id="4f8f6-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="4f8f6-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="4f8f6-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4f8f6-111">Windows 10</span></span> | <span data-ttu-id="4f8f6-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="4f8f6-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="4f8f6-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f8f6-113">Windows 7</span></span> </br><span data-ttu-id="4f8f6-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f8f6-114">Windows 8</span></span> | <span data-ttu-id="4f8f6-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="4f8f6-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="4f8f6-116">På den här skärmen bör du se __Azure PowerShell__ i listan över program.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="4f8f6-117">Det är appen som ska avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="4f8f6-118">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f8f6-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="4f8f6-119">Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="4f8f6-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="4f8f6-120">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="4f8f6-121">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="4f8f6-122">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="4f8f6-123">Om du vill kontrollera vilka versioner av Azure PowerShell som för närvarande är installerade så kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="4f8f6-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="4f8f6-124">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="4f8f6-125">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="4f8f6-126">Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än `Process` eller `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="4f8f6-127">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="4f8f6-128">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="4f8f6-129">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="4f8f6-130">Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="4f8f6-131">Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="4f8f6-132">Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="4f8f6-133">I sådant fall visas en lista med de tillgängliga versionerna av beroendet.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="4f8f6-134">Du kan sedan ta bort eventuella gamla versioner manuellt med `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="4f8f6-135">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="4f8f6-136">I syfte att underlätta för dig avinstallerar följande skript alla versioner av AzureRM __förutom__ den senaste.</span><span class="sxs-lookup"><span data-stu-id="4f8f6-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
