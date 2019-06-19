---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ead6c48496c646b5184f88aeac64fbe650be17c4
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2019
ms.locfileid: "67193183"
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
> Det går __inte__ både modulen AzureRM och modulen Az installerade samtidigt för PowerShell 5.1 för Windows. Om du vill behålla AzureRM på datorn installerar du Az-modulen för PowerShell Core 6.x eller senare. För att göra det [installerar du PowerShell Core 6.x eller senare](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) och följer instruktionerna i PowerShell Core-terminalen.

Om du vill installera moduler med globalt omfång behöver du ha utökade privilegier för att installera moduler från PowerShell-galleriet. Du installerar Azure PowerShell genom att köra följande kommando i en upphöjd session (”Kör som administratör” på Windows eller med superanvändarprivilegier på macOS eller Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Om du inte har åtkomst till administratörsprivilegier kan du installera för den aktuella användaren genom att lägga till argumentet `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
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
> Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`. Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

På grund av hur Az-modulen är paketerad uppdaterar kommandot [Update-Module](/powershell/module/powershellget/update-module) inte installationen på rätt sätt. Az är tekniskt sett en metamodul. Den omfattar alla undermoduler som innehåller cmdletar för att interagera med Azure-tjänster. Det innebär att om du vill uppdatera Azure PowerShell-modulen behöver du __installera om__, snarare än att bara __uppdatera__. Det gör du på samma sätt som när du installerar, men du kan behöva lägga till argumentet `-Force`:

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
