---
title: Översikt över Azure Stack Hub PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack Hub PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: f9bb71e19ecfe34f2c8646973f7a10526d2e8673
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427929"
---
# <a name="azure-stack-hub-module-201"></a>Azure Stack Hub-modulen 2.0.1

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack Hub som stöds är 2002.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installera

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a>Viktig information

* Stöds med 2002-uppdateringen.  

  Azure Stack Hub 2.0.0 är en icke-bakåtkompatibel ändring. Modulen använder AZ-modulen i stället för AzureRM-modulen. Du hittar en migrationsguide och en lista över de icke-bakåtkompatibla ändringarna i [Migrera från AzureRM till Azure PowerShell AZ i Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).