---
title: Installera och konfigurera Azure PowerShell Service Management-modulen | Microsoft Docs
description: Installera och konfigurera Azure PowerShell för första gången.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 21b61a2f91b4f6211fbeec8ba234782355b9a4b3
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024774"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Installera Azure PowerShell Service Management-modulen

Vi rekommenderar att du installerar Azure PowerShell från [PowerShell-galleriet](https://www.powershellgallery.com/).

## <a name="step-1-install-powershellget"></a>Steg 1: Installera PowerShellGet

Du måste ha modulen PowerShellGet för att kunna installera objekt från PowerShell-galleriet. Kontrollera att du har rätt version av PowerShellGet och att datorn uppfyller övriga systemkrav. Kör följande kommando för att se om du har PowerShellGet installerat på datorn.

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
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

Azure PowerShell-modulerna uppdateras kontinuerligt. Om du märker att onlinehjälpen för cmdletar omfattar cmdletar eller parametrar som inte finns i din modul bör du hämta och installera den senaste versionen av modulen. Du kan hitta modulens version genom att skriva in: `(Get-Module Azure).Version`.

Om du vill ha exempelskript som kan hjälpa dig att automatisera vissa av de vanliga uppgifterna i Azure kan du se [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).

Allmän information om installation, inlärning, användning och anpassning av Windows PowerShell finns i [Skript med Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).

### <a name="how-to-get-powershellget"></a>Hämta PowerShellGet

|OS-version|Installationsinstruktioner|
|---|---|
|Jag har Windows 10 eller Windows Server 2016|Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet|
|Jag vill uppgradera till PowerShell 5|[Installera den senaste versionen av WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Jag använder en Windows-version med PowerShell 3 eller PowerShell 4|[Hämta PackageManagement-moduler](http://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### Kontrollera Azure PowerShell-versionen

Flera versioner av Azure PowerShell stöds, men vi rekommenderar att du uppgraderar till den senaste versionen så snabbt som möjligt. Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-Module AzureRM` från kommandoraden.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
