---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853023"
---
# <a name="release-notes"></a><span data-ttu-id="ef27e-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="ef27e-103">Release notes</span></span>

<span data-ttu-id="ef27e-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="ef27e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="ef27e-105">Version 1.2.9</span><span class="sxs-lookup"><span data-stu-id="ef27e-105">Version 1.2.9</span></span>

<span data-ttu-id="ef27e-106">Ändringar i den här versionen</span><span class="sxs-lookup"><span data-stu-id="ef27e-106">Changes This Release</span></span>

* <span data-ttu-id="ef27e-107">Modulen AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="ef27e-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="ef27e-108">Ändringar i cmdleten Add-AzureRmResourceProviderRegistration för stöd av delning av admin och klient för Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ef27e-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="ef27e-109">En ny parameter, -ResourceManagerType, har lagts till.</span><span class="sxs-lookup"><span data-stu-id="ef27e-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="ef27e-110">Parametrarna -AdminUri, -ApiVersion, -SubscriptionId och -Token har tagits bort från varje cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef27e-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="ef27e-111">Vi har förvarnat om att dessa parametrar kommer att bli inaktuella och nu har de tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ef27e-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="ef27e-112">Modulen AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="ef27e-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="ef27e-113">Nya cmdletar har lagts till för behållarmigreringsscenarier.</span><span class="sxs-lookup"><span data-stu-id="ef27e-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="ef27e-114">Cmdletar som refererar till interna komponenter och underliggande funktioner har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ef27e-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="ef27e-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="ef27e-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="ef27e-116">En ny modul har skapats för att hantera versioner av Azure PowerShell-cmdletar med hjälp av versionsprofiler</span><span class="sxs-lookup"><span data-stu-id="ef27e-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>