---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240143"
---
# <a name="azure-stack-module-160"></a>Modulen Azure Stack 1.6.0

## <a name="requirements"></a>Krav:
Den lägsta versionen av Azure Stack som stöds är 1811.

Obs! Om du använder en tidigare version måste du installera version 1.6.0

## <a name="install"></a>Installera
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Viktig information
* Stöds med 1811-uppdateringen
* Administratörsmodul för Azs.Compute
    * Korrigerade saknat Azs-prefix för New-DataDiskObject och lade till alias med varning för kommande utfasning.
* Modulen Azs.Update.Admin
    * Lade till en varning som rekommenderar att du kör Test-AzureStack innan du installerar AzsUpdate
* Azs.Fabric.Admin
    * Ny cmdlet (Funktionerna stöds av Azure Stack 1811+)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Utfasning
        * Get-AzsInfrastructureVolume är nu ett alias till cmdleten Get-AzsVolume
* Azs.InfrastructureInsights.Admin
    *  Lade till den nya cmdleten Repair-AzsAlert
* Azs.Storage.Admin
    * Felkorrigering där standardkvotvärdena inte används
* Modulen Azs.Subscriptions.Admin
    * Korrigerade saknade Azs-prefix för New-AddonPlanDefinitionObject och lade till alias med varning för kommande utfasning.
