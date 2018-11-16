---
title: Använda experimentella Azure PowerShell-moduler
description: Förstå filosofin och användningen av experimentella Azure PowerShell-moduler.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: ff58693c8ec21b7e50e37bd85975a9ae3980a5e7
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575798"
---
# <a name="using-experimental-azure-powershell-modules"></a>Använda experimentella Azure PowerShell-moduler

Med betoning på utvecklarverktyg (i synnerhet CLI:er) i Azure experimenterar Azure PowerShell-teamet med många förbättringar av Azure PowerShell.

## <a name="experimentation-methodology"></a>Metodik

För att underlätta experimenteringen skapar vi nya Azure PowerShell-moduler som implementerar befintliga Azure SDK-funktioner på nya, mer lättanvända sätt. I de flesta fall speglar cmdletar exakt befintliga cmdletar. Experimentella cmdletar tillhandahåller däremot snabba kommentarer och smartare standardvärden som gör det enklare att skapa och hantera Azure-resurser.

Dessa moduler kan vara installerade sida vid sida med befintliga Azure PowerShell-moduler. Cmdlet-namnen har kortats ned för att få kortare namn och undvika namnkonflikter med befintliga, icke-experimentella cmdletar.

De experimentella modulerna använder följande namngivningskonvention: `AzureRM.*.Experiments`. Namngivningskonventionen liknar namngivningen i förhandsversionsmoduler: `AzureRM.*.Preview`. Förhandsversionsmoduler skiljer sig från experimentella moduler. Förhandsversionsmoduler implementerar nya funktioner i Azure-tjänster som endast är tillgängliga som en förhandsversion. Förhandsversionsmoduler ersätter befintliga Azure PowerShell-moduler och använder samma cmdlet- och parameternamn.

## <a name="how-to-install-an-experimental-module"></a>Så här installerar du en experimentell modul

Experimentella moduler publiceras i PowerShell-galleriet precis som de befintliga Azure PowerShell-modulerna. Om du vill se en lista med experimentella moduler kör du följande kommando:

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

Om du vill installera den experimentella modulen ska du använda följande kommandon från en upphöjd PowerShell-session:

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Dokumentation och support

Dokumentation som ingår i installationspaketet och som du får åtkomst till med cmdlet `Get-Help`. Ingen officiell dokumentation publiceras för experimentella moduler.

Vi uppmuntrar dig att testa dessa moduler. Din feedback gör att vi kan förbättra användbarhet och svara på dina behov. Men eftersom modulerna är experimentella är supporten för dem begränsad. Frågor eller problem rapporter kan skickas genom att skapa ett [problem](https://github.com/Azure/azure-powershell/issues) i GitHub-lagringsplatsen.

## <a name="experiments-and-areas-of-improvement"></a>Experiment och förbättringsområden

Dessa förbättringar har valts ut baserat på viktiga skillnaderna i konkurrerande produkter. Azure CLI 2.0 är det till exempel viktigt att kommandon baseras på _scenarier_ snarare än _API-ytan_.
I Azure CLI 2.0 används ett antal smarta standardvärden som förenklar kom-igång-scenarier för slutanvändare.

### <a name="core-improvements"></a>Grundläggande förbättringar

Grundläggande förbättringar räknas som ”sunt förnuft” och lite experimenterande krävs för att gå vidare och implementera uppdateringarna.

- Scenario-baserade cmdletar – *<em>All</em>-cmdletar bör utformas runt scenarier, inte Azure REST-tjänsten.

- Kortare namn – Omfattar namnen på cmdletar (till exempel `New-AzureRmVM` => `New-AzVm`) och parameternamnen (till exempel `-ResourceGroupName` => `-Rg`). Använd alias för kompatibilitet med ”gamla” cmdletar. Tillhandahåll _bakåtkompatibla_ parameteruppsättningar.

- Smarta standardvärden – Skapa smarta standardvärden för att fylla i ”obligatorisk” information. Exempel:
  - Resursgrupp
  - Plats
  - Beroende resurser

### <a name="experimental-improvements"></a>Experimentella förbättringar

Experimentella förbättringar presenterat en betydande förändring som teamet vill validera via experimentering.

- Enkla typer – Skapa-scenarier bör komma bort från komplexa typer och konfigurationsobjekt. Förenkla konfigurationen till en eller två parametrar.

- ”Smart Create” – Alla skapa-scenarier som implementerar ”Smart Create” skulle inte ha _någon_ obligatorisk parameter: all nödvändig information skulle väljas av Azure PowerShell på ett smart sätt.

- Grå parametrar – I många fall skulle vissa parametrar kunna vara ”grå” eller delvis valfria. Om parametern inte anges, ska användarna tillfrågas om de vill den parameter som genererats åt dem. Det vore också rimligt att grå parametrar med användarens medgivande skulle härleda ett värde utifrån sammanhanget.
  Exempelvis kunde det vara klokt att den grå parametern föreslår det senast använda värdet.

- Switchen `-Auto` – Switchen `-Auto` skulle göra det möjligt för användare att välja _standardvärden på allt_ samtidigt som obligatoriska parametrars integritet bevaras i huvudspåret.

### <a name="feature-specific-switches"></a>Funktionsspecifika switchar

Scenariet ”Skapa webbapp” skulle till exempel kunna ha en `-Git`- eller `-AddRemote`-switch som automatiskt skulle lägga till en ”azure” fjärrlagringsplats till en befintlig git-lagringsplats.

- Inställningsbara standardvärden – Användare bör ha möjlighet att ange vissa allmänt förekommande parametrar som standardvärden, `-ResourceGroupName` och `-Location`.

- Storleksstandard – Resursers ”storlekar” kan vara förvirrande för användarna eftersom många resursproviders använder olika namn (till exempel ”Standard\_DS1\_v2” eller ”S1”). Dock är de flesta användare mer intresserade av kostnaden. Därför vore det praktiskt att definiera ”universella” storlekar utifrån ett prissättningsschema. Användare kan välja en viss storlek eller låta Azure PowerShell välja det _bästa alternativet_ utifrån resursbudgeten.

- Utdataformat – Azure PowerShell returnerar för närvarande `PSObject` och det finns lite konsolutdata. Azure PowerShell kanske behöver visa en del information för användaren om vilka ”smarta standardvärden” som används.
