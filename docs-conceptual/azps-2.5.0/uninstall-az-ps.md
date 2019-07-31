---
title: Avinstallera Azure PowerShell
description: Så här utför du en fullständig avinstallation av Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: e71b4d0d662b29a32610fecb36351532040428e4
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657900"
---
# <a name="uninstall-the-azure-powershell-module"></a>Avinstallera Azure PowerShell-modulen

Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system. Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.

## <a name="uninstall-the-az-module"></a>Avinstallera Az-modulen

Om du vill avinstallera Az-modulerna använder du cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Men `Uninstall-Module` avinstallerar endast en modul. Om du vill ta bort Azure PowerShell helt måste du avinstallera varje modul individuellt. Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.

Om du vill kontrollera vilka versioner av Azure PowerShell som för närvarande är installerade så kör du följande kommando:

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

Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler. Sedan avinstallerar skriptet rätt version av varje undermodul. Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än `Process` eller `CurrentUser`.

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
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

När skriptet körs visas namnet och versionen för varje undermodul som avinstalleras. Om du enbart vill köra skriptet för att se vad som skulle tas bort, utan att ta bort det, så använder du alternativet `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras. Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden. I sådant fall visas en lista med de tillgängliga versionerna av beroendet.
> Du kan sedan ta bort eventuella gamla versioner manuellt med `Uninstall-Module`.

Kör det här kommandot för varje version av Azure PowerShell som du vill avinstallera. I syfte att underlätta för dig avinstallerar följande skript alla versioner av Az __utom__ den senaste.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Avinstallera AzureRM-modulen

Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns det två alternativ där du inte behöver köra `Uninstall-AllModules`-skriptet ovan. Vilken metod du ska använda beror på hur du installerade AzureRM-modulen.
Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa anvisningarna för avinstallation av MSI.

### <a name="uninstall-azure-powershell-msi"></a>Avinstallera Azure PowerShell MSI

Om du installerade Azure PowerShell AzureRM-modulerna med MSI-paketet måste du avinstallera via Windows-systemet i stället för via PowerShell.

| Plattform | Instruktioner |
|----------|--------------|
| Windows 10 | Start > Inställningar > Appar |
| Windows 7 </br>Windows 8 | Start > Kontrollpanelen > Program > Avinstallera ett program |

På den här skärmen bör du se __Azure PowerShell__ i listan över program. Det är appen som ska avinstalleras. Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.

### <a name="uninstall-from-powershell"></a>Avinstallera från PowerShell

Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med kommandot [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av `Az.Accounts`-modulen. Då tas _alla_ AzureRM-moduler bort från datorn, men administratörsbehörighet krävs.

```powershell-interactive
Uninstall-AzureRm
```

Om du inte kan köra kommandot `Uninstall-AzureRM` använder du skriptet [`Uninstall-AllModules` ](#uninstall-script) som finns i den här artikeln med följande anrop:

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```