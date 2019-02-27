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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240539"
---
# <a name="azure-stack-module-170"></a><span data-ttu-id="3142d-103">Modulen Azure Stack 1.7.0</span><span class="sxs-lookup"><span data-stu-id="3142d-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="3142d-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="3142d-104">Requirements:</span></span>
<span data-ttu-id="3142d-105">Den lägsta versionen av Azure Stack som stöds är 1901.</span><span class="sxs-lookup"><span data-stu-id="3142d-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="3142d-106">Obs! Om du använder en tidigare version måste du installera version 1.7.0</span><span class="sxs-lookup"><span data-stu-id="3142d-106">Note: If you are using an earlier version install version 1.7.0</span></span>

## <a name="install"></a><span data-ttu-id="3142d-107">Installera</span><span class="sxs-lookup"><span data-stu-id="3142d-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a><span data-ttu-id="3142d-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="3142d-108">Release Notes</span></span>
* <span data-ttu-id="3142d-109">Stöds med 1901-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="3142d-109">Supported with 1901 update</span></span>
* <span data-ttu-id="3142d-110">Det här är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="3142d-110">This a breaking change release.</span></span> <span data-ttu-id="3142d-111">Mer information om de senaste ändringarna finns i https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="3142d-111">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="3142d-112">Azs.Backup.Admin-modulen \* icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge.</span><span class="sxs-lookup"><span data-stu-id="3142d-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="3142d-113">Stöd för symmetriska nycklar fasas ut.</span><span class="sxs-lookup"><span data-stu-id="3142d-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="3142d-114">Azs.Fabric.Admin-modulen       \* Utfasning           \* Get-AzsInfrastructureVolume är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsVolume           \* Get-AzsStorageSystem är inaktuell, vi tillhandahåller den nya cmdleten Get-AzsStorageSubSystem           \* Get-AzsStoragePool är inaktuell, kapacitetsegenskapen finns i StorageSubSystem-objektet</span><span class="sxs-lookup"><span data-stu-id="3142d-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="3142d-115">Azs.Fabric.Admin-modulen           \* Felkorrigering: Add-AzsPlatformImage, Get-AzsPlatformImage: Anropa endast ConvertTo-PlatformImageObject i rätt sökväg \* Felkorrigering: Add-AzsVmExtension, Get-AzsVmExtension: Anropa endast ConvertTo-VmExtensionObject i rätt sökväg</span><span class="sxs-lookup"><span data-stu-id="3142d-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="3142d-116">Azs.Storage.Admin-modulen           \* Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.</span><span class="sxs-lookup"><span data-stu-id="3142d-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>

