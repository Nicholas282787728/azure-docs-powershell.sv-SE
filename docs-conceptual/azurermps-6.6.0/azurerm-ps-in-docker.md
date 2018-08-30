---
title: Köra Azure PowerShell i en Docker-behållare
description: Så här kör du Azure PowerShell i en Docker-behållare.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018997"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Köra Azure PowerShell i en Docker-behållare

Microsoft publicerar Docker-avbildningar med Azure PowerShell förinstallerat för att göra det enkelt att köra Azure PowerShell i bärbara miljöer. Avbildningarna erbjuder en Linux-gäst som kör PowerShell Core eller en Windows-gäst med antingen PowerShell Core eller PowerShell 5.

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
