---
title: Installera och konfigurera Azure PowerShell Service Management-modulen | Microsoft Docs
description: Installera och konfigurera Azure PowerShell för första gången.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 23ea4bcbd182cf1b063f2ae90921217de74a7044
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401529"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Installera Azure PowerShell Service Management-modulen

Vi rekommenderar att du installerar Azure PowerShell från [PowerShell-galleriet](https://www.powershellgallery.com/).

## <a name="step-1-install-powershellget"></a>Steg 1: Installera PowerShellGet

Du måste ha modulen PowerShellGet för att kunna installera objekt från PowerShell-galleriet. Kontrollera att du har rätt version av PowerShellGet och att datorn uppfyller övriga systemkrav. Kör följande kommando för att se om du har PowerShellGet installerat på datorn.

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

Nu bör du se utdata som ser ut ungefär så här:

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Om du inte har installerat PowerShellGet kan du läsa avsnittet [Hämta PowerShellGet](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Steg 2: Installera Azure PowerShell

Kör följande kommando från Windows PowerShell-konsolen som körs som administratör:

```powershell
Install-Module Azure
```

Azure-modulen är en sammanslagen modul för Azure Resource Manager-cmdletar. När du installerar AzureRM-modulen kommer alla övriga Azure-moduler som inte har installerats att hämtas och installeras från PowerShell-galleriet.

Azure Service Management-modulen delar beroenden med Azure PowerShell Resource Manager-modulerna. Om du har installerat Azure PowerShell Resource Manager-modulerna måste du lägga till parametern `-AllowClobber` i installationskommandot. Det tillåter att befintliga delade beroenden uppdateras. Utan den här parametern misslyckas installationen av modulen.

```powershell
Install-Module Azure -AllowClobber
```

När du har installerat den här modulen kan du importera modulen genom att köra följande kommando:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Använda cmdletar

Logga först in på ditt Azure-konto om du vill börja arbeta med cmdletar för Azure Service Management. Kör följande kommando för att logga in på ditt konto:

```powershell
Add-AzureAccount
```

När du har loggat in på Azure skapar Azure PowerShell en kontext för den angivna sessionen. Den kontexten innehåller miljö, konto, klient och prenumeration för Azure PowerShell som ska användas för alla cmdletar i den sessionen. Du är nu redo att använda modulerna nedan.

## <a name="azure-service-management-cmdlets"></a>Azure Service Management-cmdletar

Azure PowerShell-modulerna uppdateras kontinuerligt. Om du märker att onlinehjälpen för cmdletar omfattar cmdletar eller parametrar som inte finns i din modul bör du hämta och installera den senaste versionen av modulen. Du kan hitta modulens version genom att skriva in: `(Get-InstalledModule Azure).Version`.

Om du vill ha exempelskript som kan hjälpa dig att automatisera vissa av de vanliga uppgifterna i Azure kan du se [Windows Azure Script Center](https://www.windowsazure.com/documentation/scripts/).

Allmän information om installation, inlärning, användning och anpassning av Windows PowerShell finns i [Skript med Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).

### <a name="how-to-get-powershellget"></a>Hämta PowerShellGet

|OS-version|Installationsinstruktioner|
|---|---|
|Jag har Windows 10 eller Windows Server 2016|Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet|
|Jag vill uppgradera till PowerShell 5|[Installera den senaste versionen av WMF](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a>Kontrollera Azure PowerShell-versionen

Flera versioner av Azure PowerShell stöds, men vi rekommenderar att du uppgraderar till den senaste versionen så snabbt som möjligt. Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-InstalledModule Azure` från kommandoraden.

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
