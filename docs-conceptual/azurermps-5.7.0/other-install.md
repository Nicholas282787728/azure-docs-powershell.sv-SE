---
title: Andra sätt att installera Azure PowerShell | Microsoft Docs
description: Så här installerar du Azure PowerShell med hjälp av MSI-paketet eller installationsprogrammet för webbplattformen.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: cb4ced3b72b69546594d75e7eb7db822b549a664
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821453"
---
# <a name="other-installation-methods"></a>Andra installationsmetoder

Azure PowerShell har flera olika installationsmetoder. Vi rekommenderar att du använder PowerShellGet med PowerShell-galleriet. Azure PowerShell kan installeras på Windows med installationsprogram för webbplattformen (WebPI) eller med hjälp av MSI-filen som är tillgänglig från GitHub. Azure PowerShell kan även installeras i en Docker-behållare.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Installera på Windows med hjälp av installationsprogrammet för webbplattformen

Att installera den senaste versionen av Azure PowerShell från WebPI går till på samma sätt som det gjorde för tidigare versioner.
Hämta [Azure PowerShell WebPI-paketet](http://aka.ms/webpi-azps) och starta installationen.

> [!NOTE]
> Om du tidigare har installerat Azure-moduler från PowerShell-galleriet så kommer installationsprogrammet automatiskt att ta bort dem. Detta förenklar din miljö genom att se till att endast en version av Azure PowerShell är installerad. Det finns dock scenarier där du kan behöva flera versioner installerade på samma gång.
>
> PowerShell-galleriets moduler installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules`. WebPI-installationsprogrammet däremot installerar Azure moduler i `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Om ett fel inträffar under installationen kan du ta bort Azure*-mapparna manuellt i din `$env:ProgramFiles\WindowsPowerShell\Modules`-mapp och försöka installera igen.

När installationen är färdig bör din `$env:PSModulePath`-inställning inkludera de kataloger som innehåller Azure PowerShell-cmdletarna. Följande kommando kan användas för att kontrollera att Azure PowerShell är korrekt installerad.

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

Det här felet kan korrigeras genom att starta om datorn eller importera modulen med den fullständigt kvalificerade sökvägen. Till exempel:

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Installera på Windows med hjälp av MSI-paketet

Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://aka.ms/azps-release). Om du har installerat tidigare versioner av Azure-moduler så kommer installationsprogrammet automatiskt att ta bort dem. MSI-paketet installerar moduler i `$env:ProgramFiles\WindowsPowerShell\Modules` men skapar inte versionsspecifika mappar.

## <a name="install-in-a-docker-container"></a>Installera i en Docker-behållare

Vi underhåller en Docker-avbildning som är förkonfigurerad med Azure PowerShell.

Kör behållaren med `docker run`.

```powershell
docker run azuresdk/azure-powershell
```

Dessutom underhåller vi en delmängd cmdletar som PowerShell Core-behållare.

Använd `latest`-avbildningen för Mac/Linux.

```bash
docker run azuresdk/azure-powershell-core:latest
```

Använd `nanoserver`-avbildningen för Windows.

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

Azure PowerShell är installerat på avbildningen via `Install-Module` från [PowerShell-galleriet](https://www.powershellgallery.com/).
