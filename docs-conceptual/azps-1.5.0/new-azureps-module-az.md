---
title: Introduktion till Azure PowerShell Az-modulen
description: Vi introducerar den nya Azure PowerShell-modulen Az, som ersätter AzureRM-modulen.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882645"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduktion till den nya Azure PowerShell Az-modulen

Från och med december 2018 är Az för Azure PowerShell-modulen en allmän version och är nu den PowerShell-modulen som är avsedd för interaktion med Azure. Az erbjuder kortare kommandon, bättre stabilitet och stöd för flera plattformar. Az erbjuder också funktionsparitet och en enkel migreringsväg från AzureRM.

Az använder .NET Standard-biblioteket, vilket innebär att den körs på PowerShell 5 och PowerShell 6.
Eftersom PowerShell 6 kan köras på Linux, macOS och Windows är Azure PowerShell nu tillgängligt för alla plattformar.
Med .NET Standard kan vi förena kodbasen för Azure PowerShell med minimal inverkan på användare.

Az är en ny modul, så versionen har återställts till 1.0.0.

## <a name="upgrade-to-az"></a>Uppgradera till Az

Vi rekommenderar att alla användare uppgraderar till den nya Az-modulen. Gör så här:

* __REKOMMENDERAS__: [Avinstallera Azure PowerShell AzureRM-modulen](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Installera Azure PowerShell Az-modulen](/powershell/azure/install-az-ps)
* Aktivera kompatibilitetsläge för att lägga till alias för AzureRM-cmdletar med `Enable-AzureRMAlias` medan du bekantar dig med den nya kommandouppsättningen. Aktivera alias __endast__ om du inte har AzureRM installerat.

## <a name="migrate-existing-scripts-to-az"></a>Migrera befintliga skript till Az

Stora uppdateringar kan vara olägliga. Az-modulen har ett kompatibilitetsläge som hjälp om du vill använda befintliga skript medan du arbetar med uppdateringar till den nya syntaxen. Använd cmdleten `Enable-AzureRmAlias` för att aktivera AzureRM-kompatibilitetsläget. Denna cmdlet definierar AzureRM-cmdletnamn som alias för de nya Az-cmdletnamnen.

De nya cmdlet-namnen har utformats för att vara lätta att lära sig. I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`. Det gamla kommandot `New-AzureRMVm` har till exempel blivit `New-AzVm`.

En fullständig beskrivning av migreringsprocessen finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Stöd för AzureRM i framtiden

Den befintliga AzureRM-modulen tar inte längre emot nya cmdletar eller funktioner. AzureRM underhålls dock fortfarande officiellt och får nya buggkorrigeringar fram till december 2020. Byt till Az-modulen om du vill hålla dig uppdaterad med de senaste Azure-tjänsterna och -funktionerna.
