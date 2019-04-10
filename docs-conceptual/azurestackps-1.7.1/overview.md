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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808076"
---
# <a name="azure-stack-module-171"></a>Azure Stack-modulen 1.7.1

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack som stöds är 1901.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installera

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Viktig information

* Stöds med 1901-uppdateringen
* Det här är en icke-bakåtkompatibel ändring. Mer information om de senaste ändringarna finns i <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin-modulen * icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge. Stöd för symmetriska nycklar fasas ut.
* Azs.Fabric.Admin-modulen       * Utfasning           * Get-AzsInfrastructureVolume är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsVolume           * Get-AzsStorageSystem är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsStorageSubSystem           * Get-AzsStoragePool är inaktuell, kapacitetsegenskapen finns i StorageSubSystem-objektet
* Azs.Fabric.Admin-modulen           * Felkorrigering: Add-AzsPlatformImage, Get-AzsPlatformImage: Anropa endast ConvertTo-PlatformImageObject i rätt sökväg * Felkorrigering: Add-AzsVmExtension, Get-AzsVmExtension: Anropa endast ConvertTo-VmExtensionObject i rätt sökväg
* Azs.Storage.Admin-modulen           * Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.
