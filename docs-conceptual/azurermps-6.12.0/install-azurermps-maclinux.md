---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273811"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installera Azure PowerShell på macOS eller Linux

På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6. Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core. En .NET Standard-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.

> [!NOTE]
> För tillfället är Azure PowerShell för .NET Standard fortfarande i betaversion.
> Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.
>
> * [Problem med Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installera PowerShell Core

Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.
Detaljerade anvisningar finns i följande artikel:

* [Installera PowerShell Core på macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installera PowerShell Core på Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Installera Azure PowerShell för .NET Standard

> [!IMPORTANT]
> Modulen `AzureRM` som beskrivs i andra artiklar fungerar inte med PowerShell Core.
> Du måste installera modulen `Az` för att få tillgång till Azure PowerShell-funktioner i PowerShell Core.

I PowerShell Core är modulen PowerShellGet redan installerad. Starta PowerShell med kommandot:

```bash
pwsh
```

Kör följande kommando för att installera Azure PowerShell:

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> Om ett behörighetsfel uppstår när du försöker installera modulen kan du behöva köra PowerShell i läget för superanvändare för att installera moduler.
>
> ```bash
> sudo pwsh
> ```

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

## <a name="enable-aliases"></a>Aktivera alias

För kompatibilitet med den befintliga modulen `AzureRM` kan den nya modulen `Az` skapa bakåtkompatibla alias för `AzureRM`-cmdletar. Innan du använder modulen för första gången bör du konfigurera dessa alias med följande kommando:

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Då konfigureras alias endast för den aktuella användaren. Cmdlet-hjälpen innehåller andra värden som kan anges för `-Scope` för att konfigurera alias.

> [!NOTE]
> Om ett sökvägsfel uppstår bör du kontrollera att sökvägen finns i ditt lokala system. För omfattningen `CurrentUser` kan det här felet lösas genom att köra följande kommando i `bash`:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Logga in

Du måste läsa in `Az` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell. Du behöver __inte__ ha några utökade privilegier för att importera en modul.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `Az` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux. Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="next-steps"></a>Nästa steg

Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).
