---
title: Köra Azure PowerShell i en Docker-behållare
description: Så här kör du Azure PowerShell i en Docker-behållare.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110338"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Köra Azure PowerShell i en Docker-behållare

Det finns en uppsättning Docker-avbildningar som är förkonfigurerade med Azure PowerShell. Två typer av behållare finns tillgängliga: de som kör traditionella PowerShell på Windows och en behållare som kör PowerShell Core på antingen Windows eller Linux.

| Miljö | Docker-avbildning |
|-------------|--------------|
| PowerShell på Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core på Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core på Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Använd `docker run -it $ImageName` för att hämta en interaktiv terminal och köra någon av dessa containrar. Om du till exempel vill köra PowerShell Core på Linux-containrar använder du:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Om du vill köra en Windows-container i Docker måste OS-värden vara Windows och Docker måste konfigureras för att köra Windows-containrar. Mer information om att växla mellan Windows- och Linux-miljöer i Docker finns i Docker-dokumentationen [Växla mellan Windows- och Linux-containrar](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).

## <a name="use-a-powershell-core-container"></a>Använda en PowerShell Core-behållare

PowerShell Core-behållarna som levereras med PowerShell Core v6 och modulen `AzureRM.NetCore` förinstallerad. Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Använda Windows-behållaren med PowerShell

Windows-behållaren har modulen `AzureRM` förinstallerad. Kör cmdleten [Import-Module](/powershell/module/microsoft.powershell.core/import-module) och logga in med ditt Azure-konto:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```