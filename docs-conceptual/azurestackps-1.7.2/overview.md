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
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861350"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="d4907-103">Azure Stack Module 1.7.2</span><span class="sxs-lookup"><span data-stu-id="d4907-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="d4907-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="d4907-104">Requirements:</span></span>

<span data-ttu-id="d4907-105">Den lägsta versionen av Azure Stack som stöds är 1904.</span><span class="sxs-lookup"><span data-stu-id="d4907-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="d4907-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="d4907-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="d4907-107">Installera</span><span class="sxs-lookup"><span data-stu-id="d4907-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="d4907-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="d4907-108">Release Notes</span></span>

* <span data-ttu-id="d4907-109">Stöds med 1904-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="d4907-109">Supported with 1904 update</span></span>
* <span data-ttu-id="d4907-110">Det här är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="d4907-110">This a breaking change release.</span></span> <span data-ttu-id="d4907-111">Mer information om de senaste ändringarna finns i <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="d4907-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="d4907-112">Icke-bakåtkompatibel ändring: Backup ändras till certifikatsbaserat krypteringsläge.</span><span class="sxs-lookup"><span data-stu-id="d4907-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="d4907-113">Stöd för symmetriska nycklar fasas ut.</span><span class="sxs-lookup"><span data-stu-id="d4907-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="d4907-114">Mer information om de senaste ändringarna finns i https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="d4907-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="d4907-115">Azs.Storage.Admin-modul</span><span class="sxs-lookup"><span data-stu-id="d4907-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="d4907-116">Felkorrigering – Ny lagringskvot använder standardvärden om inget annat anges.</span><span class="sxs-lookup"><span data-stu-id="d4907-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
