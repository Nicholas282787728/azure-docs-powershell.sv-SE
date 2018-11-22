---
title: Introduktion till Azure PowerShell Az-modulen
description: Vi introducerar den nya Azure PowerShell-modulen Az, som ersätter AzureRM-modulen.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259970"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="e3eb3-103">Introduktion till den nya Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="e3eb3-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="e3eb3-104">Från november 2018 är Azure PowerShell `Az`-modulen tillgänglig som fullständig offentlig förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="e3eb3-105">Az erbjuder kortare kommandon, förbättrad stabilitet och har stöd för Windows, macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="e3eb3-106">Az erbjuder också funktionsparitet och en enkel migreringsväg från AzureRM.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="e3eb3-107">Az använder .NET Standard-biblioteket, vilket innebär att den körs på PowerShell 5.x och PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="e3eb3-108">Eftersom PowerShell 6.x kan köras på Linux, macOS och Windows innebär det att Az är tillgänglig för alla plattformar.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="e3eb3-109">Med .NET Standard kan vi förena kodbasen för Azure PowerShell med minimal inverkan på användare.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="e3eb3-110">Az är en ny modul, så versionen har nollställts.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="e3eb3-111">Den första stabila versionen blir 1.0, men modulen har funktionsparitet med AzureRm från november 2018.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="e3eb3-112">Uppgradera till Az</span><span class="sxs-lookup"><span data-stu-id="e3eb3-112">Upgrade to Az</span></span>

<span data-ttu-id="e3eb3-113">Vi rekommenderar att användare uppgraderar till den nya `Az`-modulen.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="e3eb3-114">Gör så här:</span><span class="sxs-lookup"><span data-stu-id="e3eb3-114">To do so:</span></span>

* [<span data-ttu-id="e3eb3-115">Avinstallera Azure PowerShell AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="e3eb3-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="e3eb3-116">Installera Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="e3eb3-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="e3eb3-117">Aktivera kompatibilitetsläge för AzureRM med `Enable-AzureRMAlias` medan du bekantar dig med den nya kommandouppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="e3eb3-118">Migrera befintliga skript till Az</span><span class="sxs-lookup"><span data-stu-id="e3eb3-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="e3eb3-119">Stora uppdateringar kan vara olägliga.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="e3eb3-120">Men `Az`-modulen har ett kompatibilitetsläge som hjälper dig att använda befintliga skript medan du arbetar med uppdateringar till den nya syntaxen.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="e3eb3-121">Använd `Enable-AzureRmAlias`-cmdleten för att aktivera `AzureRM`-kompatibilitetsläget.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="e3eb3-122">Denna cmdlet definierar `AzureRM`-cmdlet-namn som alias för de nya `Az`-cmdlet-namnen.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="e3eb3-123">De nya cmdlet-namnen har utformats för att vara lätta att lära sig.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="e3eb3-124">I stället för att använda `AzureRm` eller `Azure` i cmdlet-namn använder du `Az`.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="e3eb3-125">Det gamla kommandot `New-AzureRmVm` har till exempel blivit `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="e3eb3-126">En fullständig beskrivning av migreringsprocessen finns i [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="e3eb3-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="e3eb3-127">Stöd för AzureRM i framtiden</span><span class="sxs-lookup"><span data-stu-id="e3eb3-127">The future of support for AzureRM</span></span>

<span data-ttu-id="e3eb3-128">Den befintliga `AzureRM`-modulen får inte längre nya cmdletar eller funktioner när `Az` version 1.0 släpps i december 2018.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="e3eb3-129">`AzureRM` underhålls emellertid fortfarande officiellt och får felkorrigeringar.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="e3eb3-130">Om du vill hålla dig uppdaterad med de senaste Azure-tjänsterna och -funktionerna bör du byta till `Az`-modulen.</span><span class="sxs-lookup"><span data-stu-id="e3eb3-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>