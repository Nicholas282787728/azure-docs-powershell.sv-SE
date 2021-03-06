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
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427385"
---
# <a name="azure-stack-module-172"></a>Azure Stack Module 1.7.2

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack som stöds är 1904.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installera

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Viktig information

* Stöds med 1904-uppdateringen
* Det här är en icke-bakåtkompatibel ändring. Mer information om de senaste ändringarna finns i <https://aka.ms/azspshmigration170>
* Icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge. Stöd för symmetriska nycklar fasas ut.
* Mer information om de senaste ändringarna finns i https://aka.ms/azspshmigration170
* Azs.Storage.Admin-modul 
* Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.