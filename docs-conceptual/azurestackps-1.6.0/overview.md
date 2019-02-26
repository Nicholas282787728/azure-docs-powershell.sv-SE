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
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153916"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="49c43-103">Modulen Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="49c43-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="49c43-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="49c43-104">Requirements:</span></span>
<span data-ttu-id="49c43-105">Den lägsta versionen av Azure Stack som stöds är 1811.</span><span class="sxs-lookup"><span data-stu-id="49c43-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="49c43-106">Obs! Om du använder en tidigare version måste du installera version 1.6.0</span><span class="sxs-lookup"><span data-stu-id="49c43-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="49c43-107">Installera</span><span class="sxs-lookup"><span data-stu-id="49c43-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="49c43-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="49c43-108">Release Notes</span></span>
* <span data-ttu-id="49c43-109">Stöds med 1811-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="49c43-109">Supported with 1811 update</span></span>
* <span data-ttu-id="49c43-110">Administratörsmodul för Azs.Compute</span><span class="sxs-lookup"><span data-stu-id="49c43-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="49c43-111">Korrigerade saknat Azs-prefix för New-DataDiskObject och lade till alias med varning för kommande utfasning.</span><span class="sxs-lookup"><span data-stu-id="49c43-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="49c43-112">Modulen Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="49c43-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="49c43-113">Lade till en varning som rekommenderar att du kör Test-AzureStack innan du installerar AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="49c43-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="49c43-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="49c43-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="49c43-115">Ny cmdlet (Funktionerna stöds av Azure Stack 1811+)</span><span class="sxs-lookup"><span data-stu-id="49c43-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="49c43-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="49c43-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="49c43-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="49c43-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="49c43-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="49c43-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="49c43-119">Utfasning</span><span class="sxs-lookup"><span data-stu-id="49c43-119">Deprecation</span></span>
        * <span data-ttu-id="49c43-120">Get-AzsInfrastructureVolume är nu ett alias till cmdleten Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="49c43-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="49c43-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="49c43-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="49c43-122">Lade till den nya cmdleten Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="49c43-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="49c43-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="49c43-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="49c43-124">Felkorrigering där standardkvotvärdena inte används</span><span class="sxs-lookup"><span data-stu-id="49c43-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="49c43-125">Modulen Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="49c43-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="49c43-126">Korrigerade saknade Azs-prefix för New-AddonPlanDefinitionObject och lade till alias med varning för kommande utfasning.</span><span class="sxs-lookup"><span data-stu-id="49c43-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>