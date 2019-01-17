---
title: Använda experimentella Azure PowerShell-moduler
description: Förstå filosofin och användningen av experimentella Azure PowerShell-moduler.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342167"
---
# <a name="use-experimental-azure-powershell-modules"></a>Använda experimentella Azure PowerShell-moduler

Med betoning på utvecklarverktyg i Azure experimenterar Azure PowerShell-teamet med många förbättringar av Azure PowerShell. I den här artikeln beskrivs hur du registrerar dig för experiment med Azure PowerShell och ger feedback till utvecklingsteamet.

## <a name="experimentation-methodology"></a>Metodik

För att underlätta experimenteringen skapar vi nya Azure PowerShell-moduler som implementerar befintliga Azure SDK-funktioner på nya, mer lättanvända sätt. I de flesta fall speglar cmdletar exakt befintliga cmdletar. Experimentella cmdletar tillhandahåller däremot snabba kommentarer och smartare standardvärden som gör det enklare att skapa och hantera Azure-resurser.

Dessa moduler kan vara installerade sida vid sida med befintliga Azure PowerShell-moduler. Cmdlet-namnen har kortats ned för att få kortare namn och undvika namnkonflikter med befintliga, icke-experimentella cmdletar.

De experimentella modulerna använder följande namngivningskonvention: `Az.*.Experiments`. Namngivningskonventionen liknar namngivningen i förhandsversionsmoduler: `Az.*.Preview`. Förhandsversionsmoduler skiljer sig från experimentella moduler. Förhandsversionsmoduler implementerar nya funktioner i Azure-tjänster som endast är tillgängliga som en förhandsversion. Förhandsversionsmoduler ersätter befintliga Azure PowerShell-moduler och använder samma cmdlet- och parameternamn.

## <a name="how-to-install-an-experimental-module"></a>Så här installerar du en experimentell modul

Experimentella moduler publiceras i PowerShell-galleriet precis som de befintliga Azure PowerShell-modulerna. Om du vill se en lista med experimentella moduler kör du följande kommando:

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

Om du vill installera en experimentell modul använder cmdleten `Install-Module`.

### <a name="documentation-and-support"></a>Dokumentation och support

Dokumentation som ingår i installationspaketet och som du får åtkomst till med cmdlet `Get-Help`. Ingen officiell dokumentation publiceras för experimentella moduler.

Vi uppmuntrar dig att testa dessa moduler. Din feedback gör att vi kan förbättra användbarhet och svara på dina behov. Men eftersom modulerna är experimentella är supporten för dem begränsad. Frågor eller problem rapporter kan skickas genom att skapa ett [problem](https://github.com/Azure/azure-powershell/issues) i GitHub-lagringsplatsen.

## <a name="experiments-and-areas-of-improvement"></a>Experiment och förbättringsområden

Dessa förbättringar har valts ut baserat på viktiga skillnaderna i konkurrerande produkter. I Azure CLI är det till exempel viktigt att kommandon baseras på _scenarier_ i stället för _API-ytan_.
I Azure CLI används ett antal smarta standardvärden som förenklar kom-igång-scenarier för slutanvändare.

### <a name="core-improvements"></a>Grundläggande förbättringar

Grundläggande förbättringar räknas som ”sunt förnuft” och lite experimenterande krävs för att gå vidare och implementera uppdateringarna.

- Scenario-baserade cmdletar – **All*-cmdletar bör utformas runt scenarier, inte Azure REST-tjänsten.

- Kortare namn – Omfattar namnen på cmdletar och parametrar.
  Använd alias för kompatibilitet med ”gamla” cmdletar. Tillhandahåll _bakåtkompatibla_ parameteruppsättningar.

- Smarta standardvärden – Skapa smarta standardvärden för att fylla i ”obligatorisk” information. Exempel:
  - Resursgrupp
  - Plats
  - Beroende resurser

### <a name="experimental-improvements"></a>Experimentella förbättringar

Experimentella förbättringar presenterat en betydande förändring som teamet vill validera via experimentering.

- Enkla typer – Skapa-scenarier bör komma bort från komplexa typer och konfigurationsobjekt. Förenkla konfigurationen till en eller två parametrar.

- ”Smart Create” – Alla skapa-scenarier som implementerar ”Smart Create” skulle inte ha _någon_ obligatorisk parameter: all nödvändig information skulle väljas av Azure PowerShell på ett smart sätt.

- Grå parametrar – I många fall skulle vissa parametrar kunna vara ”grå” eller delvis valfria. Om parametern inte anges tillfrågas användaren om de vill att parametern ska genereras åt dem. Det vore också rimligt att grå parametrar med användarens medgivande skulle härleda ett värde utifrån sammanhanget.
  Exempelvis kunde det vara klokt att den grå parametern föreslår det senast använda värdet.

- Switchen `-Auto` – Switchen `-Auto` skulle göra det möjligt för användare att välja _standardvärden på allt_ samtidigt som obligatoriska parametrars integritet bevaras i huvudspåret.

### <a name="feature-specific-switches"></a>Funktionsspecifika switchar

Scenariet ”Skapa webbapp” skulle till exempel kunna ha en `-Git`- eller `-AddRemote`-switch som automatiskt skulle lägga till en ”azure” fjärrlagringsplats till en befintlig git-lagringsplats.

- Inställningsbara standardvärden – Användare bör kunna ange standardvärden för vanliga parametrar, till exempel `-ResourceGroupName` och `-Location`.

- Storleksstandard – Resursers ”storlekar” kan vara förvirrande för användarna eftersom många resursproviders använder olika namn (till exempel ”Standard\_DS1\_v2” eller ”S1”). Dock är de flesta användare mer intresserade av kostnaden. Därför vore det praktiskt att definiera ”universella” storlekar utifrån ett prissättningsschema. Användare kan välja en viss storlek eller låta Azure PowerShell välja det _bästa alternativet_ utifrån resursbudgeten.

- Utdataformat – Azure PowerShell returnerar för närvarande `PSObject` och det finns lite konsolutdata. Azure PowerShell kanske behöver visa en del information för användaren om vilka ”smarta standardvärden” som används.
