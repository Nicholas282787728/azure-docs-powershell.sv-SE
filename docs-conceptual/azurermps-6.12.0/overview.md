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
ms.openlocfilehash: bdd8e69a2ea9df8b4fff100e1f3cc4c82d2d9d9d
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575305"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="97c08-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c08-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="97c08-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="97c08-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="97c08-105">Du kan använda det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator och använda det i PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="97c08-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="97c08-106">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera](install-azurerm-ps.md) det på egen dator.</span><span class="sxs-lookup"><span data-stu-id="97c08-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="97c08-107">Läs artikeln [Kom igång](get-started-azureps.md) för att börja använda programmet.</span><span class="sxs-lookup"><span data-stu-id="97c08-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="97c08-108">Information om den senaste versionen finns i [viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="97c08-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="97c08-109">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="97c08-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="97c08-110">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="97c08-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97c08-111">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="97c08-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97c08-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="97c08-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97c08-113">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="97c08-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="learn-powershell-basics"></a><span data-ttu-id="97c08-114">Lär dig grunderna i PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c08-114">Learn PowerShell basics</span></span>

<span data-ttu-id="97c08-115">Om du inte känner till PowerShell kan en introduktion till PowerShell vara till hjälp.</span><span class="sxs-lookup"><span data-stu-id="97c08-115">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="97c08-116">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c08-116">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="97c08-117">Köra skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c08-117">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="97c08-118">Du kan även titta på den här videon: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Grundläggande om PowerShell: (Del 1) Komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="97c08-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="97c08-119">Eller delta i Microsoft Virtual Academy-sessionen [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) (Snabbstart för att komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="97c08-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="97c08-120">Utveckla dina färdigheter med Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="97c08-120">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="97c08-121">Automatisera Azure-uppgifter med hjälp av skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c08-121">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="97c08-122">Mer interaktiv inlärning...</span><span class="sxs-lookup"><span data-stu-id="97c08-122">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="97c08-123">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="97c08-123">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="97c08-124">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="97c08-124">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="97c08-125">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="97c08-125">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="97c08-126">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="97c08-126">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="97c08-127">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="97c08-127">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
