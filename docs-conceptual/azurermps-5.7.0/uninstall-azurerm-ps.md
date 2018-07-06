---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 052a150afa6cd90ca5babdce2aa7e3b4ff0b893b
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091651"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="ca2f9-103">Avinstallera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="ca2f9-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="ca2f9-104">Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="ca2f9-105">Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="ca2f9-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span> <span data-ttu-id="ca2f9-106">Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="ca2f9-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

# <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="ca2f9-107">Avinstallera MSI eller installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="ca2f9-107">Uninstall MSI or Web Platform Installer</span></span> 

<span data-ttu-id="ca2f9-108">Om du har installerat Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen måste du avinstallera det via Windows-systemet istället för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>
 
| <span data-ttu-id="ca2f9-109">Plattform</span><span class="sxs-lookup"><span data-stu-id="ca2f9-109">Platform</span></span> | <span data-ttu-id="ca2f9-110">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="ca2f9-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="ca2f9-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ca2f9-111">Windows 10</span></span> | <span data-ttu-id="ca2f9-112">Start > Inställningar > Appar</span><span class="sxs-lookup"><span data-stu-id="ca2f9-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="ca2f9-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca2f9-113">Windows 7</span></span> </br><span data-ttu-id="ca2f9-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ca2f9-114">Windows 8</span></span> | <span data-ttu-id="ca2f9-115">Start > Kontrollpanelen > Program > Avinstallera ett program</span><span class="sxs-lookup"><span data-stu-id="ca2f9-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="ca2f9-116">På den här skärmen bör du se ”Azure PowerShell” i listan över program och du kan avinstallera härifrån.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

# <a name="uninstall-from-powershell"></a><span data-ttu-id="ca2f9-117">Avinstallera från PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca2f9-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="ca2f9-118">Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="ca2f9-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="ca2f9-119">Men `Uninstall-Module` avinstallerar endast en modul.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="ca2f9-120">Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="ca2f9-121">Avinstallationen kan vara komplicerad om du har flera versioner av Azure PowerShell installerade.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="ca2f9-122">Följande skript kan användas för att ta bort en enskild version av Azure PowerShell fullständigt.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="ca2f9-123">Skriptet frågar PowerShell-galleriet efter en lista med beroende undermoduler.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="ca2f9-124">Sedan avinstallerar skriptet rätt version av varje undermodul.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="ca2f9-125">Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="ca2f9-126">Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="ca2f9-127">När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="ca2f9-128">Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.</span><span class="sxs-lookup"><span data-stu-id="ca2f9-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>