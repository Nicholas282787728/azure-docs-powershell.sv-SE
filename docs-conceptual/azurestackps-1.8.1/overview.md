---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: 0ee905b741c9f79b4f831bb4ea628f97566b2f1d
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427283"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="0e98a-103">Azure Stack Module 1.8.1</span><span class="sxs-lookup"><span data-stu-id="0e98a-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="0e98a-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="0e98a-104">Requirements:</span></span>

<span data-ttu-id="0e98a-105">Den lägsta versionen av Azure Stack som stöds är 1910.</span><span class="sxs-lookup"><span data-stu-id="0e98a-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="0e98a-106">Obs! Tidigare versioner av Azure Stack finns på [Installera Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="0e98a-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="0e98a-107">Installera</span><span class="sxs-lookup"><span data-stu-id="0e98a-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="0e98a-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="0e98a-108">Release Notes</span></span>

* <span data-ttu-id="0e98a-109">Stöds med 1910-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="0e98a-109">Supported with 1910 update</span></span>