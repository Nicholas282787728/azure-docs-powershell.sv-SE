---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259890"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrera från AzureRM till Azure PowerShell Az

Az-modulen har funktionsparitet med AzureRM, men använder kortare och mer konsekventa cmdlet-namn.
Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen. För att underlätta övergången erbjuder Az verktyg så att du kan köra dina befintliga skript med hjälp av AzureRM. Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till den nya modulen.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Se till att dina befintliga skript fungerar med den senaste versionen av AzureRM

Det här är det viktigaste steget! Kör dina befintliga skript och se till att de fungerar med den _senaste_ versionen av AzureRM (__6.12.0__). Om dina skript inte fungerar läser du [AzureRM-migreringsguiden](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Installera Azure PowerShell Az-modulen

Första steget är att installera Az-modulen på din plattform. För att kunna installera Az måste du avinstallera AzureRM.
I följande steg får du lära dig hur du fortsätter att köra dina befintliga skript och aktiverar kompatibilitet för gamla cmdlet-namn.

Installera Azure PowerShell Az-modulen enligt följande:

* [Avinstallera AzureRM-modulen](uninstall-azurerm-ps.md). Se till att ta bort _alla_ installerade versioner av AzureRM, inte bara den senaste versionen.
* [Installera Az-modulen](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Aktivera AzureRM-aliasläge

När AzureRM har avinstallerats och skripten fungerar med den senaste AzureRM-versionen är det dags att aktivera kompatibilitetsläget för Az-modulen. Kompatibilitet aktiveras med kommandot:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Alias gör det möjligt att använda gamla cmdlet-namn med `Az`-modulen installerad. Dessa alias skrivs till användarprofilen för det valda omfånget. Om det inte finns någon användarprofil skapas en.

> [!WARNING]
>
> Du kan använda ett annat `-Scope` för det här kommandot, men det rekommenderas inte! Alias skrivs till användarprofilen för det valda omfånget, så fortsätt att aktivera dem för ett så begränsat omfång som möjligt. Aktivering av alias i hela systemet kan också orsaka problem för andra användare som har `AzureRM` installerad i sitt lokala omfång.

När aliasläget har aktiverats kör du skripten igen för att bekräfta att de fortfarande fungerar som förväntat. 

## <a name="change-module-imports-and-cmdlet-names"></a>Ändra modulimporter och cmdlet-namn

I allmänhet har modulnamnen ändrats så att `AzureRM` och `Azure` blir `Az`, och samma sak för cmdletar.
`AzureRM.Compute`-modulens namn har till exempel ändrats till `Az.Compute`. `New-AzureRmVM` har blivit `New-AzVM`, och `Get-AzureStorageBlob` är nu `Get-AzStorageBlob`.

Det finns undantag till den här namngivningsändringen som du bör känna till innan du ändrar några namn:

| AzureRM-modul | Az-modul |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices | Az.RecoveryServices |
| AzureRM.RecoveryServices | Az.RecoveryServices |

## <a name="summary"></a>Sammanfattning

Genom att följa de här stegen kan du uppdatera alla befintliga skript så att de använder den nya modulen. Om du har några frågor eller problem med de här stegen som har gjort migreringen svår får du gärna kommentera den här artikeln så att vi kan förbättra instruktionerna.