---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Lär dig vilka steg du följer och vilka verktyg du använder för att migrera Azure PowerShell-skript från AzureRM till den nya Az PowerShell-modulen.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/1/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: bc37d0b73db0e6df226788795730730c077fcefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856780"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrera Azure PowerShell från AzureRM till Az

Alla versioner av AzureRM PowerShell-modulen är inaktuella. [Az PowerShell-modulen](install-az-ps.md) är nu den rekommenderade PowerShell-modulen för att interagera med Azure.

## <a name="why-a-new-module"></a>Varför en ny modul?

Den största och viktigaste ändringen är att [PowerShell](/powershell/scripting/overview), som baseras på .NET Standard-biblioteket, har varit en plattformsoberoende produkt från första början.

Precis som med PowerShell-språket är vår ambition att alla plattformar ska ha stöd för Azure. Därför behövde vi uppdatera Azure PowerShell-modulerna så att de använder .NET Standard och är kompatibla med PowerShell Core. I stället för att göra omfattande ändringar i den befintliga AzureRM-modulen valde vi att skapa Az-modulen.

Utvecklingen av en ny modul innebar dessutom att våra ingenjörer kunde skapa en enhetlig design och namnge cmdlets och moduler på ett konsekvent sätt. Alla moduler börjar nu med `Az.`-prefixet och alla cmdlets använder `Verb-AzNoun`-namngivningskonventionen. Tidigare var namnen på cmdlets längre och inkonsekventa.

Antalet moduler har också reducerats: Vissa moduler som fungerade med samma tjänster har slagits ihop. Nu finns cmdlets för hanterings- och dataplanet för samma tjänst i en enda modul. För dig som manuellt hanterar beroenden och importer blir allt mycket enklare med den här konsolideringen.

Dessa viktiga ändringar gör det enklare än någonsin att använda Azure med PowerShell-cmdlets, på alla plattformar.

## <a name="upgrading-to-az-powershell"></a>Uppgradera till Az PowerShell

Skript som har skrivits för AzureRM-cmdlets fungerar inte automatiskt med Az. För att underlätta övergången utvecklades [verktyg för migrering från AzureRM till AZ](https://github.com/Azure/azure-powershell-migration). Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till Az PowerShell-modulen. Mer information om varför Az PowerShell-modulen skapades finns i [Introduktion till den nya Azure PowerShell Az-modulen](new-azureps-module-az.md).

De nya cmdlet-namnen har utformats för att vara lätta att lära sig. I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`. Till exempel har den gamla cmdleten `New-AzureRMVm` blivit `New-AzVm`.
Migreringen handlar dock inte bara om att bekanta sig med nya cmdlet-namn. Det finns omdöpta moduler, parametrar och andra viktiga ändringar.

En fullständig lista över icke-bakåtkompatibla ändringar mellan AzureRM och Az finns i de [fullständiga ändringarna från AzureRM till Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Se till att befintliga skript fungerar med den senaste versionen av AzureRM

Innan du påbörjar migreringen bör du kontrollera vilka versioner av AzureRM som finns installerade på datorn.
Du kan då se till att skripten redan körs med den senaste versionen, och du ser vilka versioner av AzureRM som behöver avinstalleras.

Om du vill kontrollera vilka versioner av AzureRM du har installerade kör du följande exempel:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Den **senaste** tillgängliga versionen av AzureRM är **6.13.1**. Om du inte har den här versionen kan de befintliga skripten behöva ytterligare modifieringar för att de ska fungera med Az-modulen, förutom det som beskrivs i den här artikeln och i [listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md).

Om skripten inte fungerar med AzureRM 6.13.1 uppdaterar du dem enligt [migreringsguiden för AzureRM 5.x till 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Om du använder en tidigare version av AzureRM-modulen finns det migreringsguider för varje större version.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Alternativ 1 (rekommenderas): Migrera PowerShell-skript automatiskt

Det här rekommenderade alternativet minimerar arbetet med att migrera AzureRM-skript till Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installera verktygen för migrering från AzureRM till Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Konvertera dina skript automatiskt

Med verktygen för migrering från AzureRM till Az kan du skapa en plan för att bestämma vilka ändringar som ska utföras för dina skript innan du ändrar dem och innan du installerar Az PowerShell-modulen.

Snabbstarten [Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen](quickstart-migrate-azurerm-to-az-automatically.md) vägleder dig genom hela processen med att uppdatera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Alternativ 2: Använd kompatibilitetsläge med Enable-AzureRmAlias

Az-modulen har ett kompatibilitetsläge för befintliga skript medan du arbetar med uppdateringar till den nya syntaxen. Cmdleten [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) aktiverar ett kompatibilitetsläge via alias. Det här läget gör att du kan använda befintliga skript med minimal modifiering under tiden som du migrerar till Az. Som standard aktiverar `Enable-AzureRmAlias` bara kompatibilitetsalias för den aktuella PowerShell-sessionen. Använd dess `Scope`-parameter om du vill bevara kompatibilitetsalias mellan PowerShell-sessioner. Mer information finns i [referensdokumentation för Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Även om cmdlet-namnen har alias kan det finnas nya (eller omdöpta) parametrar och ändrade returvärden för Az-cmdletar. Tro inte att migreringen är klappad och klar bara för att du aktiverar alias! I den [fullständiga listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md) ser du var skripten kan kräva uppdateringar.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Alternativ 3: Migrera dina skript i Visual Studio Code med Azure PowerShell-tillägget

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Installera Azure PowerShell-tillägget för Visual Studio Code

Installera [Azure PowerShell-tillägget för VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>Konvertera dina skript manuellt

1. Läs in ditt AzureRM-skript i VSCode
2. Starta migreringen genom att öppna kommandopaletten `Ctrl+Shift+P` och välja `Migrate Azure PowerShell script`
3. Välj källversionen `AzureRM`
4. Följ de rekommenderade åtgärderna för alla understrukna kommandon eller parametrar.

## <a name="next-steps"></a>Nästa steg

[Avinstallera AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
[Installera Azure PowerShell](install-az-ps.md)
