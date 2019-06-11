---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855796"
---
# <a name="azure-stack-module-172"></a>Azure Stack Module 1.7.2

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack som stöds är 1904.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>Installera PowerShell för Azure Stack

Installationen består av tre steg:

1. Installera PowerShell för Azure Stack beroende på din version av Azure Stack
2. Aktivera ytterligare lagringsfunktioner
3. Bekräfta installationen av PowerShell

### <a name="install-azure-stack-powershell"></a>Installera Azure Stack PowerShell

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a>Aktivera ytterligare lagringsfunktioner

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a>Viktig information

* Stöds med 1904-uppdateringen
* Det här är en icke-bakåtkompatibel ändring. Mer information om de senaste ändringarna finns i <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin-modulen * icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge. Stöd för symmetriska nycklar fasas ut.
* Azs.Fabric.Admin-modulen       * Utfasning           * Get-AzsInfrastructureVolume är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsVolume           * Get-AzsStorageSystem är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsStorageSubSystem           * Get-AzsStoragePool är inaktuell, kapacitetsegenskapen finns i StorageSubSystem-objektet
* Azs.Fabric.Admin-modulen           * Felkorrigering: Add-AzsPlatformImage, Get-AzsPlatformImage: Anropa endast ConvertTo-PlatformImageObject i rätt sökväg * Felkorrigering: Add-AzsVmExtension, Get-AzsVmExtension: Anropa endast ConvertTo-VmExtensionObject i rätt sökväg
* Azs.Storage.Admin-modulen           * Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.
