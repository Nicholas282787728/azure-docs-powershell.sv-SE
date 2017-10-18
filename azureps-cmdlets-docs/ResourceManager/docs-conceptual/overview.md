---
title: "Översikt över Azure PowerShell | Microsoft Docs"
description: "En översikt över Azure PowerShell med länkar till installation och konfiguration."
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: ed681a6e920f698caab978ad57fcee9a76420afd
ms.sourcegitcommit: e6b7e20bbd04eda51416c56b13f867102b602d1a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/07/2017
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="8184f-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8184f-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="8184f-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="8184f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="8184f-105">Du kan använda det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator och använda det i PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="8184f-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="8184f-106">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera](install-azurerm-ps.md) det på egen dator.</span><span class="sxs-lookup"><span data-stu-id="8184f-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="8184f-107">Läs artikeln [Kom igång](get-started-azureps.md) för att börja använda programmet.</span><span class="sxs-lookup"><span data-stu-id="8184f-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="8184f-108">Information om den senaste versionen finns i [viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8184f-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="8184f-109">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8184f-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="8184f-110">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="8184f-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8184f-111">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="8184f-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8184f-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="8184f-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8184f-113">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="8184f-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]<span data-ttu-id="8184f-114"> > Om du har distributioner som använder den klassiska distributionsmodellen och inte kan konverteras kan du installera Service Management-versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8184f-114"> > If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="8184f-115">Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="8184f-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="8184f-116">Behöver du hjälp med PowerShell?</span><span class="sxs-lookup"><span data-stu-id="8184f-116">Need help with PowerShell?</span></span>

<span data-ttu-id="8184f-117">Om du inte känner till PowerShell, kan du ta hjälp av en introduktion till PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8184f-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="8184f-118">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="8184f-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="8184f-119">Köra skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="8184f-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="8184f-120">Du kan även titta på den här videon: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Grundläggande om PowerShell: (Del 1) Komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="8184f-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="8184f-121">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="8184f-121">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="8184f-122">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8184f-122">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="8184f-123">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="8184f-123">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="8184f-124">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8184f-124">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="8184f-125">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="8184f-125">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
