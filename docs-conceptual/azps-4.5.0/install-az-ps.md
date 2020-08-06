---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.openlocfilehash: caa0c2fbba8b8b7e07424481360a60f3da163e66
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566550"
---
# <a name="install-azure-powershell"></a>Installera Azure PowerShell

Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av [PowerShellGet](/powershell/scripting/gallery/installing-psget). De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.

Azure PowerShell är också tillgängligt i Azure [Cloud Shell](/azure/cloud-shell/overview) och är nu förinstallerat i [Docker-avbildningar](azureps-in-docker.md).

## <a name="requirements"></a>Krav

> [!NOTE]
> PowerShell 7.x och senare är den rekommenderade versionen av PowerShell för användning med Azure PowerShell på alla plattformar.

Azure PowerShell fungerar med PowerShell 6.2.4 och senare på alla plattformar. Modulen stöds även med PowerShell 5.1 i Windows. Installera [den senaste versionen av PowerShell](/powershell/scripting/install/installing-powershell) för ditt operativsystem. Det finns inga ytterligare krav för Azure PowerShell när du kör verktyget på PowerShell 6.2.4 och senare.

Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Använda Azure PowerShell i PowerShell 5.1 på Windows:

1. Uppdatera till [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).
   Om du använder Windows 10 version 1607 eller senare är PowerShell 5.1 redan installerat.
2. Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).
3. Kontrollera att du har den senaste versionen av PowerShellGet. Kör `Install-Module -Name PowerShellGet -Force`.

## <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

> [!WARNING]
> Det går inte att ha både modulen AzureRM och modulen Az installerade samtidigt för PowerShell 5.1 för Windows. Om du vill behålla AzureRM på datorn installerar du Az-modulen för PowerShell 6.2.4 eller senare.

Att använda PowerShellGet-cmdletar är den installationsmetod som föredras. Installera Az-modulen endast för den aktuella användaren. Detta är det rekommenderade installationsomfånget. Den här metoden fungerar på samma sätt för plattformarna Windows, macOS och Linux. Kör följande kommando från en PowerShell-session:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

Att installera modulen för alla användare i ett system kräver förhöjd behörighet. Starta PowerShell-sessionen med **Kör som administratör** i Windows eller använd kommandot `sudo` på macOS eller Linux:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar. När du installerar den laddas alla allmänt tillgängliga Az PowerShell-moduler ned så att deras cmdletar blir tillgängliga för användning.

## <a name="install-offline"></a>Installera offline

I en del miljöer går det inte att ansluta till PowerShell-galleriet. I sådana situationer kan du fortfarande installera offline på något av dessa sätt:

* Ladda ned modulerna till en annan plats i nätverket och använd den som en installationskälla.
  Med den här metoden kan du cachelagra PowerShell-moduler på en enda server eller filresurs så att de kan distribueras med PowerShellGet till frånkopplade system. Läs artikeln om hur du [arbetar med lokala PowerShellGet-lagringsplatser](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) för mer information om hur du konfigurerar lokala lagringsplatser och installerar på frånkopplade system.
* [Ladda ned Azure PowerShell MSI](install-az-ps-msi.md) till en dator som är ansluten till nätverket, och kopiera sedan installationsprogrammet till system som saknar åtkomst till PowerShell-galleriet. Tänk på att MSI-installationsprogrammet endast fungerar för PowerShell 5.1 på Windows.
* Spara modulen med [Save-Module](/powershell/module/PowershellGet/Save-Module) till en filresurs, eller spara den till en annan källa och kopiera den manuellt till andra datorer:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Felsökning

Här är några vanliga problem som kan uppstå när du installerar Azure PowerShell-modulen. Om du stöter på ett problem som inte tas upp här kan du [öppna ett ärende på GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Proxy blockerar anslutning

Om du får felmeddelanden från `Install-Module` som indikerar att det inte går att nå PowerShell Gallery kan du hindras av en proxy. Olika operativsystem och nätverksmiljöer har olika krav för att konfigurera en systemomfattande proxy. Systemadministratören kan ge dig information om proxyinställningarna och hur du konfigurerar dem för din miljö.

Själva PowerShell kan inte konfigureras för att använda den här proxyn automatiskt. Med PowerShell 5.1 och senare konfigurerar du proxyn för PowerShell-sessionen med följande kommandon:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Om autentiseringsuppgifter för operativsystemet är rätt konfigurerade dirigerar den här konfigurationen PowerShell-begärandena genom proxyn. För att den här inställningen ska finnas kvar mellan sessionerna lägger du till kommandona i en [PowerShell-profil](/powershell/module/microsoft.powershell.core/about/about_profiles).

För att du ska kunna installera paketet måste proxyservern tillåta HTTPS-anslutningar till följande adress:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Logga in

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Om du har inaktiverat modulen för automatisk inläsning, kan du importera den manuellt med `Import-Module -Name Az`.
> Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

Om du vill uppdatera en PowerShell-modul ska du använda samma metod som för att installera modulen. Om du ursprungligen till exempel använde `Install-Module` använder du [Update-Module](/powershell/module/powershellget/update-module) för att hämta den senaste versionen. Om du ursprungligen använde MSI-paketet laddar du ned och installerar det nya MSI-paketet.

PowerShellGet-cmdletar kan inte uppdatera moduler som har installerats från ett MSI-paket. MSI-paket uppdaterar inte moduler som har installerats med PowerShellGet. Om du har problem med att uppdatera med PowershellGet bör du **installera om**, i stället för **uppdatera**. Ominstallation görs på samma sätt som när du installerar, men du behöver lägga till parametern `-Force`:

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

Till skillnad från MSI-baserade installationer, tar installationer eller uppdateringar med PowerShellGet inte bort äldre versioner som kan finnas i systemet. Om du vill ta bort äldre versioner av Azure PowerShell från ditt system går du till [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md). Mer information om MSI-baserade installationer finns i [Installera Azure PowerShell med MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Använd flera versioner av Azure PowerShell

Det är möjligt att installera fler än en version av Azure PowerShell. Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.

Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.

Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av parametern `-RequiredVersion`:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a>Använd flera lagringsplatser med PowerShellGet

Parametern **Repository** krävs om du har lagt till fler lagringsplatser i PowerShellGet i ditt system och Az-modulen finns på fler än en av dem.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues). Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Efterföljande moment

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner. Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).
