---
title: Översikt över Azure PowerShell | Microsoft Docs
description: En översikt över Azure PowerShell med länkar till installation och konfiguration.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5bd3e788f84bad171e13f43fb9c97d922a1e5222
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523424"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="e4e6f-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4e6f-103">Overview of Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="e4e6f-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="e4e6f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="e4e6f-105">Du kan använda det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator och använda det i PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="e4e6f-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="e4e6f-106">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera](install-azurerm-ps.md) det på egen dator.</span><span class="sxs-lookup"><span data-stu-id="e4e6f-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="e4e6f-107">Läs artikeln [Kom igång](get-started-azureps.md) för att börja använda programmet.</span><span class="sxs-lookup"><span data-stu-id="e4e6f-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="e4e6f-108">Information om den senaste versionen finns i [viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e4e6f-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="e4e6f-109">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e4e6f-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

- [<span data-ttu-id="e4e6f-110">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="e4e6f-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/linux/powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="e4e6f-111">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="e4e6f-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/windows/powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="e4e6f-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="e4e6f-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="e4e6f-113">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e4e6f-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="e4e6f-114">Lär dig grunderna i PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4e6f-114">Learn PowerShell basics</span></span>

<span data-ttu-id="e4e6f-115">Om du inte känner till PowerShell, kan du ta hjälp av en introduktion till PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4e6f-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

- [<span data-ttu-id="e4e6f-116">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4e6f-116">Installing PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
- [<span data-ttu-id="e4e6f-117">Utbildningsresurser för PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4e6f-117">PowerShell learning resources</span></span>](/powershell/scripting/learn/more-powershell-learning)

<span data-ttu-id="e4e6f-118">Du kan även se den här videon: [PowerShell-grunder: (Del 1) Komma igång med PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="e4e6f-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="e4e6f-119">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="e4e6f-119">Other Azure PowerShell modules</span></span>

- [<span data-ttu-id="e4e6f-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e4e6f-120">Azure Active Directory</span></span>](/powershell/module/activedirectory/)
- [<span data-ttu-id="e4e6f-121">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e4e6f-121">Azure Service Fabric</span></span>](/powershell/module/AzureRM.ServiceFabric/)
