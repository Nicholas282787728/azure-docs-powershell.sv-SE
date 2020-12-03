---
title: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen
description: Lär dig hur du migrerar PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427844"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Snabbstart: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen

I den här artikeln får du lära dig hur du uppgraderar dina PowerShell-skript och skriptmoduler från AzureRM till Az PowerShell-modulen automatiskt med hjälp av PowerShell-modulen Az.Tools.Migration.

> [!IMPORTANT]
> PowerShell-modulen Az.Tools.Migration finns för närvarande som allmänt tillgänglig förhandsversion. Förhandsversionen tillhandahålls utan serviceavtal. Den rekommenderas inte för produktionsarbetsbelastningar. Vissa funktioner kanske inte stöds eller kan vara begränsade. Mer information finns i [Kompletterande villkor för användning av Microsoft Azure-förhandsversioner](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Du kan ge feedback och rapportera problem med PowerShell-modulen Az.Tools.Migration via [ett GitHub-ärende](https://github.com/Azure/azure-powershell-migration/issues) på lagringsplatsen `azure-powershell-migration`.

## <a name="requirements"></a>Krav

* Uppdatera dina befintliga PowerShell-skript till den senaste versionen av [AzureRM PowerShell-modulen (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installera PowerShell-modulen Az.Tools.Migration.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Steg 1: Skapa en uppgraderingsplan

Med cmdleten `New-AzUpgradeModulePlan` skapar du en uppgraderingsplan för att migrera dina skript och moduler till Az PowerShell-modulen. Uppgraderingsplanen specificerar den specifika filen och de offsetpunkter som behöver ändras vid flytten från AzureRM till Az PowerShell-cmdletarna.

> [!NOTE]
> Cmdleten `New-AzUpgradeModulePlan` kör inte planen. Den genererar bara uppgraderingsstegen.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Granska resultatet av uppgraderingsplanen.

```powershell
# Show the entire upgrade plan
$Plan
```

Kör följande kommando för att filtrera resultatet och visa kommandon som har varningar eller fel. På så sätt kan du snabbt identifiera fel innan du utför uppgraderingen, vilket är praktiskt om du har stora resultatmängder.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Steg 2: Genomför uppgraderingen

Uppgraderingsplanen utförs när du kör cmdleten `Invoke-AzUpgradeModulePlan`. Det här kommandot utför en uppgradering av den angivna filen eller mapparna förutom eventuella fel som identifierades av cmdleten `New-AzUpgradeModulePlan`.

Det här kommandot kräver att du anger om filerna ska ändras på plats eller om nya filer ska sparas vid sidan av dina ursprungliga filer (de ursprungliga filerna lämnas oförändrade).

> [!CAUTION]
> Detta går inte att ångra. Se alltid till att du har en säkerhetskopia av de PowerShell-skript och moduler som du tänker uppgradera.

> [!WARNING]
> Cmdleten `Invoke-AzUpgradeModulePlan` är destruktiv när alternativet `-FileEditMode ModifyExistingFiles` har angetts! Den ändrar dina skript och funktioner på plats enligt den moduluppgraderingsplan som skapades av cmdleten `New-AzUpgradeModulePlan`. Som icke-destruktivt alternativ anger du i stället `-FileEditMode SaveChangesToNewFiles`.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Granska resultatet av uppgraderingen.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Om fel returneras kan du ta en närmare titt på felresultaten med hjälp av följande kommando:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Begränsningar

* Automatiserade ändringar av parameternamn till ihopslagna parameteruppsättningar stöds inte. Om det påträffas när en uppgraderingsplan skapas returneras en varning.
* Fil-I/O-åtgärder använder standardkodning. Ovanliga filkodningssituationer kan orsaka problem.
* AzureRM-cmdletar som skickats som argument till testuttryck i Pester-enhetstester identifieras inte.
* För närvarande stöds endast AZ PowerShell-modul version 4.6.1 som mål.

## <a name="next-steps"></a>Nästa steg

Du kan läsa mer om Azure PowerShell-modulen i [Azure PowerShell-dokumentationen](/powershell/azure/)