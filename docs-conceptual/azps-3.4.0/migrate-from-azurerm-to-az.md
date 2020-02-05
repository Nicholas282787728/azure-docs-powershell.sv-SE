---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002817"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrera Azure PowerShell från AzureRM till Az

Az-modulen har funktionsparitet med AzureRM, men använder kortare och mer konsekventa cmdlet-namn.
Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen. För att underlätta övergången erbjuder Az verktyg så att du kan köra dina befintliga skript med hjälp av AzureRM. Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till den nya modulen.

En fullständig lista över icke-bakåtkompatibla ändringar mellan AzureRM och Az finns i de [fullständiga ändringarna från AzureRM till Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Se till att befintliga skript fungerar med den senaste versionen av AzureRM

Innan du påbörjar migreringen bör du kontrollera vilka versioner av AzureRM som finns installerade på datorn. Du kan då se till att skripten redan körs med den senaste versionen, och du ser vilka versioner av AzureRM som behöver avinstalleras.

Om du vill kontrollera vilka versioner av AzureRM du har installerade kör du följande kommando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

Den __senaste__ tillgängliga versionen av AzureRM är __6.13.1__. Om du inte har den här versionen kan de befintliga skripten behöva ytterligare modifieringar för att de ska fungera med Az-modulen, förutom det som beskrivs här och i [listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md).

Om skripten inte fungerar med AzureRM 6.13.1 uppdaterar du dem enligt [migreringsguiden för AzureRM 5.x till 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Om du använder en tidigare version av AzureRM-modulen finns det migreringsguider för varje större version.

## <a name="uninstall-azurerm"></a>Avinstallera AzureRM

Det är inte säkert att Az-modulen är kompatibel med befintliga AzureRM-installationer i PowerShell 5.1 för Windows. Innan du installerar Az-modulen bör du [avinstallera AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Om du inte är vill ta bort AzureRM-modulen från datorn kan du installera Az-modulen för [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x eller senare i stället. PowerShell Core och PowerShell 5.1 för Windows använder ett annat modulbibliotek, som inte orsakar konflikter. Du kan fortfarande [aktivera alias](#enable-azurerm-compatibility-aliases) i PowerShell Core.

## <a name="install-the-azure-powershell-az-module"></a>Installera Azure PowerShell Az-modulen

Första steget är att installera Az-modulen på din plattform. När du installerar Az bör du avinstallera AzureRM. I följande steg får du lära dig hur du fortsätter att köra dina befintliga skript och aktiverar kompatibilitet för gamla cmdlet-namn.

När du vill installera Azure PowerShell Az-modulen följer du i [Installera Az-modulen](install-az-ps.md).

> [!NOTE]
> I det här läget kan du vilja köra cmdleten [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) som finns i Az-modulen, för att se till att alla versioner av AzureRM har avinstallerats och att de inte orsakar konflikter.

## <a name="enable-azurerm-compatibility-aliases"></a>Aktivera AzureRM-kompatibilitetsalias

När AzureRM har avinstallerats och skripten fungerar med den senaste AzureRM-versionen är nästa steg att aktivera kompatibilitetsläget för Az-modulen. Kompatibilitet aktiveras med kommandot:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Alias gör det möjligt att använda äldre cmdlet-namn med Az-modulen installerad. Dessa alias skrivs till profilen för det valda omfånget. Om det inte finns någon profil skapas en.
När du använder ett `-Scope` som är bredare än `CurrentUser` så krävs rätt behörigheter för att skapa eller uppdatera motsvarande profilfil.

> [!IMPORTANT]
> __Det är bara__ cmdlet-namn som har alias. Modulnamn har inte det. Om du använder `#Requires`, `Import-Module`, beroendelistor i `.psd1` eller helt kvalificerade cmdlet-namn ska du se till att du migrerar dem i det här läget genom att följa processerna i [listan med icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md) för modulnamnen.

> [!WARNING]
>
> Du kan använda ett annat `-Scope` för det här kommandot, men det rekommenderas inte. Alias skrivs till användarprofilen för det valda omfånget, så fortsätt att aktivera dem för ett så begränsat omfång som möjligt. Aktivering av alias i hela systemet kan orsaka problem för andra användare som har AzureRM installerat i sitt lokala omfång.

När aliasläget har aktiverats kör du skripten igen för att bekräfta att de fortfarande fungerar som förväntat.
Vissa parameternamn har ändrats, lagts till eller gjorts obligatoriska av Az-modulen. Utdatatyperna för cmdletar kan ha ändrats också. De här ändringarna finns i [listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md).

## <a name="update-cmdlets-modules-and-parameters"></a>Uppdatera cmdletar, moduler och parametrar

När skript uppdateras och körs under alias kan du ta dig tid att uppdatera dem och använda nya cmdletar och dra nytta av andra ändringar som nya funktioner. För de flesta skript behöver du bara uppdatera cmdlet-namnen [ enligt det nya cmdlet-namngivningsschemat i Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). Det kan också finnas andra ändringar som du behöver göra för att få skripten att fungera, beroende på vad de gör och vilka Azure PowerShell-funktioner de dra nytta av.

[Blob Storage-cmdletarna](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) har till exempel arbetats om helt och använder en ny asynkron modell. Skript som använder dem kräver mer uppdateringsarbete än de där de enda viktiga ändringarna var cmdlet-namn.

Även om du hittills bara behövt göra små, enkla ändringar i skripten, eller om de fungerar helt utan ändringar när alias är aktiverade, bör du läsa [listan över alla icke-bakåtkompatibla ändringar i Az 1.0.0](migrate-az-1.0.0.md) och se till att du inte förlitar dig på ”transparenta” beteenden för alias, vilka kan försvinna när du ändrar cmdlet-namnen och inaktiverar alias.

## <a name="disable-aliases"></a>Inaktivera alias

När du har slutfört migreringen och inte längre förlitar dig på aliasbeteende rekommenderar vi att du inaktiverar alias. Det gör du med cmdleten [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> När du kör den här cmdleten ska du __se till__  att du anropar den för varje `-Scope` som `Enable-AzureRmAlias` anropades för. Det kan annars fortfarande finnas skript på datorn som förlitar sig på aliasbeteenden.
