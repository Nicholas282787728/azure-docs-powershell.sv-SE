---
title: Introduktion till Azure PowerShell Az-modulen
description: Vi introducerar den nya Azure PowerShell-modulen Az, som ersätter AzureRM-modulen.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 9812987dcc10bf5ef65ceef9195218c84042e114
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408912"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduktion till den nya Azure PowerShell Az-modulen

Från och med december 2018 finns Az-modulen för Azure PowerShell tillgänglig i en allmän version och är nu den PowerShell-modul som är avsedd för interaktion med Azure. Az erbjuder kortare kommandon, bättre stabilitet och stöd för flera plattformar. Az har även funktionsparitet med AzureRM, vilket underlättar migreringen.

> [!NOTE]
> PowerShell 7.x och senare är den rekommenderade versionen av PowerShell för användning med Azure PowerShell på alla plattformar.

Med den senaste Az-modulen fungerar Azure PowerShell med PowerShell 6.x och senare på alla plattformar, inklusive Windows, macOS och Linux. Modulen är också kompatibelt med PowerShell 5.1 i Windows.

Az är en ny modul, så versionen har återställts till 1.0.0.

## <a name="why-a-new-module"></a>Varför en ny modul?

Det kan vara svårt att genomföra stora uppdateringar. Det är viktigt att vi förklarar varför vi introducerar en ny uppsättning moduler, med nya cmdletar, för att interagera med Azure via PowerShell.

Den största och viktigaste ändringen är att PowerShell har varit en plattformsoberoende produkt ända sedan [PowerShell](/powershell/scripting/overview), baserat på .NET Standard-biblioteket.
Vi jobbar för att Azure ska fungera med alla plattformar. Det innebär att Azure PowerShell-modulerna behövde uppdateras för att gå att använda med .NET Standard och vara kompatibla med PowerShell Core. I stället för att genomföra omfattande ändringar på den befintliga AzureRM-modulen skapade vi Az-modulen.

Utvecklingen av en ny modul innebar dessutom att våra ingenjörer kunde skapa en enhetlig design och namnge cmdletar och moduler på ett konsekvent sätt. Alla moduler börjar nu med prefixet `Az.`. Alla cmdletar använder formen _Verb_-`Az`_Noun_ (verb och substantiv). Tidigare cmdlet-namn var längre och dessutom inkonsekventa.

Vi minskade också antalet moduler: Vissa moduler som fungerade med samma tjänster har slagits ihop. Nu ligger cmdletar för hantering och data i enskilda moduler för deras respektive tjänster. För dig som manuellt hanterar beroenden och importer blir saker och ting mycket enklare.

Genom att genomföra de här ändringarna, som krävde en ny Azure PowerShell-modul, har teamet gjort det ännu enklare att använda Azure med PowerShell-cmdletar, och på flera plattformar än tidigare.

## <a name="upgrade-to-az"></a>Uppgradera till Az

Om du vill dra nytta av de senaste Azure-funktionerna i PowerShell bör du migrera till Az-modulen så snart som möjligt. Om du inte är redo att ersätta AzureRM med Az-modulen finns det ett par alternativ för att experimentera med Az:

- Du kan använda en `PowerShell`-miljö med [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview). Azure Cloud Shell är en webbläsarbaserad skalmiljö där Az-modulen redan är installerad och `Enable-AzureRM`-kompatibilitetsalias aktiverade.
- Behåll AzureRM-modulen med PowerShell 5.1 för Windows, men installera Az-modulen för PowerShell 6.x och senare. PowerShell 5.1 för Windows och PowerShell 6.x använder separata modulsamlingar. Följ anvisningarna för att installera den [senaste versionen av PowerShell](/powershell/scripting/install/installing-powershell) och [installera sedan Az-modulen](install-az-ps.md) från PowerShell 6.x eller senare.

Så uppgraderar du från en befintlig AzureRM-installation:

1. [Avinstallera Azure PowerShell AzureRM-modulen](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Installera Azure PowerShell Az-modulen](install-az-ps.md)
3. **VALFRITT** : Aktivera kompatibilitetsläge för att lägga till alias för AzureRM-cmdletar med [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) medan du bekantar dig med den nya kommandouppsättningen. Du hittar mer information i nästa avsnitt och i [Påbörja migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Migrera befintliga skript till Az

De nya cmdlet-namnen har utformats för att vara lätta att lära sig. I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`. Det gamla kommandot `New-AzureRMVm` har till exempel blivit `New-AzVm`.
Migreringen är dock mer omfattande än nya cmdlet-namn: Det finns omdöpta moduler, parametrar och andra viktiga ändringar.

Vi har flera resurser som hjälper dig att migrera från AzureRM till Az:

- [Kom igång med migrering från AzureRM till Az](migrate-from-azurerm-to-az.md)
- [Fullständig lista över icke-bakåtkompatibla ändringar från AzureRM till Az 1.0.0](migrate-az-1.0.0.md)
- Cmdleten [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Az-modulen har ett kompatibilitetsläge för befintliga skript medan du arbetar med uppdateringar till den nya syntaxen. Med cmdleten [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) kan du använda ett kompatibilitetsläge för befintliga skript med minimala modifikationer medan du genomför den fullständiga migreringen till Az. Som standard aktiverar `Enable-AzureRmAlias` bara kompatibilitetsalias för den aktuella PowerShell-sessionen. Använd dess `Scope`-parameter om du vill bevara kompatibilitetsalias mellan PowerShell-sessioner. Mer information finns i [referensdokumentation för Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Även om cmdlet-namnen har alias kan det finnas nya (eller omdöpta) parametrar och ändrade returvärden för Az-cmdletar. Tro inte att migreringen är klappad och klar bara för att du aktiverar alias! I den [fullständiga listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md) ser du var skripten kan kräva uppdateringar.

## <a name="continued-support-for-azurerm"></a>Fortsatt stöd för AzureRM

Inga nya cmdletar eller funktioner kommer att ges ut för AzureRM, men modulen underhålls fortfarande officiellt och felkorrigeringar kommer att ges ut till och med december 2020.
