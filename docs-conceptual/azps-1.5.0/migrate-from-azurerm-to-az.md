---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882673"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrera från AzureRM till Azure PowerShell Az

Az-modulen har funktionsparitet med AzureRM, men använder kortare och mer konsekventa cmdlet-namn.
Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen. För att underlätta övergången erbjuder Az verktyg så att du kan köra dina befintliga skript med hjälp av AzureRM. Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till den nya modulen.

En fullständig lista över icke-bakåtkompatibla ändringar mellan AzureRM och Az finns i [Migreringsguiden för Az 1.0.0](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>Sök efter installerade versioner av AzureRM

Az-modulen kan vara installerad samtidigt som AzureRM-modulen, men detta rekommenderas inte. Innan du påbörjar migreringen bör du kontrollera vilka versioner av AzureRM som finns installerade på datorn. Då kan du se till att skripten redan körs med den senaste versionen, och du ser om det går att aktivera kommandoalias utan att avinstallera AzureRM.

Om du vill kontrollera vilka versioner av AzureRM du har installerade kör du följande kommando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Se till att dina befintliga skript fungerar med den senaste versionen av AzureRM

Det här är det viktigaste steget! Kör dina befintliga skript och se till att de fungerar med den _senaste_ versionen av AzureRM (__6.13.1__). Om dina skript inte fungerar läser du [AzureRM-migreringsguiden](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Installera Azure PowerShell Az-modulen

Första steget är att installera Az-modulen på din plattform. När du installerar Az bör du avinstallera AzureRM. I följande steg får du lära dig hur du fortsätter att köra dina befintliga skript och aktiverar kompatibilitet för gamla cmdlet-namn.

Installera Azure PowerShell Az-modulen enligt följande:

* __REKOMMENDERAS__: [Avinstallera AzureRM-modulen](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Se till att ta bort _alla_ installerade versioner av AzureRM, inte bara den senaste versionen.
* [Installera Az-modulen](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Aktivera AzureRM-kompatibilitetsalias 

> [!IMPORTANT]
>
> Aktivera kompatibilitetsläge endast om du har avinstallerat _alla_ versioner av AzureRM. Om du aktiverar kompatibilitetsläge när det fortfarande finns tillgängliga AzureRM-cmdletar kan du få oväntade resultat. Hoppa över det här steget om du väljer att behålla AzureRM installerat, men tänk på att alla AzureRM-cmdletar kommer att använda de äldre modulerna och inte anropa några Az-cmdletar.

När AzureRM har avinstallerats och skripten fungerar med den senaste AzureRM-versionen är nästa steg att aktivera kompatibilitetsläget för Az-modulen. Kompatibilitet aktiveras med kommandot:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Alias gör det möjligt att använda äldre cmdlet-namn med Az-modulen installerad. Dessa alias skrivs till användarprofilen för det valda omfånget. Om det inte finns någon användarprofil skapas en.

> [!WARNING]
>
> Du kan använda ett annat `-Scope` för det här kommandot, men det rekommenderas inte. Alias skrivs till användarprofilen för det valda omfånget, så fortsätt att aktivera dem för ett så begränsat omfång som möjligt. Aktivering av alias i hela systemet kan också orsaka problem för andra användare som har AzureRM installerat i sitt lokala omfång.

När aliasläget har aktiverats kör du skripten igen för att bekräfta att de fortfarande fungerar som förväntat. 

## <a name="change-module-imports-and-cmdlet-names"></a>Ändra modulimporter och cmdlet-namn

I allmänhet har modulnamnen ändrats så att `AzureRM` och `Azure` blir `Az`, och samma sak för cmdletar.
`AzureRM.Compute`-modulens namn har till exempel ändrats till `Az.Compute`. `New-AzureRMVM` har blivit `New-AzVM`, och `Get-AzureStorageBlob` är nu `Get-AzStorageBlob`.

Det finns undantag för den här namngivningsändringen som du bör känna till. Vissa moduler har bytt namn eller slagits samman till befintliga modeller utan att det påverkar suffixet för deras cmdletar, förutom att `AzureRM` eller `Azure` ändras till `Az`. I övrigt ändras det fullständiga cmdlet-suffixet så att det återspeglar det nya modulnamnet.

| AzureRM-modul | Az-modul | Ändrat cmdlet-suffix? |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Ja |
| AzureRM.Insights | Az.Monitor | Ja |
| AzureRM.DataFactories | Az.DataFactory | Ja |
| AzureRM.DataFactoryV2 | Az.DataFactory | Ja |
| AzureRM.RecoveryServices | Az.RecoveryServices | Nej |
| AzureRM.RecoveryServices | Az.RecoveryServices | Nej |
| AzureRM.Tags | Az.Resources | Nej |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Nej |
| AzureRM.UsageAggregates | Az.Billing | Nej |
| AzureRM.Consumption | Az.Billing | Nej |

## <a name="summary"></a>Sammanfattning

Genom att följa de här stegen kan du uppdatera alla befintliga skript så att de använder den nya modulen. Om du har några frågor eller problem med de här stegen som har gjort migreringen svår får du gärna kommentera den här artikeln så att vi kan förbättra instruktionerna.
