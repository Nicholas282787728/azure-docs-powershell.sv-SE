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
# <a name="how-to-uninstall-azure-powershell-modules"></a>Så här avinstallerar du Azure PowerShell-moduler

Den här artikeln beskriver hur du avinstallerar en äldre version av Azure PowerShell eller tar bort det fullständigt från ditt system. Om du har bestämt dig för att avinstallera Azure PowerShell fullständigt kan du ge oss feedback genom cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback). Om du har påträffat en bugg vill vi gärna att du [öppnar ett GitHub-supportärende](https://github.com/azure/azure-powershell/issues) så att den kan korrigeras.

## <a name="uninstall-the-az-module"></a>Avinstallera Az-modulen

Om du har Az-modulen installerad på datorn och vill avinstallera den finns det två alternativ. Vilken metod du ska använda beror på hur du installerade Az-modulen. Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa MSI-stegen för avinstallation.

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a>Alternativ 1: Avinstallera Az PowerShell-modulen från MSI

Om du har installerat Az PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.

|         Plattform         |                      Instruktioner                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Inställningar > Appar                                |
| Windows 7 </br>Windows 8 | Start > Kontrollpanelen > Program > Avinstallera ett program |

På den här skärmen bör du se **Azure PowerShell** i listan över program. Det är appen som ska avinstalleras. Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a>Alternativ 2: Avinstallera Az PowerShell-modulen från PowerShellGet

Om du vill avinstallera Az-modulerna kan du använda cmdleten [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Men `Uninstall-Module` avinstallerar endast en modul. Om du vill ta bort Az PowerShell-modulen helt måste du avinstallera varje modul individuellt. Avinstallationen kan vara komplicerad om du har fler än en version av Azure PowerShell installerad.

Om du vill kontrollera vilka versioner av Az PowerShell-modulen som är installerade kör du följande kommando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

Följande skript frågar PowerShell-galleriet efter en lista med beroende undermoduler. Sedan avinstallerar skriptet rätt version av varje undermodul. Du måste ha administratörsåtkomst för att köra det här skriptet i ett annat omfång än **Process** eller **Nuvarande användare**.

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

Om du vill använda den här funktionen kopierar och klistrar du in koden i PowerShell-sessionen. Följande exempel visar hur du kör funktionen för att ta bort en äldre version av Az PowerShell-modulen och dess undermoduler.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

När skriptet körs visas **Namn**, **Version** och **Tillstånd** för varje undermodul som avinstalleras. Om du enbart vill köra skriptet för att se vad som skulle tas bort utan att ta bort något använder du parametern `-WhatIf`.

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
> Om det här skriptet inte kan matcha ett exakt beroende med den version som ska avinstalleras kommer inte _någon_ version av beroendet att avinstalleras. Det beror på att det kan finnas andra versioner av målmodulen i systemet som förlitar sig på dessa beroenden.

Kör följande exempel för varje version av Az PowerShell-modulen som du vill avinstallera.
För att göra det enklare för dig avinstallerar följande skript alla versioner av Az **förutom** den senaste.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Avinstallera AzureRM-modulen

Om du har installerat Az-modulen på datorn och vill avinstallera AzureRM finns två alternativ. Vilken metod du ska använda beror på hur du installerade AzureRM-modulen. Om du inte känner till den ursprungliga installationsmetoden börjar du med att följa MSI-stegen för avinstallation.

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a>Alternativ 1: Avinstallera AzureRM PowerShell-modulen från MSI

Om du har installerat AzureRM PowerShell-modulen med hjälp av MSI-paketet måste du avinstallera det via Windows-systemet i stället för PowerShell.

|         Plattform         |                      Instruktioner                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Inställningar > Appar                                |
| Windows 7 </br>Windows 8 | Start > Kontrollpanelen > Program > Avinstallera ett program |

På den här skärmen bör du se **Azure PowerShell** eller **Microsoft Azure PowerShell – månad, år** i listan över program. Det är appen som ska avinstalleras. Om det här programmet inte visas i listan så installerade du via PowerShellGet. Då följer du anvisningarna som följer.

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a>Alternativ 2: Avinstallera AzureRM PowerShell-modulen från PowerShellGet

Om du installerade AzureRM med PowerShellGet så kan du ta bort modulerna med cmdleten [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), som är tillgängligt som en del av modulen `Az.Accounts`.

För att kunna använda `Az.Accounts`-modulen behöver du ha Az-modulen installerad.  Det finns inte stöd för att ha både AzureRM-modulen och Az-modulen installerade samtidigt. Däremot kan Az-modulen användas för omedelbar avinstallation av AzureRM-modulen.  Du kan installera Az-modulen och kringgå AzureRM-modulvarningen med följande kommando om du inte redan har Az-modulen installerad:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

När Az-modulen har installerats tar följande kommando bort _alla_ AzureRM-moduler från datorn. Det kräver dock administratörsbehörigheter.

```powershell-interactive
Uninstall-AzureRm
```
