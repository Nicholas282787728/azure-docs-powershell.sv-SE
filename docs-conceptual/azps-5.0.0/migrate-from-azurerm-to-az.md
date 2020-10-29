---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753876"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrera Azure PowerShell från AzureRM till Az

Alla versioner av AzureRM PowerShell-modulen är inaktuella, men stöds fortfarande. [Az PowerShell-modulen](install-az-ps.md) är nu den rekommenderade PowerShell-modulen för att interagera med Azure.

Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen. För att underlätta övergången utvecklades [verktyg för migrering från AzureRM till AZ](https://github.com/Azure/azure-powershell-migration). Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till Az PowerShell-modulen. Mer information om varför Az PowerShell-modulen skapades finns i [Introduktion till den nya Azure PowerShell Az-modulen](new-azureps-module-az.md).

En fullständig lista över icke-bakåtkompatibla ändringar mellan AzureRM och Az finns i de [fullständiga ändringarna från AzureRM till Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Se till att befintliga skript fungerar med den senaste versionen av AzureRM

Innan du påbörjar migreringen bör du kontrollera vilka versioner av AzureRM som finns installerade på datorn.
Du kan då se till att skripten redan körs med den senaste versionen, och du ser vilka versioner av AzureRM som behöver avinstalleras.

Om du vill kontrollera vilka versioner av AzureRM du har installerade kör du följande exempel:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Den **senaste** tillgängliga versionen av AzureRM är **6.13.1** . Om du inte har den här versionen kan de befintliga skripten behöva ytterligare modifieringar för att de ska fungera med Az-modulen, förutom det som beskrivs i den här artikeln och i [listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md).

Om skripten inte fungerar med AzureRM 6.13.1 uppdaterar du dem enligt [migreringsguiden för AzureRM 5.x till 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Om du använder en tidigare version av AzureRM-modulen finns det migreringsguider för varje större version.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installera verktygen för migrering från AzureRM till Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Migrera PowerShell-skript automatiskt

Med verktygen för migrering från AzureRM till Az kan du skapa en plan för att bestämma vilka ändringar som ska utföras för dina skript innan du ändrar dem och innan du installerar Az PowerShell-modulen.

Snabbstarten [Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen](quickstart-migrate-azurerm-to-az-automatically.md) vägleder dig genom hela processen med att uppdatera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.

## <a name="next-steps"></a>Nästa steg

[Installera Azure PowerShell](install-az-ps.md)
[Avinstallera AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
