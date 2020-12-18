---
title: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen
description: Lär dig hur du migrerar PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488538"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Snabbstart: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen

I den här artikeln får du lära dig hur du uppgraderar dina PowerShell-skript och skriptmoduler från AzureRM till Az PowerShell-modulen automatiskt med hjälp av PowerShell-modulen Az.Tools.Migration.

> [!IMPORTANT]
> PowerShell-modulen Az.Tools.Migration finns för närvarande som allmänt tillgänglig förhandsversion. Förhandsversionen tillhandahålls utan serviceavtal. Den rekommenderas inte för produktionsarbetsbelastningar. Vissa funktioner kanske inte stöds eller kan vara begränsade. Mer information finns i [Kompletterande villkor för användning av Microsoft Azure-förhandsversioner](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

## <a name="requirements"></a>Krav

* Uppdatera dina befintliga PowerShell-skript till den senaste versionen av [AzureRM PowerShell-modulen (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installera PowerShell-modulen Az.Tools.Migration.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Steg 1: Skapa en uppgraderingsplan

Med cmdleten **`New-AzUpgradeModulePlan`** skapar du en uppgraderingsplan för att migrera dina skript och moduler till Az PowerShell-modulen. Denna cmdlet gör inga ändringar i dina befintliga skript. Använd **`FilePath`** -parametern för att rikta in på ett särskilt skript eller **`DirectoryPath`** -parameter för att rikta in på alla skript i en speciell mapp.

> [!NOTE]
> Cmdleten **`New-AzUpgradeModulePlan`** kör inte planen. Den genererar bara uppgraderingsstegen.

I följande exempel skapas en plan för alla skript i mappen _`C:\Scripts`_ . **`OutVariable`** -parametern anges så att resultaten returneras och lagras samtidigt i en variabel med namnet **`Plan`** .

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Som du ser i följande utdata specificerar uppgraderingsplanen den specifika filen och de offsetpunkter som behöver ändras vid flytten från AzureRM till Az PowerShell-cmdletarna.

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

Innan du utför uppgraderingen måste du se resultatet av planen för problem. I följande exempel returneras en lista över skript och objekten i dessa skript som hindrar dem från att uppgraderas automatiskt.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

De objekt som visas i följande utdata kommer inte att uppgraderas automatiskt utan att problemen först korrigeras manuellt. Kända problem som inte kan uppgraderas automatiskt innehåller alla kommandon som använder ihopbuntning.

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>Steg 2: Genomför uppgraderingen

> [!CAUTION]
> Detta går inte att ångra. Se alltid till att du har en säkerhetskopia av de PowerShell-skript och moduler som du tänker uppgradera.

När du är nöjd med planen utförs uppgraderingen med **`Invoke-AzUpgradeModulePlan`** -cmdleten. Ange **`SaveChangesToNewFiles`** för parametervärdet **`FileEditMode`** för att förhindra att ändringar görs i de ursprungliga skripten. När du använder det här läget utförs uppgraderingen genom att skapa en kopia av varje inriktat skript med _`_az_upgraded`_ i filnamnet.

> [!WARNING]
> Cmdleten **`Invoke-AzUpgradeModulePlan`** är destruktiv när alternativet **`-FileEditMode ModifyExistingFiles`** har angetts! Den ändrar dina skript och funktioner på plats enligt den moduluppgraderingsplan som skapades av cmdleten **`New-AzUpgradeModulePlan`** . Som icke-destruktivt alternativ anger du i stället **`-FileEditMode SaveChangesToNewFiles`** .

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

Om fel returneras kan du ta en närmare titt på felresultaten med hjälp av följande kommando:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>Begränsningar

* Automatiserade ändringar av parameternamn till ihopslagna parameteruppsättningar stöds inte. Om det påträffas när en uppgraderingsplan skapas returneras en varning.
* Fil-I/O-åtgärder använder standardkodning. Ovanliga filkodningssituationer kan orsaka problem.
* AzureRM-cmdletar som skickats som argument till testuttryck i Pester-enhetstester identifieras inte.
* För närvarande stöds endast AZ PowerShell-modul version 4.6.1 som mål.

## <a name="how-to-report-issues"></a>Så här rapporterar du problem

Du kan ge feedback och rapportera problem med PowerShell-modulen Az.Tools.Migration via [ett GitHub-ärende](https://github.com/Azure/azure-powershell-migration/issues) på lagringsplatsen `azure-powershell-migration`.

## <a name="next-steps"></a>Nästa steg

Du kan läsa mer om Azure PowerShell-modulen i [Azure PowerShell-dokumentationen](/powershell/azure/)