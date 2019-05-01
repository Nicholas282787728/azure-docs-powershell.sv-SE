---
title: Introduktion till Azure PowerShell Az-modulen
description: Vi introducerar den nya Azure PowerShell-modulen Az, som ersätter AzureRM-modulen.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068837"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="df2dc-103">Introduktion till den nya Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="df2dc-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="df2dc-104">Från och med december 2018 är Az för Azure PowerShell-modulen en allmän version och är nu den PowerShell-modulen som är avsedd för interaktion med Azure.</span><span class="sxs-lookup"><span data-stu-id="df2dc-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="df2dc-105">Az erbjuder kortare kommandon, bättre stabilitet och stöd för flera plattformar.</span><span class="sxs-lookup"><span data-stu-id="df2dc-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="df2dc-106">Az erbjuder också funktionsparitet och en enkel migreringsväg från AzureRM.</span><span class="sxs-lookup"><span data-stu-id="df2dc-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="df2dc-107">Az använder .NET Standard-biblioteket, vilket innebär att den körs på PowerShell 5 och PowerShell 6.</span><span class="sxs-lookup"><span data-stu-id="df2dc-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="df2dc-108">Eftersom PowerShell 6 kan köras på Linux, macOS och Windows är Azure PowerShell nu tillgängligt för alla plattformar.</span><span class="sxs-lookup"><span data-stu-id="df2dc-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="df2dc-109">Med .NET Standard kan vi förena kodbasen för Azure PowerShell med minimal inverkan på användare.</span><span class="sxs-lookup"><span data-stu-id="df2dc-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="df2dc-110">Az är en ny modul, så versionen har återställts till 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="df2dc-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="df2dc-111">Uppgradera till Az</span><span class="sxs-lookup"><span data-stu-id="df2dc-111">Upgrade to Az</span></span>

<span data-ttu-id="df2dc-112">Vi rekommenderar att alla användare uppgraderar till den nya Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="df2dc-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="df2dc-113">Gör så här:</span><span class="sxs-lookup"><span data-stu-id="df2dc-113">To do so:</span></span>

* <span data-ttu-id="df2dc-114">__REKOMMENDERAS__: [Avinstallera Azure PowerShell AzureRM-modulen](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="df2dc-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="df2dc-115">Installera Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="df2dc-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="df2dc-116">Aktivera kompatibilitetsläge för att lägga till alias för AzureRM-cmdletar med `Enable-AzureRMAlias` medan du bekantar dig med den nya kommandouppsättningen.</span><span class="sxs-lookup"><span data-stu-id="df2dc-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="df2dc-117">Aktivera alias __endast__ om du inte har AzureRM installerat.</span><span class="sxs-lookup"><span data-stu-id="df2dc-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="df2dc-118">Migrera befintliga skript till Az</span><span class="sxs-lookup"><span data-stu-id="df2dc-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="df2dc-119">Stora uppdateringar kan vara olägliga.</span><span class="sxs-lookup"><span data-stu-id="df2dc-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="df2dc-120">Az-modulen har ett kompatibilitetsläge som hjälp om du vill använda befintliga skript medan du arbetar med uppdateringar till den nya syntaxen.</span><span class="sxs-lookup"><span data-stu-id="df2dc-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="df2dc-121">Använd cmdleten `Enable-AzureRmAlias` för att aktivera AzureRM-kompatibilitetsläget.</span><span class="sxs-lookup"><span data-stu-id="df2dc-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="df2dc-122">Denna cmdlet definierar AzureRM-cmdletnamn som alias för de nya Az-cmdletnamnen.</span><span class="sxs-lookup"><span data-stu-id="df2dc-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="df2dc-123">De nya cmdlet-namnen har utformats för att vara lätta att lära sig.</span><span class="sxs-lookup"><span data-stu-id="df2dc-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="df2dc-124">I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`.</span><span class="sxs-lookup"><span data-stu-id="df2dc-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="df2dc-125">Det gamla kommandot `New-AzureRMVm` har till exempel blivit `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="df2dc-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="df2dc-126">En fullständig beskrivning av migreringsprocessen finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="df2dc-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="df2dc-127">Stöd för AzureRM i framtiden</span><span class="sxs-lookup"><span data-stu-id="df2dc-127">The future of support for AzureRM</span></span>

<span data-ttu-id="df2dc-128">Den befintliga AzureRM-modulen tar inte längre emot nya cmdletar eller funktioner.</span><span class="sxs-lookup"><span data-stu-id="df2dc-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="df2dc-129">AzureRM underhålls dock fortfarande officiellt och får nya buggkorrigeringar fram till december 2020.</span><span class="sxs-lookup"><span data-stu-id="df2dc-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="df2dc-130">Byt till Az-modulen om du vill hålla dig uppdaterad med de senaste Azure-tjänsterna och -funktionerna.</span><span class="sxs-lookup"><span data-stu-id="df2dc-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
