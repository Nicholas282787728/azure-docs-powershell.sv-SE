---
title: Alla ändringar från AzureRM till Azure PowerShell Az 1.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 1 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: 1d99f04525a33f03f859bfb4abe263b12ca6add9
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516767"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="026cb-103">Icke-bakåtkompatibla ändringar för Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="026cb-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="026cb-104">I det här dokumentet finns detaljerad information om ändringar mellan AzureRM 6.x och den nya Az-modulen, version 1.x och senare.</span><span class="sxs-lookup"><span data-stu-id="026cb-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="026cb-105">Innehållsförteckningen leder dig genom en fullständig migrering, inklusive modulspecifika ändringar som kan påverka skripten.</span><span class="sxs-lookup"><span data-stu-id="026cb-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="026cb-106">Allmänna råd om hur du kommer igång med en migrering från AzureRM till Az finns i [Starta migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="026cb-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="026cb-107">Vi har infört icke-bakåtkompatibla ändringar mellan Az 1.0.0 och Az 2.0.0 också.</span><span class="sxs-lookup"><span data-stu-id="026cb-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="026cb-108">När du har följt den guiden om hur du uppdaterar från AzureRM till Az kan du läsa om [icke-bakåtkompatibla ändringar för Az 2.0.0](migrate-az-2.0.0.md) att ta reda på om du behöver göra ytterligare ändringar.</span><span class="sxs-lookup"><span data-stu-id="026cb-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="026cb-109">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="026cb-109">Table of Contents</span></span>

- [<span data-ttu-id="026cb-110">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="026cb-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="026cb-111">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="026cb-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="026cb-112">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="026cb-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="026cb-113">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="026cb-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="026cb-114">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="026cb-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="026cb-115">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="026cb-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="026cb-116">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="026cb-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="026cb-117">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="026cb-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="026cb-118">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="026cb-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="026cb-119">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="026cb-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="026cb-120">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="026cb-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="026cb-121">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="026cb-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="026cb-122">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="026cb-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="026cb-123">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="026cb-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="026cb-124">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="026cb-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="026cb-125">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="026cb-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="026cb-126">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="026cb-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="026cb-127">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="026cb-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="026cb-128">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="026cb-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="026cb-129">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="026cb-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="026cb-130">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="026cb-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="026cb-131">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="026cb-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="026cb-132">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="026cb-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="026cb-133">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="026cb-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="026cb-134">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="026cb-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="026cb-135">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="026cb-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="026cb-136">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="026cb-136">General breaking changes</span></span>

<span data-ttu-id="026cb-137">I det här avsnittet beskriver vi de allmänna icke-bakåtkompatibla ändringarna i den nya utformningen av Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="026cb-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="026cb-138">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="026cb-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="026cb-139">I AzureRM-modulen är de cmdletar som används antingen `AzureRM` eller `Azure` som ett substantivprefix.</span><span class="sxs-lookup"><span data-stu-id="026cb-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="026cb-140">Az förenklar och normaliserar cmdlet-namn så att Az används som cmdlet-substantivprefix för alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="026cb-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="026cb-141">Exempel:</span><span class="sxs-lookup"><span data-stu-id="026cb-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="026cb-142">Har ändrats till:</span><span class="sxs-lookup"><span data-stu-id="026cb-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="026cb-143">För att göra övergången till de nya cmdlet-namnen enklare introduceras två nya cmdletar, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) och [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="026cb-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="026cb-144">`Enable-AzureRmAlias` skapar alias för de äldre cmdlet-namnen i AzureRM till de nyare cmdlet-namnen i Az.</span><span class="sxs-lookup"><span data-stu-id="026cb-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="026cb-145">Med argumentet `-Scope` med `Enable-AzureRmAlias` kan du välja var alias ska aktiveras.</span><span class="sxs-lookup"><span data-stu-id="026cb-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="026cb-146">Till exempel kan följande skript i AzureRM:</span><span class="sxs-lookup"><span data-stu-id="026cb-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="026cb-147">Kan köras med minimala ändringar med `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="026cb-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="026cb-148">När `Enable-AzureRmAlias -Scope CurrentUser` körs kan alias aktiveras för alla PowerShell-sessioner som du öppnar, så när denna cmdlet har körts behöver ett skript som detta inte ändras alls:</span><span class="sxs-lookup"><span data-stu-id="026cb-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="026cb-149">All information om användningen av alias-cmdletar finns i [referensmaterialet för Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="026cb-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="026cb-150">När du är redo att inaktivera alias tar `Disable-AzureRmAlias` bort skapade alias.</span><span class="sxs-lookup"><span data-stu-id="026cb-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="026cb-151">All information finns i [referensmaterialet till Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="026cb-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="026cb-152">När du inaktiverar alias ska du se till att de är inaktiverade för _alla_ omfång som har aktiverade alias.</span><span class="sxs-lookup"><span data-stu-id="026cb-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="026cb-153">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="026cb-153">Module Name Changes</span></span>

<span data-ttu-id="026cb-154">Modulnamnen har ändrats från `AzureRM.*` till `Az.*`, förutom följande moduler:</span><span class="sxs-lookup"><span data-stu-id="026cb-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="026cb-155">AzureRM-modul</span><span class="sxs-lookup"><span data-stu-id="026cb-155">AzureRM module</span></span> | <span data-ttu-id="026cb-156">Az-modul</span><span class="sxs-lookup"><span data-stu-id="026cb-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="026cb-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="026cb-157">Azure.Storage</span></span> | <span data-ttu-id="026cb-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="026cb-158">Az.Storage</span></span> |
| <span data-ttu-id="026cb-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="026cb-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="026cb-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="026cb-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="026cb-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="026cb-161">AzureRM.Profile</span></span> | <span data-ttu-id="026cb-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="026cb-162">Az.Accounts</span></span> |
| <span data-ttu-id="026cb-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="026cb-163">AzureRM.Insights</span></span> | <span data-ttu-id="026cb-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="026cb-164">Az.Monitor</span></span> |
| <span data-ttu-id="026cb-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="026cb-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="026cb-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="026cb-166">Az.DataFactory</span></span> |
| <span data-ttu-id="026cb-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="026cb-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="026cb-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="026cb-168">Az.DataFactory</span></span> |
| <span data-ttu-id="026cb-169">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="026cb-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="026cb-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="026cb-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="026cb-171">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="026cb-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="026cb-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="026cb-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="026cb-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="026cb-173">AzureRM.Tags</span></span> | <span data-ttu-id="026cb-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="026cb-174">Az.Resources</span></span> |
| <span data-ttu-id="026cb-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="026cb-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="026cb-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="026cb-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="026cb-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="026cb-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="026cb-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="026cb-178">Az.Billing</span></span> |
| <span data-ttu-id="026cb-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="026cb-179">AzureRM.Consumption</span></span> | <span data-ttu-id="026cb-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="026cb-180">Az.Billing</span></span> |

<span data-ttu-id="026cb-181">Ändringarna i modulnamnen innebär att alla skript som använder `#Requires` eller `Import-Module` för att läsa in specifika moduler måste ändras så att de använder den nya modulen i stället.</span><span class="sxs-lookup"><span data-stu-id="026cb-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="026cb-182">För moduler där cmdletsuffixet inte har ändrats innebär det att även om modulnamnet har ändrats har suffixet som anger åtgärdsutrymmet _inte_ det.</span><span class="sxs-lookup"><span data-stu-id="026cb-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="026cb-183">Migrera instruktioner av typen #Requires och Import-Module</span><span class="sxs-lookup"><span data-stu-id="026cb-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="026cb-184">Skript som använder `#Requires` eller `Import-Module` för att deklarera beroende av AzureRM-moduler måste uppdateras så att de nya modulnamnen används.</span><span class="sxs-lookup"><span data-stu-id="026cb-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="026cb-185">Exempel:</span><span class="sxs-lookup"><span data-stu-id="026cb-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="026cb-186">Ska ändras till:</span><span class="sxs-lookup"><span data-stu-id="026cb-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="026cb-187">För `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="026cb-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="026cb-188">Ska ändras till:</span><span class="sxs-lookup"><span data-stu-id="026cb-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="026cb-189">Migrera fullständigt kvalificerade cmdlet-anrop</span><span class="sxs-lookup"><span data-stu-id="026cb-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="026cb-190">Skript som använder modulkvalificerade cmdlet-anrop som:</span><span class="sxs-lookup"><span data-stu-id="026cb-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="026cb-191">Måste ändras så att de nya modul- och cmdlet-namnen används</span><span class="sxs-lookup"><span data-stu-id="026cb-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="026cb-192">Migrera modulmanifestberoenden</span><span class="sxs-lookup"><span data-stu-id="026cb-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="026cb-193">För moduler som uttrycker beroenden av AzureRM-moduler via en modulmanifestfil (.psd1) behöver modulnamnen uppdateras i avsnittet `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="026cb-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="026cb-194">Måste ändras till:</span><span class="sxs-lookup"><span data-stu-id="026cb-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="026cb-195">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="026cb-195">Removed modules</span></span>

<span data-ttu-id="026cb-196">Följande moduler har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="026cb-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="026cb-197">Verktygen för de här tjänsterna stöds inte längre aktivt.</span><span class="sxs-lookup"><span data-stu-id="026cb-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="026cb-198">Kunderna rekommenderas att övergå till alternativa tjänster så snart som möjligt.</span><span class="sxs-lookup"><span data-stu-id="026cb-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="026cb-199">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="026cb-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="026cb-200">Om Az ska användas med PowerShell 5.1 för Windows måste .NET Framework 4.7.2 vara installerat.</span><span class="sxs-lookup"><span data-stu-id="026cb-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="026cb-201">För PowerShell Core 6.x och senare krävs inte .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="026cb-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="026cb-202">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="026cb-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="026cb-203">På grund av ändringar i autentiseringsflödet för .NET Standard tar vi tillfälligt bort användarinloggning med PSCredential.</span><span class="sxs-lookup"><span data-stu-id="026cb-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="026cb-204">Funktionen återintroduceras i version 1/15/2019/ av Windows PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="026cb-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="026cb-205">Det här diskuteras mer ingående i [det här GitHub-ärendet.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="026cb-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="026cb-206">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="026cb-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="026cb-207">På grund av ändringar i autentiseringsflödet för .NET Standard använder vi enhetsinloggning som standardinloggningsflöde under interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="026cb-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="026cb-208">Webbläsarbaserad webbinloggning återintroduceras som standardfunktion i version 1/15/2019 av PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="026cb-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="026cb-209">Då kan användarna välja enhetsinloggning med hjälp av en växlingsparameter.</span><span class="sxs-lookup"><span data-stu-id="026cb-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="026cb-210">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="026cb-210">Module breaking changes</span></span>

<span data-ttu-id="026cb-211">I det här avsnittet beskriver vi icke-bakåtkompatibla ändringar för enskilda moduler och cmdletar.</span><span class="sxs-lookup"><span data-stu-id="026cb-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="026cb-212">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="026cb-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="026cb-213">Följande cmdletar togs bort:</span><span class="sxs-lookup"><span data-stu-id="026cb-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="026cb-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="026cb-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="026cb-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="026cb-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="026cb-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="026cb-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="026cb-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="026cb-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="026cb-218">Använd istället cmdleten **Set-AzApiManagement** för att ställa dessa egenskaper</span><span class="sxs-lookup"><span data-stu-id="026cb-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="026cb-219">Följande egenskaper togs bort:</span><span class="sxs-lookup"><span data-stu-id="026cb-219">Removed the following properties:</span></span>
  - <span data-ttu-id="026cb-220">Egenskapen `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` och `ScmHostnameConfiguration` av typen `PsApiManagementHostnameConfiguration` har tagits bort från `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="026cb-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="026cb-221">Använd i stället `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` och `ScmCustomHostnameConfiguration` av typen `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="026cb-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="026cb-222">Egenskapen `StaticIPs` har tagits bort från PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="026cb-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="026cb-223">Egenskapen har delats upp i `PublicIPAddresses` och `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="026cb-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="026cb-224">Den nödvändiga egenskapen `Location` har tagits bort från cmdleten New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="026cb-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="026cb-225">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="026cb-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="026cb-226">Parametern `InvoiceName` har tagits bort från cmdleten `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="026cb-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="026cb-227">Skripten behöver nu använda andra identitetsparametrar för fakturan.</span><span class="sxs-lookup"><span data-stu-id="026cb-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="026cb-228">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="026cb-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="026cb-229">Parameteruppsättningen `GetSkusWithAccountParamSetName` har tagits bort från cmdleten `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="026cb-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="026cb-230">Du måste hämta SKU:er efter typ och plats i stället för att använda ResourceGroupName och Account Name.</span><span class="sxs-lookup"><span data-stu-id="026cb-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="026cb-231">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="026cb-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="026cb-232">`IdentityIds` tas bort från egenskapen `Identity` i objekten `PSVirtualMachine` och `PSVirtualMachineScaleSet` Skripten bör nu inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="026cb-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="026cb-233">Typ av `InstanceView`-egenskap för `PSVirtualMachineScaleSetVM`-objekt ändras från `VirtualMachineInstanceView` till `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="026cb-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="026cb-234">Egenskaperna `AutoOSUpgradePolicy` och `AutomaticOSUpgrade` tas bort från egenskapen `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="026cb-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="026cb-235">Typ av `Sku`-egenskap i `PSSnapshotUpdate`-objekt ändras från `DiskSku` till `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="026cb-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="026cb-236">`VmScaleSetVMParameterSet` tas bort från cmdleten `Add-AzVMDataDisk`, och du kan inte längre lägga till en datadisk individuellt till en virtuell ScaleSet-dator.</span><span class="sxs-lookup"><span data-stu-id="026cb-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="026cb-237">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="026cb-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="026cb-238">Parametern `GatewayName` har blivit obligatorisk i cmdleten `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="026cb-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="026cb-239">Cmdleten `New-AzDataFactoryGatewayKey` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="026cb-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="026cb-240">Parametern `LinkedServiceName` har tagits bort från cmdleten `Get-AzDataFactoryV2ActivityRun` Skripten ska inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="026cb-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="026cb-241">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="026cb-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="026cb-242">Följande inaktuella cmdletar har tagits bort: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` och `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="026cb-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="026cb-243">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="026cb-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="026cb-244">I följande cmdletar har parametern `Encoding` ändrats från typen `FileSystemCmdletProviderEncoding` till `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="026cb-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="026cb-245">Den här ändringen tar bort kodningsvärdena `String` och `Oem`.</span><span class="sxs-lookup"><span data-stu-id="026cb-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="026cb-246">Övriga tidigare kodningsvärden kvarstår.</span><span class="sxs-lookup"><span data-stu-id="026cb-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="026cb-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="026cb-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="026cb-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="026cb-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="026cb-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="026cb-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="026cb-250">Det inaktuella egenskapsaliaset `Tags` har tagits bort från cmdletarna `New-AzDataLakeStoreAccount` och `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="026cb-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="026cb-251">Skript som använder</span><span class="sxs-lookup"><span data-stu-id="026cb-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="026cb-252">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="026cb-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="026cb-253">De inaktuella egenskaperna `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` har tagits bort från `PSDataLakeStoreAccountBasic`-objekt.</span><span class="sxs-lookup"><span data-stu-id="026cb-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="026cb-254">Alla skript som använder den `PSDatalakeStoreAccount` som returnerades från `Get-AzDataLakeStoreAccount` ska inte längre referera till dessa egenskaper.</span><span class="sxs-lookup"><span data-stu-id="026cb-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="026cb-255">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="026cb-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="026cb-256">Egenskapen `PurgeDisabled` har tagits bort från `PSKeyVaultKeyAttributes`-, `PSKeyVaultKeyIdentityItem`- och `PSKeyVaultSecretAttributes`-objekt Skript ska inte längre referera till egenskapen ```PurgeDisabled``` för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="026cb-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="026cb-257">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="026cb-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="026cb-258">Tog bort inaktuellt egenskapsalias `Tags` från skript för cmdleten `New-AzMediaService` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="026cb-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="026cb-259">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="026cb-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="026cb-260">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="026cb-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="026cb-261">Tog bort pluralnamnet `Categories` och parametern `Timegrains` och ersatte med singularparameternamn från cmdlet-skript för `Set-AzDiagnosticSetting` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="026cb-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="026cb-262">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="026cb-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="026cb-263">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="026cb-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="026cb-264">Tog bort den inaktuella parametern `ResourceId` från cmdleten `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="026cb-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="026cb-265">Tog bort den inaktuella egenskapen `EnableVmProtection` från objektet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="026cb-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="026cb-266">Tog bort den inaktuella cmdleten `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="026cb-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="026cb-267">Skript bör inte längre fatta bearbetningsbeslut baserat på värdena för dessa fält.</span><span class="sxs-lookup"><span data-stu-id="026cb-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="026cb-268">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="026cb-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="026cb-269">Standardparameteruppsättningen för `Get-AzOperationalInsightsDataSource` har tagits bort och `ByWorkspaceNameByKind` är nu standardparameteruppsättning</span><span class="sxs-lookup"><span data-stu-id="026cb-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="026cb-270">Skript som listar datakällor med hjälp av</span><span class="sxs-lookup"><span data-stu-id="026cb-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="026cb-271">ska ändras så att de anger en typ</span><span class="sxs-lookup"><span data-stu-id="026cb-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="026cb-272">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="026cb-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="026cb-273">Parametern `Encryption` har tagits bort från cmdleten `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="026cb-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="026cb-274">Parametern `TargetStorageAccountName` är nu obligatorisk för hanterade diskåterställningar i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="026cb-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="026cb-275">Tog bort parametrarna `StorageAccountName` och `StorageAccountResourceGroupName` i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="026cb-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="026cb-276">Tog bort parametern `Name` i cmdleten `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="026cb-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="026cb-277">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="026cb-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="026cb-278">Parametern `Sku` har tagits bort från cmdleten `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="026cb-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="026cb-279">Parametern `Password` har tagits bort från cmdleten `New-AzADServicePrincipal` och `New-AzADSpCredential` Lösenord genereras automatiskt och skript som tillhandahöll lösenordet:</span><span class="sxs-lookup"><span data-stu-id="026cb-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="026cb-280">Bör ändras så att de hämtar lösenordet från utdata:</span><span class="sxs-lookup"><span data-stu-id="026cb-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="026cb-281">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="026cb-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="026cb-282">Följande cmdlet-returtyper har ändrats:</span><span class="sxs-lookup"><span data-stu-id="026cb-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="026cb-283">Egenskapen `ServiceTypeHealthPolicies` av typen `ApplicationHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="026cb-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="026cb-284">Egenskapen `ApplicationHealthPolicies` av typen `ClusterUpgradeDeltaHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="026cb-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="026cb-285">Egenskapen `OverrideUserUpgradePolicy` av typen `ClusterUpgradePolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="026cb-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="026cb-286">Ändringarna påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="026cb-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="026cb-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="026cb-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="026cb-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="026cb-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="026cb-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="026cb-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="026cb-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="026cb-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="026cb-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="026cb-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="026cb-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="026cb-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="026cb-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="026cb-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="026cb-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="026cb-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="026cb-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="026cb-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="026cb-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="026cb-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="026cb-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="026cb-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="026cb-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="026cb-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="026cb-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="026cb-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="026cb-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="026cb-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="026cb-301">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="026cb-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="026cb-302">Tog bort parametrarna `State` och `ResourceId` från cmdleten `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="026cb-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="026cb-303">Följande inaktuella cmdletar har tagits bort: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="026cb-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="026cb-304">Tog bort den inaktuella parametern `Current` från cmdleten `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="026cb-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="026cb-305">Tog bort den inaktuella parametern `DatabaseName` från cmdleten `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="026cb-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="026cb-306">Tog bort den inaktuella parametern `PrivilegedLogin` från cmdleten `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="026cb-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="026cb-307">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="026cb-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="026cb-308">Standardparameteruppsättningen har ändrats till `OAuthParameterSet` för att det ska gå att skapa en Oauth-lagringskontext endast med namnet på lagringskontot</span><span class="sxs-lookup"><span data-stu-id="026cb-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="026cb-309">Exempel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="026cb-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="026cb-310">Parametern `Location` har blivit obligatorisk i cmdleten `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="026cb-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="026cb-311">Storage-API-metoderna använder nu TAP (uppgiftsbaserat asynkront mönster) i stället för synkrona API-anrop.</span><span class="sxs-lookup"><span data-stu-id="026cb-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="026cb-312">Följande exempel visar de nya asynkrona kommandona:</span><span class="sxs-lookup"><span data-stu-id="026cb-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="026cb-313">Blobögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="026cb-313">Blob Snapshot</span></span>

<span data-ttu-id="026cb-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="026cb-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="026cb-315">Az:</span><span class="sxs-lookup"><span data-stu-id="026cb-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="026cb-316">Dela ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="026cb-316">Share Snapshot</span></span>

<span data-ttu-id="026cb-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="026cb-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="026cb-318">Az:</span><span class="sxs-lookup"><span data-stu-id="026cb-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="026cb-319">Ångra borttagning av mjukborttagen blob</span><span class="sxs-lookup"><span data-stu-id="026cb-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="026cb-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="026cb-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="026cb-321">Az:</span><span class="sxs-lookup"><span data-stu-id="026cb-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="026cb-322">Ange blobnivå</span><span class="sxs-lookup"><span data-stu-id="026cb-322">Set Blob Tier</span></span>

<span data-ttu-id="026cb-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="026cb-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="026cb-324">Az:</span><span class="sxs-lookup"><span data-stu-id="026cb-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="026cb-325">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="026cb-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="026cb-326">Inaktuella egenskaper har tagits bort från `PSAppServicePlan`-, `PSCertificate`-, `PSCloningInfo`- och `PSSite`-objekten</span><span class="sxs-lookup"><span data-stu-id="026cb-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
