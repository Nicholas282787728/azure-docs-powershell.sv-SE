---
title: Översikt över Azure PowerShell
description: En översikt över Azure PowerShell Az-modulen med information om hur du installerar och kommer igång.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 58fb9c222eb1fcbace189917138d9a75564bfb29
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464969"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="6e53b-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e53b-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="6e53b-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="6e53b-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="6e53b-105">Azure PowerShell använder .NET Standard, vilket gör det tillgängligt för Windows, macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="6e53b-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="6e53b-106">Azure PowerShell är också tillgängligt i Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="6e53b-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="6e53b-107">Om den nya Az-modulen</span><span class="sxs-lookup"><span data-stu-id="6e53b-107">About the new Az module</span></span>

<span data-ttu-id="6e53b-108">I den här dokumentationen beskrivs den nya Az-modulen för Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e53b-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="6e53b-109">Den nya modulen skrivs från grunden i .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="6e53b-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="6e53b-110">När .NET Standard används kan Azure PowerShell köras under PowerShell 5.x i Windows eller PowerShell 6 på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="6e53b-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="6e53b-111">Az-modulen är nu rätt sätt att interagera med Azure via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e53b-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="6e53b-112">Vi fortsätter göra felkorrigeringar i AzureRM men inga nya funktioner läggs till.</span><span class="sxs-lookup"><span data-stu-id="6e53b-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="6e53b-113">Fullständig information om den nya modulen, som nya kommandonamn och underhållsplaner för AzureRM, finns i [Introduktion till Azure PowerShell Az-modulen](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="6e53b-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="6e53b-114">Om du vill komma igång med den nya modulen direkt läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6e53b-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="6e53b-115">[AzureRM-dokumentationen](/powershell/azure/azurerm) finns också tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="6e53b-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6e53b-116">Medan Azure-dokumentationen uppdateras för att återspegla de nya modul-cmdlet-namnen kan det hända att AzureRM-kommandona fortfarande används i artiklarna.</span><span class="sxs-lookup"><span data-stu-id="6e53b-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="6e53b-117">När du har installerat Az-modulen rekommenderar vi att du aktiverar AzureRM-cmdlet-aliasen med `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="6e53b-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="6e53b-118">Mer information finns i artikeln [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6e53b-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="6e53b-119">Köra eller installera</span><span class="sxs-lookup"><span data-stu-id="6e53b-119">Run or install</span></span>

<span data-ttu-id="6e53b-120">Du kan installera Azure PowerShell på alla plattformar som har stöd för PowerShell 5.x eller PowerShell 6.x eller körs i Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="6e53b-120">You can install Azure PowerShell on any platform which supports PowerShell 5.x or PowerShell 6.x, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="6e53b-121">Om du vill köra det i webbläsaren med Azure Cloud Shell läser du [Snabbstart för PowerShell i Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="6e53b-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="6e53b-122">Om du vill installera Azure PowerShell på datorn läser du [Installera Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6e53b-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="6e53b-123">Information om den senaste versionen av Azure PowerShell finns i [Viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6e53b-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="6e53b-124">Kom igång</span><span class="sxs-lookup"><span data-stu-id="6e53b-124">Get Started</span></span>

<span data-ttu-id="6e53b-125">Läs artikeln [Komma igång med Azure PowerShell](get-started-azureps.md) om du vill lära dig grunderna i Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6e53b-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="6e53b-126">Om du inte känner till PowerShell kan en introduktion vara till hjälp:</span><span class="sxs-lookup"><span data-stu-id="6e53b-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="6e53b-127">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e53b-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="6e53b-128">Köra skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e53b-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="6e53b-129">PowerShell-grunder: (Del 1) Komma igång med PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e53b-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* <span data-ttu-id="6e53b-130">Microsoft Virtual Academys [Komma igång med PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span><span class="sxs-lookup"><span data-stu-id="6e53b-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="6e53b-131">Följande exempel kan hjälpa dig med några vanliga användningsområden för Azure:</span><span class="sxs-lookup"><span data-stu-id="6e53b-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="6e53b-132">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="6e53b-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="6e53b-133">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="6e53b-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="6e53b-134">Web Apps</span><span class="sxs-lookup"><span data-stu-id="6e53b-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="6e53b-135">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6e53b-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="6e53b-136">Utveckla dina färdigheter med Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="6e53b-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="6e53b-137">Automatisera Azure-uppgifter med hjälp av skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e53b-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="6e53b-138">Mer interaktiv inlärning...</span><span class="sxs-lookup"><span data-stu-id="6e53b-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="6e53b-139">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="6e53b-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="6e53b-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6e53b-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="6e53b-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6e53b-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="6e53b-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="6e53b-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
