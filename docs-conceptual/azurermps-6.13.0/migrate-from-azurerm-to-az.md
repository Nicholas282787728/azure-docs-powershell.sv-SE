---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587711"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="d4c34-103">Migrera från AzureRM till Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="d4c34-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="d4c34-104">Az-modulen har funktionsparitet med AzureRM, men använder kortare och mer konsekventa cmdlet-namn.</span><span class="sxs-lookup"><span data-stu-id="d4c34-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="d4c34-105">Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen.</span><span class="sxs-lookup"><span data-stu-id="d4c34-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="d4c34-106">För att underlätta övergången erbjuder Az verktyg så att du kan köra dina befintliga skript med hjälp av AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d4c34-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="d4c34-107">Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till den nya modulen.</span><span class="sxs-lookup"><span data-stu-id="d4c34-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="d4c34-108">Se till att dina befintliga skript fungerar med den senaste versionen av AzureRM</span><span class="sxs-lookup"><span data-stu-id="d4c34-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="d4c34-109">Det här är det viktigaste steget!</span><span class="sxs-lookup"><span data-stu-id="d4c34-109">This is the most important step!</span></span> <span data-ttu-id="d4c34-110">Kör dina befintliga skript och se till att de fungerar med den _senaste_ versionen av AzureRM (__6.13.0__).</span><span class="sxs-lookup"><span data-stu-id="d4c34-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.13.0__).</span></span> <span data-ttu-id="d4c34-111">Om dina skript inte fungerar läser du [AzureRM-migreringsguiden](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="d4c34-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="d4c34-112">Installera Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="d4c34-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="d4c34-113">Första steget är att installera Az-modulen på din plattform.</span><span class="sxs-lookup"><span data-stu-id="d4c34-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="d4c34-114">För att kunna installera Az måste du avinstallera AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d4c34-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="d4c34-115">I följande steg får du lära dig hur du fortsätter att köra dina befintliga skript och aktiverar kompatibilitet för gamla cmdlet-namn.</span><span class="sxs-lookup"><span data-stu-id="d4c34-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="d4c34-116">Installera Azure PowerShell Az-modulen enligt följande:</span><span class="sxs-lookup"><span data-stu-id="d4c34-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="d4c34-117">[Avinstallera AzureRM-modulen](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d4c34-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="d4c34-118">Se till att ta bort _alla_ installerade versioner av AzureRM, inte bara den senaste versionen.</span><span class="sxs-lookup"><span data-stu-id="d4c34-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="d4c34-119">Installera Az-modulen</span><span class="sxs-lookup"><span data-stu-id="d4c34-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="d4c34-120"><a name="aliases"/>Aktivera AzureRM-aliasläge</span><span class="sxs-lookup"><span data-stu-id="d4c34-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="d4c34-121">När AzureRM har avinstallerats och skripten fungerar med den senaste AzureRM-versionen är det dags att aktivera kompatibilitetsläget för Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="d4c34-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="d4c34-122">Kompatibilitet aktiveras med kommandot:</span><span class="sxs-lookup"><span data-stu-id="d4c34-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="d4c34-123">Alias gör det möjligt att använda gamla cmdlet-namn med `Az`-modulen installerad.</span><span class="sxs-lookup"><span data-stu-id="d4c34-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="d4c34-124">Dessa alias skrivs till användarprofilen för det valda omfånget.</span><span class="sxs-lookup"><span data-stu-id="d4c34-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="d4c34-125">Om det inte finns någon användarprofil skapas en.</span><span class="sxs-lookup"><span data-stu-id="d4c34-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="d4c34-126">Du kan använda ett annat `-Scope` för det här kommandot, men det rekommenderas inte!</span><span class="sxs-lookup"><span data-stu-id="d4c34-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="d4c34-127">Alias skrivs till användarprofilen för det valda omfånget, så fortsätt att aktivera dem för ett så begränsat omfång som möjligt.</span><span class="sxs-lookup"><span data-stu-id="d4c34-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="d4c34-128">Aktivering av alias i hela systemet kan också orsaka problem för andra användare som har `AzureRM` installerad i sitt lokala omfång.</span><span class="sxs-lookup"><span data-stu-id="d4c34-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="d4c34-129">När aliasläget har aktiverats kör du skripten igen för att bekräfta att de fortfarande fungerar som förväntat.</span><span class="sxs-lookup"><span data-stu-id="d4c34-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="d4c34-130">Ändra modulimporter och cmdlet-namn</span><span class="sxs-lookup"><span data-stu-id="d4c34-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="d4c34-131">I allmänhet har modulnamnen ändrats så att `AzureRM` och `Azure` blir `Az`, och samma sak för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="d4c34-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="d4c34-132">`AzureRM.Compute`-modulens namn har till exempel ändrats till `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="d4c34-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="d4c34-133">`New-AzureRmVM` har blivit `New-AzVM`, och `Get-AzureStorageBlob` är nu `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="d4c34-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="d4c34-134">Det finns undantag till den här namngivningsändringen som du bör känna till innan du ändrar några namn:</span><span class="sxs-lookup"><span data-stu-id="d4c34-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="d4c34-135">AzureRM-modul</span><span class="sxs-lookup"><span data-stu-id="d4c34-135">AzureRM module</span></span> | <span data-ttu-id="d4c34-136">Az-modul</span><span class="sxs-lookup"><span data-stu-id="d4c34-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="d4c34-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="d4c34-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="d4c34-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4c34-138">Az.DataFactory</span></span> |
| <span data-ttu-id="d4c34-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d4c34-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="d4c34-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4c34-140">Az.DataFactory</span></span> |
| <span data-ttu-id="d4c34-141">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4c34-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="d4c34-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4c34-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="d4c34-143">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4c34-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="d4c34-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4c34-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="d4c34-145">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4c34-145">Summary</span></span>

<span data-ttu-id="d4c34-146">Genom att följa de här stegen kan du uppdatera alla befintliga skript så att de använder den nya modulen.</span><span class="sxs-lookup"><span data-stu-id="d4c34-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="d4c34-147">Om du har några frågor eller problem med de här stegen som har gjort migreringen svår får du gärna kommentera den här artikeln så att vi kan förbättra instruktionerna.</span><span class="sxs-lookup"><span data-stu-id="d4c34-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>
