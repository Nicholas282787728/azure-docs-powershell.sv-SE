---
title: Översikt över Azure PowerShell | Microsoft Docs
description: En översikt över Azure PowerShell med länkar till installation och konfiguration.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: 32decf653a956d0b0b202b38a238f42fa831ecae
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737823"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="1b5fa-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b5fa-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="1b5fa-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="1b5fa-105">Du kan använda det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator och använda det i PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="1b5fa-106">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera](install-azurerm-ps.md) det på egen dator.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="1b5fa-107">Läs artikeln [Kom igång](get-started-azureps.md) för att börja använda programmet.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="1b5fa-108">Information om den senaste versionen finns i [viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1b5fa-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="1b5fa-109">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="1b5fa-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="1b5fa-110">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="1b5fa-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1b5fa-111">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="1b5fa-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1b5fa-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="1b5fa-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1b5fa-113">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1b5fa-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="1b5fa-114">Om du har distributioner som använder sig av den klassiska distributionsmodellen och som inte kan konverteras, kan du installera Service Management-versionen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="1b5fa-115">Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="1b5fa-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="1b5fa-116">Lär dig grunderna i PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b5fa-116">Learn PowerShell basics</span></span>

<span data-ttu-id="1b5fa-117">Om du inte känner till PowerShell kan en introduktion till PowerShell vara till hjälp.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="1b5fa-118">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b5fa-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="1b5fa-119">Köra skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b5fa-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="1b5fa-120">Du kan även titta på den här videon: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Grundläggande om PowerShell: (Del 1) Komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="1b5fa-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="1b5fa-121">Eller delta i Microsoft Virtual Academy-sessionen [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) (Snabbstart för att komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="1b5fa-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="1b5fa-122">Utveckla dina färdigheter med Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="1b5fa-122">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="1b5fa-123">Automatisera Azure-uppgifter med hjälp av skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b5fa-123">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="1b5fa-124">Mer interaktiv inlärning...</span><span class="sxs-lookup"><span data-stu-id="1b5fa-124">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="1b5fa-125">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="1b5fa-125">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="1b5fa-126">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1b5fa-126">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="1b5fa-127">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="1b5fa-127">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="1b5fa-128">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1b5fa-128">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="1b5fa-129">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="1b5fa-129">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
