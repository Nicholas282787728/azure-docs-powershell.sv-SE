---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: e314374eff433d1869378bdaa9a0370c3fd3d8d1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022958"
---
# <a name="azure-stack-module-182"></a><span data-ttu-id="b01ca-103">Azure Stack-modul 1.8.2</span><span class="sxs-lookup"><span data-stu-id="b01ca-103">Azure Stack Module 1.8.2</span></span>

## <a name="requirements"></a><span data-ttu-id="b01ca-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="b01ca-104">Requirements:</span></span>

<span data-ttu-id="b01ca-105">Den lägsta versionen av Azure Stack som stöds är 1910.</span><span class="sxs-lookup"><span data-stu-id="b01ca-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="b01ca-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="b01ca-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="b01ca-107">Installera</span><span class="sxs-lookup"><span data-stu-id="b01ca-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a><span data-ttu-id="b01ca-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="b01ca-108">Release Notes</span></span>

* <span data-ttu-id="b01ca-109">Stöds med 1910-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="b01ca-109">Supported with 1910 update</span></span>
