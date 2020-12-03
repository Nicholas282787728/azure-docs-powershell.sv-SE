---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: e19fea440025e7a00a037e360ac95ff8e0e62129
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428018"
---
# <a name="azure-stack-module-180"></a>Azure Stack Module 1.8.0

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack som stöds är 1910.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installera

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Viktig information

* Stöds med 1910-uppdateringen
* Ändringarna omfattar:

    - **Ny DRP Admin-modul**: DRP (Deployment Resource Provider) kan användas för att orkestrera distributioner av resursprovidrar till Azure Stack Hub. Dessa kommandon interagerar med DRP via Azure Resource Manager-skiktet.

    - **BRP**:
        - Stöder återställning av enskilda roller med säkerhetskopiering av Azure-stackinfrastrukturen.
        - Lägg till parametern `RoleName` till cmdleten R`estore-AzsBackup`.

    - **FRP**: Icke-bakåtkompatibla ändringar för **enhets-** och **volymresurser** med API-version 2019-05-01. Funktionerna stöds av Azure Stack Hub 1910 och senare:
        - Värdet för ID, `Name`, `HealthStatus` och `OperationalStatus` har ändrats.
        - Stöder nya egenskaper: `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` och `StoragePool` för **enhetsresurser**.
        - Egenskaperna `CanPool` och `CannotPoolReason` för **enhetsresurser** är inaktuella. Använd `OperationalStatus` i stället.