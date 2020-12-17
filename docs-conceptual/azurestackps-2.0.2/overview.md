---
title: Översikt över Azure Stack Hub PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack Hub PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: ec4591e4f44fa56b7482d2dec3f525cb02dbd94b
ms.sourcegitcommit: a24069b411d3a6011067770430b6dcdd4b2c2159
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/16/2020
ms.locfileid: "97532267"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="4946f-103">Azure Stack Hub-modul 2.0.2</span><span class="sxs-lookup"><span data-stu-id="4946f-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="4946f-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="4946f-104">Requirements:</span></span>

<span data-ttu-id="4946f-105">Den lägsta versionen av Azure Stack Hub som stöds är 2002.</span><span class="sxs-lookup"><span data-stu-id="4946f-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="4946f-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="4946f-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="4946f-107">Installera</span><span class="sxs-lookup"><span data-stu-id="4946f-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease -SkipPublisherCheck

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="4946f-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="4946f-108">Release Notes</span></span>

* <span data-ttu-id="4946f-109">Stöds med 2002-uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="4946f-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="4946f-110">Azure Stack Hub 2.0.0 är en icke-bakåtkompatibel ändring.</span><span class="sxs-lookup"><span data-stu-id="4946f-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="4946f-111">Modulen använder AZ-modulen i stället för AzureRM-modulen.</span><span class="sxs-lookup"><span data-stu-id="4946f-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="4946f-112">Du hittar en migrationsguide och en lista över de icke-bakåtkompatibla ändringarna i [Migrera från AzureRM till Azure PowerShell AZ i Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="4946f-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>
