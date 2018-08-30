---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018647"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installera Azure PowerShell på macOS eller Linux

På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6. Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core. En speciell .NET Core-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.

> [!NOTE]
> För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.
> De här produkterna har begränsad support. Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.
>
> * [Problem med PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problem med Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installera PowerShell Core

Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.
Detaljerade anvisningar finns i följande artikel:

* [Installera PowerShell Core på macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installera PowerShell Core på Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installera Azure PowerShell för .NET Core

I PowerShell Core är modulen PowerShellGet redan installerad. Du måste ha utökade privilegier för att installera moduler i PowerShell, så du måste starta din session som en superanvändare:

```bash
sudo pwsh
```

Kör följande kommando för att installera Azure PowerShell:

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Modulen `AzureRM` som beskrivs i andra artiklar är inte byggd för .NET Core och fungerar inte med PowerShell Core. Både `AzureRM` och `AzureRM.NetCore` använder samma cmdlet-namn, så den enda skillnaden är namnet på den samlade modulen och vilken .NET-version de är skapade för att användas med.

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

## <a name="sign-in"></a>Logga in

Du måste läsa in `AzureRM.Netcore` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell. Du behöver __inte__ ha några utökade privilegier för att importera en modul.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux. Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="available-cmdlets"></a>Tillgängliga cmdlet:ar

Azure PowerShell-moduler för .NET Core håller fortfarande på att utvecklas. De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna. Följande funktioner är implementerade i AzureRM.Netcore-moduler:

* Kontohantering
  * Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory
  * Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext
* Miljö
  * Hämta andra Microsoft Azure-miljöer
  * Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)
* Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.
  * Virtuell dator
  * App Service (Websites)
  * SQL Database
  * Storage
  * Nätverk

## <a name="next-steps"></a>Nästa steg

Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).
