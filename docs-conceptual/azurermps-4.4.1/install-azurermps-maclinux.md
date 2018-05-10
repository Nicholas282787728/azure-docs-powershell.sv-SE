---
title: Installera och konfigurera Azure PowerShell på macOS och Linux | Microsoft Docs
description: Så här installerar och konfigurerar du Azure PowerShell på macOS och Linux för första gången.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Installera och konfigurera Azure PowerShell på macOS och Linux

Nu är det möjligt att installera PowerShell Core v6 och Azure PowerShell på andra plattformar än Windows-plattformar.
Processen för att installera Azure PowerShell på macOS och Linux är ungefär densamma som för Windows, men du måste först installera PowerShell Core v6.

> [!NOTE]

> För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.
> De här produkterna har begränsad support. Skicka gärna in ärenden till GitHub om du har problem eller upptäcker buggar.
>
> * [Problem med PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problem med Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Steg 1: Installera PowerShell Core v6

Processen för att installera PowerShell Core v6 varierar beroende på måloperativsystem.
Det går att installera PowerShell Core v6 på Windows, men den här artikeln handlar om macOS och Linux. Om du vill använda Azure PowerShell på Windows kan du läsa artikeln om att [installera](./install-azurerm-ps.md) på Windows.

Processen för att installera **PowerShell Core v6** på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.
Detaljerade anvisningar finns i följande artikel:

- [Installera PowerShell Core på macOS och Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Steg 2: Installera Azure PowerShell för .NET Core

I PowerShell Core v6 är modulen PowerShellGet redan installerad. Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet. Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Steg 3: Läs in modulen AzureRM.Netcore

När modulen har installerats måste du läsa in modulen i din PowerShell-session. Moduler läses in med `Import-Module`-cmdleten enligt följande:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:

```powershell
Login-AzureRMAccount
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
