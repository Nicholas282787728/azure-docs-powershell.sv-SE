---
title: Installera Azure PowerShell på Windows med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5f7f65aa25d86feb77a85fc28d122118216542cc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588051"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installera Azure PowerShell på Windows med PowerShellGet

Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö med hjälp av PowerShellGet. PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).

Anvisningar för hur du installerar Azure PowerShell på andra plattformar finns i [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).

Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell. Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.

## <a name="requirements"></a>Krav

Du behöver PowerShellGet version 1.1.2.0 eller senare för att installera Azure PowerShell. Kör följande kommando för att kontrollera om det är tillgängligt på ditt system:

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Nu bör du se utdata som ser ut ungefär så här:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Kör följande kommando om du behöver uppdatera din installation av PowerShellGet:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Följ anvisningarna i tabellen nedan för ditt system om du inte har PowerShellGet installerat.

|Scenario|Installationsinstruktioner|
|---|---|
|Windows 10<br/>Windows Server 2016|Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet|
|Uppgradera till PowerShell 5| <ol><li>[Installera den senaste versionen av WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Kör följande kommando:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows med PowerShell 3 eller PowerShell 4|<ol><il>[Hämta PackageManagement-modulerna](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Kör följande kommando:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> För att kunna använda PowerShellGet, krävs en körningsprincip som låter dig köra skript. Mer information om PowerShell-körningsprincipen finns i [Om körningsprinciper](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework. Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core. Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

Du behöver ha utökade behörigheter för att installera moduler från PowerShell-galleriet. Kör följande kommando i en upphöjd session för att installera Azure PowerShell:

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

Modulen `AzureRM` är en sammanslagen modul för Azure PowerShell-cmdletar. När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.

## <a name="sign-in"></a>Logga in

Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module). Det här kommandot avinstallerar __inte__ tidigare versioner.

```powershell-interactive
Update-Module -Name AzureRM
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.

## <a name="use-multiple-versions-of-azure-powershell"></a>Använd flera versioner av Azure PowerShell

Det är möjligt att installera flera versioner av Azure PowerShell. Du kan behöva mer än en version om du arbetar med lokala Azure Stack-resurser, kör en äldre version av Windows så att du inte kan uppdatera till PowerShell 5.0 eller använder den klassiska Azure-distributionsmodellen. Ange argumentet `-RequiredVersion` när du installerar för att installera en äldre version.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

När du läser in Azure PowerShell-modulen läses den senaste versionen in som standard. Ange argumentet `-RequiredVersion` för att läsa in en annan version.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).
Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Nästa steg

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.
