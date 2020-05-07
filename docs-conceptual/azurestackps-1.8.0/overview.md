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
# <a name="azure-stack-module-180"></a><span data-ttu-id="870c8-103">Azure Stack Module 1.8.0</span><span class="sxs-lookup"><span data-stu-id="870c8-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="870c8-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="870c8-104">Requirements:</span></span>

<span data-ttu-id="870c8-105">Den lägsta versionen av Azure Stack som stöds är 1910.</span><span class="sxs-lookup"><span data-stu-id="870c8-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="870c8-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="870c8-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="870c8-107">Installera</span><span class="sxs-lookup"><span data-stu-id="870c8-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="870c8-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="870c8-108">Release Notes</span></span>

* <span data-ttu-id="870c8-109">Stöds med 1910-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="870c8-109">Supported with 1910 update</span></span>
* <span data-ttu-id="870c8-110">Exempel på några av ändringarna är:</span><span class="sxs-lookup"><span data-stu-id="870c8-110">Changes include:</span></span>

    - <span data-ttu-id="870c8-111">**Ny DRP Admin-modul**: DRP (Deployment Resource Provider) kan användas för att orkestrera distributioner av resursprovidrar till Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="870c8-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="870c8-112">Dessa kommandon interagerar med DRP via Azure Resource Manager-skiktet.</span><span class="sxs-lookup"><span data-stu-id="870c8-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="870c8-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="870c8-113">**BRP**:</span></span>
        - <span data-ttu-id="870c8-114">Stöder återställning av enskilda roller med säkerhetskopiering av Azure-stackinfrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="870c8-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="870c8-115">Lägg till parametern `RoleName` till cmdleten R`estore-AzsBackup`.</span><span class="sxs-lookup"><span data-stu-id="870c8-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="870c8-116">**FRP**: Icke-bakåtkompatibla ändringar för **enhets-** och **volymresurser** med API-version 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="870c8-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="870c8-117">Funktionerna stöds av Azure Stack Hub 1910 och senare:</span><span class="sxs-lookup"><span data-stu-id="870c8-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="870c8-118">Värdet för ID, `Name`, `HealthStatus` och `OperationalStatus` har ändrats.</span><span class="sxs-lookup"><span data-stu-id="870c8-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="870c8-119">Stöder nya egenskaper: `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` och `StoragePool` för **enhetsresurser**.</span><span class="sxs-lookup"><span data-stu-id="870c8-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="870c8-120">Egenskaperna `CanPool` och `CannotPoolReason` för **enhetsresurser** är inaktuella. Använd `OperationalStatus` i stället.</span><span class="sxs-lookup"><span data-stu-id="870c8-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
