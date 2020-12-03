---
title: Översikt över Azure Stack Hub PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack Hub PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: 166c5339c95507b8a9ef1a32d46f589b8d792794
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427963"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="74526-103">Azure Stack Hub-modulen 2.0.0</span><span class="sxs-lookup"><span data-stu-id="74526-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="74526-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="74526-104">Requirements:</span></span>

<span data-ttu-id="74526-105">Den lägsta versionen av Azure Stack Hub som stöds är 2002.</span><span class="sxs-lookup"><span data-stu-id="74526-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="74526-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="74526-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="74526-107">Installera</span><span class="sxs-lookup"><span data-stu-id="74526-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="74526-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="74526-108">Release Notes</span></span>

* <span data-ttu-id="74526-109">Stöds med 2002-uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="74526-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="74526-110">Azure Stack Hub 2.0.0 är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="74526-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="74526-111">Modulen använder AZ-modulen i stället för AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="74526-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="74526-112">Du hittar en migrationsguide och en lista över de icke-bakåtkompatibla ändringarna i [Migrera från AzureRM till Azure PowerShell AZ i Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="74526-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>