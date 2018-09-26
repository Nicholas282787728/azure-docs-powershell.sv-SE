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
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300773"
---
# <a name="uninstall-the-azure-powershell-module"></a>Avinstallera Azure PowerShell-modulen

Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system. Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi"></a>Avinstallera MSI

Om du har installerat Azure PowerShell med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.

| Plattform | Instruktioner |
|----------|--------------|
| Windows 10 | Start > Inställningar > Appar |
| Windows 7 </br>Windows 8 | Start > Kontrollpanelen > Program > Avinstallera ett program |

På den här skärmen bör du se ”Azure PowerShell” i listan över program och du kan avinstallera härifrån.

## <a name="uninstall-from-powershell"></a>Avinstallera från PowerShell

Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Men `Uninstall-Module` avinstallerar endast en modul. Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt. Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.

Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler. Sedan avinstallerar skriptet rätt version av varje undermodul.

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

Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen. Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera.
