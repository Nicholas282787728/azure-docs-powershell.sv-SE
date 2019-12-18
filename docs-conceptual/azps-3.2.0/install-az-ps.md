---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182238"
---
# <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet. De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar. För Az-modulen kan för närvarande inga andra installationsmetoder användas.

## <a name="requirements"></a>Krav

Azure PowerShell fungerar med PowerShell 5.1 och senare i Windows och med PowerShell Core 6.x och senare på valfri plattform. Om du är osäker på om du har PowerShell, eller macOS eller Linux, [installerar du senaste versionen av PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Köra Azure PowerShell på PowerShell 5.1 på Windows:

1. Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.
2. Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).

Det finns inga ytterligare krav för Azure PowerShell när du använder PowerShell Core.

## <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

> [!WARNING]
> Det går __inte__ både modulen AzureRM och modulen Az installerade samtidigt för PowerShell 5.1 för Windows. Om du vill behålla AzureRM på datorn installerar du Az-modulen för PowerShell Core 6.x eller senare. För att göra det [installerar du PowerShell Core 6.x eller senare](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) och följer instruktionerna i PowerShell Core-terminalen.

Den rekommenderade installationsmetoden är att begränsa installationen till den aktiva användaren:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Om du vill installera för alla användare i ett system krävs administratörsbehörighet. I macOS eller Linux kör du som administratör eller med `sudo`-kommandot i en PowerShell-session med förhöjd behörighet:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar. När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.

## <a name="install-offline"></a>Installera offline

I en del miljöer går det inte att ansluta till PowerShell-galleriet. I sådana situationer kan du fortfarande installera offline på något av dessa sätt:

* Ladda ned modulerna till en annan plats och använd det som en installationskälla på ditt nätverk. Det här kan vara komplicerat, men då kan du cachelagra PowerShell-moduler på en enda server eller filresurs så att de kan distribueras med PowerShellGet till frånkopplade system. Läs artikeln om hur du [arbetar med lokala PowerShellGet-lagringsplatser](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) för mer information om hur du konfigurerar lokala lagringsplatser och installerar på frånkopplade system.
* [Ladda ned Azure PowerShell MSI](install-az-ps-msi.md) till en dator som är ansluten till nätverket, och kopiera sedan installationsprogrammet till system som saknar åtkomst till PowerShell-galleriet. Tänk på att MSI-installationsprogrammet endast fungerar för PowerShell 5.1 på Windows.
* Spara modulen med [Save-Module](/powershell/module/PowershellGet/Save-Module) till en filresurs, eller spara den till en annan källa och kopiera den manuellt till andra datorer:
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Felsökning

Här är några vanliga problem som kan uppstå när du installerar Azure PowerShell-modulen. Om du stöter på ett problem som inte tas upp här kan du [öppna ett ärende på GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Proxy blockerar anslutning

Om du får felmeddelanden från `Install-Module` som indikerar att det inte går att nå PowerShell Gallery kan du hindras av en proxy. Olika operativsystem har olika krav för att konfigurera en systemomfattande proxy. Det tas inte upp i detalj här. Systemadministratören kan ge dig information om proxyinställningarna och hur du konfigurerar dem för operativsystemet.

Själva PowerShell kan inte konfigureras för att använda den här proxyn automatiskt. Med PowerShell 5.1 och senare konfigurerar du proxyn för PowerShell-sessionen med följande kommando:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Om autentiseringsuppgifter för operativsystemet är rätt konfigurerade dirigeras PowerShell-begärandena genom proxyn.
För att den här inställningen ska finnas kvar mellan sessionerna lägger du till kommandot i en [PowerShell profil](/powershell/module/microsoft.powershell.core/about/about_profiles).

För att du ska kunna installera paketet måste proxyservern tillåta HTTPS-anslutningar till följande adress:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Logga in

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Om du har inaktiverat modulen för automatisk inläsning, kan du importera den manuellt med `Import-Module Az`. Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

På grund av hur Az-modulen är paketerad uppdaterar kommandot [Update-Module](/powershell/module/powershellget/update-module) inte installationen på rätt sätt. När du installerar AZ-modulen samlar den in och installerar alla sina beroende undermoduler och tillhandahåller cmdletarna för varje tjänst.
Det innebär att om du vill uppdatera Azure PowerShell-modulen behöver du __installera om__, snarare än att bara __uppdatera__. Det gör du på samma sätt som när du installerar, men du kan behöva lägga till argumentet `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Det här kan skriva över installerade moduler, men du kan fortfarande ha äldre versioner kvar på datorn.
Om du vill ta bort äldre versioner av Azure PowerShell från ditt system läser du [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Använd flera versioner av Azure PowerShell

Det är möjligt att installera fler än en version av Azure PowerShell. Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.

Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion`:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).
Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Nästa steg

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.
Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).
