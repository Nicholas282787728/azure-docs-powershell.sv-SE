---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323279"
---
# <a name="other-installation-methods"></a>Andra installationsmetoder

Den här artikeln förklarar hur du installerar Azure PowerShell med hjälp av en hanterad tjänstidentitet eller installationsprogrammet för webbplattformen (WebPI). Du kan även köra Azure PowerShell från en Docker-behållare. Använd endast dessa installationsmetoder om de är nödvändiga för ditt system. Det kanoniska sättet att installera Azure PowerShell är med PowerShellGet. Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).

Information om hur du installerar i Linux- eller macOS-miljöer finns i [Installera Azure PowerShell på macOS eller Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Installera eller uppdatera på Windows med hjälp av installationsprogrammet för webbplattformen

Att installera den senaste versionen av Azure PowerShell från WebPI går till på samma sätt som det gjorde för tidigare versioner.
Hämta [Azure PowerShell WebPI-paketet](http://aka.ms/webpi-azps) och starta installationen.

> [!NOTE]
> Om du tidigare har installerat Azure-moduler från PowerShell-galleriet så kommer installationsprogrammet automatiskt att ta bort dem. Detta förenklar din miljö genom att se till att endast en version av Azure PowerShell är installerad. Det finns dock scenarier där du kan behöva flera versioner installerade på samma gång.
>
> PowerShell-galleriets moduler installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules`. WebPI-installationsprogrammet däremot installerar Azure moduler i `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Om ett fel inträffar under installationen kan du ta bort `Azure*`-mapparna manuellt i din `$env:ProgramFiles\WindowsPowerShell\Modules`-mapp och försöka installera igen.

När installationen är färdig bör din `$env:PSModulePath`-inställning inkludera de kataloger som innehåller Azure PowerShell-cmdletarna. Följande kommando kan användas för att kontrollera att Azure PowerShell är korrekt installerat:

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Det finns ett känt problem som kan uppstå när du installerar från WebPI. Om datorn kräver en omstart på grund av systemuppdateringar eller andra installationer kan det göra att uppdateringarna för `$env:PSModulePath` inte inkluderar sökvägen där Azure PowerShell är installerat.

När du försöker läsa in eller köra cmdletar efter installationen kan du få följande felmeddelande:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Det här felet kan korrigeras genom att starta om datorn eller importera modulen med den fullständigt kvalificerade sökvägen.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installera eller uppdatera på Windows med hjälp av MSI-paketet

Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://aka.ms/azps-release). Om du har installerat tidigare versioner av Azure-moduler så kommer installationsprogrammet automatiskt att ta bort dem. MSI-paketet installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules` men skapar inte versionsspecifika mappar.

## <a name="run-in-a-docker-container"></a>Kör i en Docker-behållare

Vi underhåller en uppsättning Docker-avbildningar som är förkonfigurerad med Azure PowerShell. Det finns två typer av behållare: de som kör traditionella PowerShell på Windows och en behållare som kör PowerShell Core på antingen Windows eller Linux.

| Miljö | Docker-avbildning |
|-------------|--------------|
| PowerShell på Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core på Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core på Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Använd `docker run -it $ImageName` för att hämta en interaktiv terminal och köra någon av dessa behållare. Om du till exempel vill köra PowerShell Core på Linux-behållare använder du:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Om du vill köra en Windows-behållare i Docker måste OS-värden vara Windows och Docker måste konfigureras för att köra Windows-behållare. Mer information om att växla mellan Windows- och Linux-miljöer i Docker finns i Docker-dokumentationen [Växla mellan Windows- och Linux-behållare](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).