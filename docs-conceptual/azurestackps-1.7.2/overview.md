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
# <a name="azure-stack-module-172"></a><span data-ttu-id="45019-103">Azure Stack Module 1.7.2</span><span class="sxs-lookup"><span data-stu-id="45019-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="45019-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="45019-104">Requirements:</span></span>

<span data-ttu-id="45019-105">Den lägsta versionen av Azure Stack som stöds är 1904.</span><span class="sxs-lookup"><span data-stu-id="45019-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="45019-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="45019-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="45019-107">Installera PowerShell för Azure Stack</span><span class="sxs-lookup"><span data-stu-id="45019-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="45019-108">Installationen består av tre steg:</span><span class="sxs-lookup"><span data-stu-id="45019-108">Installation has three steps:</span></span>

1. <span data-ttu-id="45019-109">Installera PowerShell för Azure Stack beroende på din version av Azure Stack</span><span class="sxs-lookup"><span data-stu-id="45019-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="45019-110">Aktivera ytterligare lagringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="45019-110">Enable additional storage features</span></span>
3. <span data-ttu-id="45019-111">Bekräfta installationen av PowerShell</span><span class="sxs-lookup"><span data-stu-id="45019-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="45019-112">Installera Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="45019-112">Install Azure Stack PowerShell</span></span>

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

### <a name="enable-additional-storage-features"></a><span data-ttu-id="45019-113">Aktivera ytterligare lagringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="45019-113">Enable additional storage features</span></span>

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

## <a name="release-notes"></a><span data-ttu-id="45019-114">Viktig information</span><span class="sxs-lookup"><span data-stu-id="45019-114">Release Notes</span></span>

* <span data-ttu-id="45019-115">Stöds med 1904-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="45019-115">Supported with 1904 update</span></span>
* <span data-ttu-id="45019-116">Det här är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="45019-116">This a breaking change release.</span></span> <span data-ttu-id="45019-117">Mer information om de senaste ändringarna finns i <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="45019-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="45019-118">Azs.Backup.Admin-modulen \* icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge.</span><span class="sxs-lookup"><span data-stu-id="45019-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="45019-119">Stöd för symmetriska nycklar fasas ut.</span><span class="sxs-lookup"><span data-stu-id="45019-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="45019-120">Azs.Fabric.Admin-modulen       \* Utfasning           \* Get-AzsInfrastructureVolume är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsVolume           \* Get-AzsStorageSystem är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsStorageSubSystem           \* Get-AzsStoragePool är inaktuell, kapacitetsegenskapen finns i StorageSubSystem-objektet</span><span class="sxs-lookup"><span data-stu-id="45019-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="45019-121">Azs.Fabric.Admin-modulen           \* Felkorrigering: Add-AzsPlatformImage, Get-AzsPlatformImage: Anropa endast ConvertTo-PlatformImageObject i rätt sökväg \* Felkorrigering: Add-AzsVmExtension, Get-AzsVmExtension: Anropa endast ConvertTo-VmExtensionObject i rätt sökväg</span><span class="sxs-lookup"><span data-stu-id="45019-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="45019-122">Azs.Storage.Admin-modulen           \* Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.</span><span class="sxs-lookup"><span data-stu-id="45019-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
