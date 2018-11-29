---
title: Introduktion till Azure PowerShell Az-modulen
description: Vi introducerar den nya Azure PowerShell-modulen Az, som ersätter AzureRM-modulen.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587320"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduktion till den nya Azure PowerShell Az-modulen

Från november 2018 är Azure PowerShell `Az`-modulen tillgänglig som fullständig offentlig förhandsversion.
Az erbjuder kortare kommandon, förbättrad stabilitet och har stöd för Windows, macOS och Linux. Az erbjuder också funktionsparitet och en enkel migreringsväg från AzureRM.

Az använder .NET Standard-biblioteket, vilket innebär att den körs på PowerShell 5.x och PowerShell 6.x.
Eftersom PowerShell 6.x kan köras på Linux, macOS och Windows innebär det att Az är tillgänglig för alla plattformar.
Med .NET Standard kan vi förena kodbasen för Azure PowerShell med minimal inverkan på användare.

Az är en ny modul, så versionen har nollställts. Den första stabila versionen blir 1.0, men modulen har funktionsparitet med AzureRm från november 2018.

## <a name="upgrade-to-az"></a>Uppgradera till Az

Vi rekommenderar att användare uppgraderar till den nya `Az`-modulen. Gör så här:

* [Avinstallera Azure PowerShell AzureRM-modulen](/powershell/azure/uninstall-azurerm-ps)
* [Installera Azure PowerShell Az-modulen](/powershell/azure/install-az-ps)
* Aktivera kompatibilitetsläge för AzureRM med `Enable-AzureRMAlias` medan du bekantar dig med den nya kommandouppsättningen.

## <a name="migrate-existing-scripts-to-az"></a>Migrera befintliga skript till Az

Stora uppdateringar kan vara olägliga. Men `Az`-modulen har ett kompatibilitetsläge som hjälper dig att använda befintliga skript medan du arbetar med uppdateringar till den nya syntaxen. Använd `Enable-AzureRmAlias`-cmdleten för att aktivera `AzureRM`-kompatibilitetsläget. Denna cmdlet definierar `AzureRM`-cmdlet-namn som alias för de nya `Az`-cmdlet-namnen.

De nya cmdlet-namnen har utformats för att vara lätta att lära sig. I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`. Det gamla kommandot `New-AzureRmVm` har till exempel blivit `New-AzVm`.

En fullständig beskrivning av migreringsprocessen finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Stöd för AzureRM i framtiden

Den befintliga `AzureRM`-modulen får inte längre nya cmdletar eller funktioner när `Az` version 1.0 släpps i december 2018. `AzureRM` underhålls emellertid fortfarande officiellt och får felkorrigeringar. Om du vill hålla dig uppdaterad med de senaste Azure-tjänsterna och -funktionerna bör du byta till `Az`-modulen.