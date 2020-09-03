---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 17a9b604da84f131c434e3001732a34f7d620fbd
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243590"
---
# <a name="uninstall-the-azure-powershell-module"></a>Avinstallera Azure PowerShell-modulen

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system. Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi-or-web-platform-installer"></a>Avinstallera MSI eller installationsprogrammet för webbplattformen

Om du har installerat Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen måste du avinstallera det via Windows-systemet istället för PowerShell.

| Plattform | Instruktioner |
|----------|--------------|
| Windows 10 | Start > Inställningar > Appar |
| Windows 7 </br>Windows 8 | Start > Kontrollpanelen > Program > Avinstallera ett program |

På den här skärmen bör du se ”Azure PowerShell” i listan över program och du kan avinstallera härifrån.

## <a name="uninstall-from-powershell"></a>Avinstallera från PowerShell

Om du installerade Azure PowerShell med hjälp av PowerShellGet kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Men `Uninstall-Module` avinstallerar endast en modul. Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt. Avinstallationen kan vara komplicerad om du har flera versioner av Azure PowerShell installerade.

Följande skript kan användas för att ta bort en enskild version av Azure PowerShell fullständigt. Skriptet frågar PowerShell-galleriet efter en lista med beroende undermoduler. Sedan avinstallerar skriptet rätt version av varje undermodul.

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

Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen. Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras. Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras. Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden. I sådant fall visas en lista med de tillgängliga versionerna av beroendet.
> Du kan sedan ta bort eventuella gamla versioner manuellt med `Uninstall-Module`.


Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera. I syfte att underlätta för dig avinstallerar följande skript alla versioner av AzureRM __förutom__ den senaste.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
