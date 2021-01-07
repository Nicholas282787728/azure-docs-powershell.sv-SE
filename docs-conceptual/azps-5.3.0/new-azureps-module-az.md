---
title: Introduktion till Azure Az PowerShell-modulen
description: Vi presenterar Az PowerShell-modulen. Modulen ersätter AzureRM PowerShell-modulen och rekommenderas för interaktion med Azure.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 9021a1d8fdc73aedb87b17631f8e67cb8ef79166
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "97894101"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Introduktion till Azure Az PowerShell-modulen

## <a name="overview"></a>Översikt

Az PowerShell-modulen är en uppsättning cmdlets för hantering av Azure-resurser direkt från PowerShell. PowerShell har kraftfulla automatiseringsfunktioner som underlättar hanteringen av Azure-resurser exempelvis i kontexten för en CI/CD-pipeline.

Az PowerShell-modulen ersätter AzureRM och är den rekommenderade versionen för interaktion med Azure.

Du kan använda Az PowerShell-modulen genom att göra något av följande:

* [Installera Az PowerShell-modulen via PowerShellGet](install-az-ps.md) (rekommenderat alternativ).
* [Installera Az PowerShell-modulen med MSI](install-az-ps-msi.md).
* [Använd Azure Cloud Shell](/azure/cloud-shell/overview).
* [Använd Az PowerShell Docker-containern](azureps-in-docker.md).

## <a name="features"></a>Funktioner

Az PowerShell-modulen har följande fördelar:

* Säkerhet och stabilitet
  * Kryptering av tokencache
  * Förhindrande av attacktypen man-in–the-middle
  * Stöd för autentisering med ADFS 2019
  * Autentisering med användarnamn och lösenord i PowerShell 7
  * Stöd för funktioner som Kontinuerlig tillgänglighetskontroll (kommer 2021)
* Stöd för alla Azure-tjänster
  * Alla allmänt tillgängliga Azure-tjänster har en motsvarande PowerShell-modul som stöds
  * Flera felkorrigeringar och uppgraderingar av API-versioner sedan AzureRM
* Nya funktioner
  * Stöd i Cloud Shell och på alla plattformar
  * Kan hämta och använda åtkomsttoken för åtkomst till Azure-resurser
  * Cmdlet som är tillgänglig för avancerade REST-åtgärder med Azure-resurser

> [!NOTE]
> PowerShell 7 och senare är den rekommenderade versionen av PowerShell för användning med Az PowerShell på alla plattformar.

Az PowerShell-modulen baseras på .NET Standard-biblioteket och fungerar med PowerShell 7 och senare på alla plattformar, t.ex. Windows, macOS och Linux. Den är också kompatibel med Windows PowerShell 5.1.

Vår ambition är att alla plattformar ska ha stöd för Azure och att alla Az PowerShell-moduler ska vara plattformsoberoende.

## <a name="upgrade-your-environment-to-az"></a>Uppgradera din miljö till Az

För att dra nytta av de senaste Azure-funktionerna i PowerShell rekommenderar vi att du migrerar till Az-modulen. Om du inte är redo att ersätta AzureRM med Az-modulen finns det ett par alternativ för att experimentera med Az:

* Du kan använda en `PowerShell`-miljö med [Azure Cloud Shell](/azure/cloud-shell/overview). Azure Cloud Shell är en webbläsarbaserad skalmiljö där Az-modulen redan är installerad och `Enable-AzureRM`-kompatibilitetsalias aktiverade.
* Behåll AzureRM-modulen i Windows PowerShell 5.1 och installera Az-modulen i PowerShell 7 eller senare. Windows PowerShell 5.1 och PowerShell 7 och senare använder separata samlingar med moduler. Följ anvisningarna för att installera den [senaste versionen av PowerShell](/powershell/scripting/install/installing-powershell) och [installera sedan Az-modulen](install-az-ps.md) från PowerShell 7 eller senare.

Så uppgraderar du från en befintlig AzureRM-installation:

1. [Avinstallera Azure PowerShell AzureRM-modulen](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Installera Azure PowerShell Az-modulen](install-az-ps.md)
1. **VALFRITT**: Aktivera kompatibilitetsläge för att lägga till alias för AzureRM-cmdletar med [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) medan du bekantar dig med den nya kommandouppsättningen. Mer information finns i nästa avsnitt och i [Starta migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Migrera befintliga skript från AzureRM till Az

Om dina skript fortfarande baseras på AzureRM-modulen har vi flera resurser som hjälper dig med migreringen:

* [Kom igång med migrering från AzureRM till Az](migrate-from-azurerm-to-az.md)
* [Fullständig lista över icke-bakåtkompatibla ändringar från AzureRM till Az 1.0.0](migrate-az-1.0.0.md)
* Cmdleten [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Support

Az är den mest aktuella PowerShell-modulen för Azure. Problem eller önskemål om funktioner kan loggas direkt på [GitHub-lagringsplatsen](https://github.com/Azure/azure-powershell) eller via Microsofts support om du har ett supportavtal. Nya efterfrågade funktioner implementeras i den senaste versionen av Az. Korrigeringar av kritiska problem implementeras i de två senaste versionerna av Az.

Inga nya cmdletar eller funktioner kommer att ges ut för AzureRM, Officiellt underhålls AzureRM-modulen fortfarande och kritiska korrigeringar erbjuds till slutet av februari 2021.

## <a name="data-collection"></a>Datainsamling

Azure PowerShell samlar in telemetridata som standard. Microsoft samlar in data för att upptäcka användningsmönster, identifiera vanliga problem och förbättra upplevelsen av Azure PowerShell.
Microsoft Azure PowerShell samlar inte in privata eller personliga data. Användningsdata hjälper oss att identifiera problem, t.ex. cmdlets som inte ger väntat resultat, och att prioritera vårt arbete.

Även om vi har stor nytta av insikterna från dessa data, förstår vi att inte alla vill skicka sina användningsdata. Du kan inaktivera datainsamling med cmdleten [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection). Du kan också läsa vår [sekretesspolicy](https://privacy.microsoft.com/privacystatement) om du vill ha mer information.
