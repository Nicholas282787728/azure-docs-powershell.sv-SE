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
ms.openlocfilehash: fd1f2a3778e348ba41b46acb4bdce19e18a7f4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "81524973"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="b95f1-103">Azure Stack Hub-modulen 2.0.0</span><span class="sxs-lookup"><span data-stu-id="b95f1-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b95f1-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="b95f1-104">Requirements:</span></span>

<span data-ttu-id="b95f1-105">Den lägsta versionen av Azure Stack Hub som stöds är 2002.</span><span class="sxs-lookup"><span data-stu-id="b95f1-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="b95f1-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="b95f1-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="b95f1-107">Installera</span><span class="sxs-lookup"><span data-stu-id="b95f1-107">Install</span></span>

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


## <a name="release-notes"></a><span data-ttu-id="b95f1-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="b95f1-108">Release Notes</span></span>

* <span data-ttu-id="b95f1-109">Stöds med 2002-uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b95f1-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="b95f1-110">Azure Stack Hub 2.0.0 är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="b95f1-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="b95f1-111">Modulen använder AZ-modulen i stället för AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="b95f1-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="b95f1-112">Du hittar en migrationsguide och en lista över de icke-bakåtkompatibla ändringarna i [Migrera från AzureRM till Azure PowerShell AZ i Azure Stack Hub](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="b95f1-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
