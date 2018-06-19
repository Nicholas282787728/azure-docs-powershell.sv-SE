---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323177"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installera Azure PowerShell på macOS eller Linux

På plattformar som inte använder Windows är det möjligt att både köra Azure PowerShell och PowerShell Core v6. Den här produkten är utformad på .NET Core istället för det vanliga Azure PowerShell som är skapat på .NET Framework för Windows. Den kan köras på alla plattformar som har stöd för körning på .NET Core.

> [!NOTE]
> För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.
> De här produkterna har begränsad support. Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.
>
> * [Problem med PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problem med Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>Installera PowerShell Core v6

Processen för att installera PowerShell Core v6 på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.
Detaljerade anvisningar finns i följande artikel:

- [Installera PowerShell Core på macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Installera PowerShell Core på Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installera Azure PowerShell för .NET Core

I PowerShell Core v6 är modulen PowerShellGet redan installerad. Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet. Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Läs in modulen AzureRM.Netcore

När modulen har installerats måste du läsa in modulen i din PowerShell-session. Moduler läses in med `Import-Module`-cmdleten enligt följande:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:

```powershell
Connect-AzureRmAccount
```

När du har angivit kommandot ovan visas en dialogruta som ber dig att gå till `https://aka.ms/devicelogin` och ange koden som tillhandahålls.

## <a name="available-cmdlets"></a>Tillgängliga cmdlet:ar

Azure PowerShell-moduler för .NET Standard är fortfarande under utveckling. De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna. Följande funktioner är implementerade i AzureRM.Netcore-moduler:

* Kontohantering
  - Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory
  - Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext
* Miljö
  - Hämta andra Microsoft Azure-miljöer
  - Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)
* Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.
  - Virtuell dator
  - App Service (Websites)
  - SQL Database
  - Storage
  - Nätverk

## <a name="next-steps"></a>Nästa steg

Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).
