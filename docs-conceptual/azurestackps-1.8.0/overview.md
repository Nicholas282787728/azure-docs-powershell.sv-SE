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
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264418"
---
# <a name="azure-stack-module-180"></a>Azure Stack Module 1.8.0

## <a name="requirements"></a>Krav:

Den lägsta versionen av Azure Stack som stöds är 1910.

Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

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
* Exempel på några av ändringarna är:

    - **Ny DRP Admin-modul**: DRP (Deployment Resource Provider) kan användas för att orkestrera distributioner av resursprovidrar till Azure Stack Hub. Dessa kommandon interagerar med DRP via Azure Resource Manager-skiktet.

    - **BRP**:
        - Stöder återställning av enskilda roller med säkerhetskopiering av Azure-stackinfrastrukturen.
        - Lägg till parametern `RoleName` till cmdleten R`estore-AzsBackup`.

    - **FRP**: Icke-bakåtkompatibla ändringar för **enhets-** och **volymresurser** med API-version 2019-05-01. Funktionerna stöds av Azure Stack Hub 1910 och senare:
        - Värdet för ID, `Name`, `HealthStatus` och `OperationalStatus` har ändrats.
        - Stöder nya egenskaper: `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` och `StoragePool` för **enhetsresurser**.
        - Egenskaperna `CanPool` och `CannotPoolReason` för **enhetsresurser** är inaktuella. Använd `OperationalStatus` i stället.
