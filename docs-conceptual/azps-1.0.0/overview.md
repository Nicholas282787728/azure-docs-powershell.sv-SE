---
title: Översikt över Azure PowerShell
description: En översikt över Azure PowerShell Az-modulen med information om hur du installerar och kommer igång.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736468"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="28952-103">Översikt över Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="28952-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="28952-104">Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="28952-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="28952-105">Azure PowerShell använder .NET Standard, vilket gör det tillgängligt för Windows, macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="28952-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="28952-106">Azure PowerShell är också tillgängligt från Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="28952-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="28952-107">Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera det lokalt](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="28952-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="28952-108">Läs artikeln [Komma igång](get-started-azureps.md) om du vill lära dig grunderna i Azure PowerShell och komma igång med Azure.</span><span class="sxs-lookup"><span data-stu-id="28952-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="28952-109">Information om den senaste versionen av Azure PowerShell finns i [Viktig information](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="28952-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="28952-110">Om den nya Az-modulen</span><span class="sxs-lookup"><span data-stu-id="28952-110">About the new Az module</span></span>

<span data-ttu-id="28952-111">I den här dokumentationen beskrivs den nya Az-modulen för Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28952-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="28952-112">Den nya modulen skrivs från grunden i .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="28952-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="28952-113">När .NET Standard används kan Azure PowerShell köras under PowerShell 5.x i Windows eller PowerShell 6 på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="28952-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="28952-114">Az-modulen är nu rätt sätt att interagera med Azure via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28952-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="28952-115">Vi fortsätter göra felkorrigeringar i AzureRM men inga nya funktioner läggs till.</span><span class="sxs-lookup"><span data-stu-id="28952-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="28952-116">Fullständig information om den nya modulen, som nya kommandonamn och underhållsplaner för AzureRM, finns i [Introduktion till Azure PowerShell Az-modulen](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="28952-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="28952-117">Om du vill komma igång med den nya modulen direkt läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="28952-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="28952-118">[AzureRM-dokumentationen](/powershell/azure/azurerm) finns också tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="28952-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="28952-119">Medan Azure-dokumentationen uppdateras för att återspegla de nya modul-cmdlet-namnen kan det hända att AzureRM-kommandona fortfarande används i artiklarna.</span><span class="sxs-lookup"><span data-stu-id="28952-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="28952-120">När du har installerat Az-modulen rekommenderar vi att du aktiverar AzureRM-cmdlet-aliasen med `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="28952-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="28952-121">Mer information finns i artikeln [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="28952-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="28952-122">Vanliga scenarier</span><span class="sxs-lookup"><span data-stu-id="28952-122">Common scenarios</span></span>

<span data-ttu-id="28952-123">Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="28952-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="28952-124">Virtuella Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="28952-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="28952-125">Virtuella Windows-datorer</span><span class="sxs-lookup"><span data-stu-id="28952-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="28952-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="28952-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="28952-127">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="28952-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="28952-128">Lär dig grunderna i PowerShell</span><span class="sxs-lookup"><span data-stu-id="28952-128">Learn PowerShell basics</span></span>

<span data-ttu-id="28952-129">Om du inte känner till PowerShell kan en introduktion vara till hjälp.</span><span class="sxs-lookup"><span data-stu-id="28952-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="28952-130">Installera PowerShell</span><span class="sxs-lookup"><span data-stu-id="28952-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="28952-131">Köra skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="28952-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="28952-132">Du kan även se den här videon: [PowerShell-grunder: (Del 1) Komma igång med PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="28952-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="28952-133">Eller delta i Microsoft Virtual Academy-sessionen [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) (Snabbstart för att komma igång med PowerShell).</span><span class="sxs-lookup"><span data-stu-id="28952-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="28952-134">Utveckla dina färdigheter med Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="28952-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="28952-135">Automatisera Azure-uppgifter med hjälp av skript med PowerShell</span><span class="sxs-lookup"><span data-stu-id="28952-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="28952-136">Mer interaktiv inlärning...</span><span class="sxs-lookup"><span data-stu-id="28952-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="28952-137">Andra Azure PowerShell-moduler</span><span class="sxs-lookup"><span data-stu-id="28952-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="28952-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="28952-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="28952-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="28952-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="28952-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="28952-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="28952-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="28952-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
