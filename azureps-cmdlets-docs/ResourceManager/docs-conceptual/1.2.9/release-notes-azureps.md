---
title: "Ändringslogg för Azure PowerShell | Microsoft Docs"
description: "Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="073e3-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="073e3-103">Release notes</span></span>
<a id="release-notes" class="xliff"></a>

<span data-ttu-id="073e3-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="073e3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <span data-ttu-id="073e3-105">Version 1.2.9</span><span class="sxs-lookup"><span data-stu-id="073e3-105">Version 1.2.9</span></span>
<a id="version-129" class="xliff"></a>

<span data-ttu-id="073e3-106">Ändringar i den här versionen</span><span class="sxs-lookup"><span data-stu-id="073e3-106">Changes This Release</span></span>

* <span data-ttu-id="073e3-107">Modulen AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="073e3-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="073e3-108">Ändringar i cmdleten Add-AzureRmResourceProviderRegistration för stöd av delning av admin och klient för Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="073e3-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="073e3-109">En ny parameter, -ResourceManagerType, har lagts till.</span><span class="sxs-lookup"><span data-stu-id="073e3-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="073e3-110">Parametrarna -AdminUri, -ApiVersion, -SubscriptionId och -Token har tagits bort från varje cmdlet.</span><span class="sxs-lookup"><span data-stu-id="073e3-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="073e3-111">Vi har förvarnat om att dessa parametrar kommer att bli inaktuella och nu har de tagits bort.</span><span class="sxs-lookup"><span data-stu-id="073e3-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="073e3-112">Modulen AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="073e3-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="073e3-113">Nya cmdletar har lagts till för behållarmigreringsscenarier.</span><span class="sxs-lookup"><span data-stu-id="073e3-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="073e3-114">Cmdletar som refererar till interna komponenter och underliggande funktioner har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="073e3-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="073e3-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="073e3-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="073e3-116">En ny modul har skapats för att hantera versioner av Azure PowerShell-cmdletar med hjälp av versionsprofiler</span><span class="sxs-lookup"><span data-stu-id="073e3-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>