---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 385dd0281185cfb9e7bdd2c98e4c557659fff384
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425354"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="48fa7-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="48fa7-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="48fa7-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="48fa7-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="48fa7-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="48fa7-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="48fa7-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="48fa7-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi"></a><span data-ttu-id="48fa7-107">Avinstallera MSI</span><span class="sxs-lookup"><span data-stu-id="48fa7-107">Uninstall MSI</span></span>

<span data-ttu-id="48fa7-108">Om du har installerat Azure PowerShell med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48fa7-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="48fa7-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="48fa7-109">Platform</span></span> | <span data-ttu-id="48fa7-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="48fa7-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="48fa7-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="48fa7-111">Windows 10</span></span> | <span data-ttu-id="48fa7-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="48fa7-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="48fa7-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48fa7-113">Windows 7</span></span> </br><span data-ttu-id="48fa7-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48fa7-114">Windows 8</span></span> | <span data-ttu-id="48fa7-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="48fa7-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="48fa7-116">På den här skärmen bör du se ”Azure PowerShell” i listan över program och du kan avinstallera härifrån.</span><span class="sxs-lookup"><span data-stu-id="48fa7-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="48fa7-117">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="48fa7-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="48fa7-118">Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="48fa7-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="48fa7-119">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="48fa7-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="48fa7-120">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="48fa7-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="48fa7-121">Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="48fa7-121">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="48fa7-122">Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="48fa7-122">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="48fa7-123">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="48fa7-123">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="48fa7-124">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="48fa7-124">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="48fa7-125">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48fa7-125">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="48fa7-126">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="48fa7-126">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="48fa7-127">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="48fa7-127">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>
