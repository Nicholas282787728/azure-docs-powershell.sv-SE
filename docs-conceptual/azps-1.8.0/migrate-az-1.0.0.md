---
title: Alla ändringar från AzureRM till Azure PowerShell Az 1.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 1 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 81aa067d6d5ea868f317ee8086038c59c89f0384
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408432"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="42cfe-103">Icke-bakåtkompatibla ändringar för Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="42cfe-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="42cfe-104">I det här dokumentet finns detaljerad information om ändringar mellan AzureRM 6.x och den nya Az-modulen, version 1.x och senare.</span><span class="sxs-lookup"><span data-stu-id="42cfe-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="42cfe-105">Innehållsförteckningen leder dig genom en fullständig migrering, inklusive modulspecifika ändringar som kan påverka skripten.</span><span class="sxs-lookup"><span data-stu-id="42cfe-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="42cfe-106">Allmänna råd om hur du kommer igång med en migrering från AzureRM till Az finns i [Starta migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="42cfe-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="42cfe-107">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="42cfe-107">Table of Contents</span></span>

- [<span data-ttu-id="42cfe-108">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42cfe-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="42cfe-109">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="42cfe-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="42cfe-110">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="42cfe-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="42cfe-111">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="42cfe-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="42cfe-112">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="42cfe-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="42cfe-113">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="42cfe-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="42cfe-114">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="42cfe-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="42cfe-115">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42cfe-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="42cfe-116">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="42cfe-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="42cfe-117">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="42cfe-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="42cfe-118">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="42cfe-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="42cfe-119">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="42cfe-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="42cfe-120">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="42cfe-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="42cfe-121">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="42cfe-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="42cfe-122">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="42cfe-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="42cfe-123">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="42cfe-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="42cfe-124">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="42cfe-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="42cfe-125">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="42cfe-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="42cfe-126">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="42cfe-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="42cfe-127">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="42cfe-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="42cfe-128">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="42cfe-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="42cfe-129">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="42cfe-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="42cfe-130">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="42cfe-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="42cfe-131">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="42cfe-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="42cfe-132">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="42cfe-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="42cfe-133">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="42cfe-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="42cfe-134">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42cfe-134">General breaking changes</span></span>

<span data-ttu-id="42cfe-135">I det här avsnittet beskriver vi de allmänna icke-bakåtkompatibla ändringarna i den nya utformningen av Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="42cfe-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="42cfe-136">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="42cfe-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="42cfe-137">I AzureRM-modulen är de cmdletar som används antingen `AzureRM` eller `Azure` som ett substantivprefix.</span><span class="sxs-lookup"><span data-stu-id="42cfe-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="42cfe-138">Az förenklar och normaliserar cmdlet-namn så att Az används som cmdlet-substantivprefix för alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42cfe-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="42cfe-139">Ett exempel:</span><span class="sxs-lookup"><span data-stu-id="42cfe-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="42cfe-140">Har ändrats till:</span><span class="sxs-lookup"><span data-stu-id="42cfe-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="42cfe-141">För att göra övergången till de nya cmdlet-namnen enklare introduceras två nya cmdletar, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) och [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="42cfe-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="42cfe-142">`Enable-AzureRmAlias` skapar alias för de äldre cmdlet-namnen i AzureRM till de nyare cmdlet-namnen i Az.</span><span class="sxs-lookup"><span data-stu-id="42cfe-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="42cfe-143">Med argumentet `-Scope` med `Enable-AzureRmAlias` kan du välja var alias ska aktiveras.</span><span class="sxs-lookup"><span data-stu-id="42cfe-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="42cfe-144">Till exempel kan följande skript i AzureRM:</span><span class="sxs-lookup"><span data-stu-id="42cfe-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="42cfe-145">Kan köras med minimala ändringar med `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="42cfe-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="42cfe-146">När `Enable-AzureRmAlias -Scope CurrentUser` körs kan alias aktiveras för alla PowerShell-sessioner som du öppnar, så när denna cmdlet har körts behöver ett skript som detta inte ändras alls:</span><span class="sxs-lookup"><span data-stu-id="42cfe-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="42cfe-147">All information om användningen av alias-cmdletar finns i [referensmaterialet för Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="42cfe-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="42cfe-148">När du är redo att inaktivera alias tar `Disable-AzureRmAlias` bort skapade alias.</span><span class="sxs-lookup"><span data-stu-id="42cfe-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="42cfe-149">All information finns i [referensmaterialet till Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="42cfe-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42cfe-150">När du inaktiverar alias ska du se till att de är inaktiverade för _alla_ omfång som har aktiverade alias.</span><span class="sxs-lookup"><span data-stu-id="42cfe-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="42cfe-151">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="42cfe-151">Module Name Changes</span></span>

<span data-ttu-id="42cfe-152">Modulnamnen har ändrats från `AzureRM.*` till `Az.*`, förutom följande moduler:</span><span class="sxs-lookup"><span data-stu-id="42cfe-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="42cfe-153">AzureRM-modul</span><span class="sxs-lookup"><span data-stu-id="42cfe-153">AzureRM module</span></span> | <span data-ttu-id="42cfe-154">Az-modul</span><span class="sxs-lookup"><span data-stu-id="42cfe-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="42cfe-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="42cfe-155">Azure.Storage</span></span> | <span data-ttu-id="42cfe-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42cfe-156">Az.Storage</span></span> |
| <span data-ttu-id="42cfe-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="42cfe-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="42cfe-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="42cfe-159">AzureRM.Profile</span></span> | <span data-ttu-id="42cfe-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42cfe-160">Az.Accounts</span></span> |
| <span data-ttu-id="42cfe-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="42cfe-161">AzureRM.Insights</span></span> | <span data-ttu-id="42cfe-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42cfe-162">Az.Monitor</span></span> |
| <span data-ttu-id="42cfe-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="42cfe-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="42cfe-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42cfe-164">Az.DataFactory</span></span> |
| <span data-ttu-id="42cfe-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="42cfe-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="42cfe-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42cfe-166">Az.DataFactory</span></span> |
| <span data-ttu-id="42cfe-167">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="42cfe-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="42cfe-169">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="42cfe-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42cfe-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="42cfe-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="42cfe-171">AzureRM.Tags</span></span> | <span data-ttu-id="42cfe-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42cfe-172">Az.Resources</span></span> |
| <span data-ttu-id="42cfe-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="42cfe-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="42cfe-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42cfe-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="42cfe-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="42cfe-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="42cfe-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="42cfe-176">Az.Billing</span></span> |
| <span data-ttu-id="42cfe-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="42cfe-177">AzureRM.Consumption</span></span> | <span data-ttu-id="42cfe-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="42cfe-178">Az.Billing</span></span> |

<span data-ttu-id="42cfe-179">Ändringarna i modulnamnen innebär att alla skript som använder `#Requires` eller `Import-Module` för att läsa in specifika moduler måste ändras så att de använder den nya modulen i stället.</span><span class="sxs-lookup"><span data-stu-id="42cfe-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="42cfe-180">För moduler där cmdletsuffixet inte har ändrats innebär det att även om modulnamnet har ändrats har suffixet som anger åtgärdsutrymmet _inte_ det.</span><span class="sxs-lookup"><span data-stu-id="42cfe-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="42cfe-181">Migrera instruktioner av typen #Requires och Import-Module</span><span class="sxs-lookup"><span data-stu-id="42cfe-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="42cfe-182">Skript som använder `#Requires` eller `Import-Module` för att deklarera beroende av AzureRM-moduler måste uppdateras så att de nya modulnamnen används.</span><span class="sxs-lookup"><span data-stu-id="42cfe-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="42cfe-183">Ett exempel:</span><span class="sxs-lookup"><span data-stu-id="42cfe-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="42cfe-184">Ska ändras till:</span><span class="sxs-lookup"><span data-stu-id="42cfe-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="42cfe-185">För `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="42cfe-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="42cfe-186">Ska ändras till:</span><span class="sxs-lookup"><span data-stu-id="42cfe-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="42cfe-187">Migrera fullständigt kvalificerade cmdlet-anrop</span><span class="sxs-lookup"><span data-stu-id="42cfe-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="42cfe-188">Skript som använder modulkvalificerade cmdlet-anrop som:</span><span class="sxs-lookup"><span data-stu-id="42cfe-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="42cfe-189">Måste ändras så att de nya modul- och cmdlet-namnen används</span><span class="sxs-lookup"><span data-stu-id="42cfe-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="42cfe-190">Migrera modulmanifestberoenden</span><span class="sxs-lookup"><span data-stu-id="42cfe-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="42cfe-191">För moduler som uttrycker beroenden av AzureRM-moduler via en modulmanifestfil (.psd1) behöver modulnamnen uppdateras i avsnittet `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="42cfe-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="42cfe-192">Måste ändras till:</span><span class="sxs-lookup"><span data-stu-id="42cfe-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="42cfe-193">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="42cfe-193">Removed modules</span></span>

<span data-ttu-id="42cfe-194">Följande moduler har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="42cfe-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="42cfe-195">Verktygen för de här tjänsterna stöds inte längre aktivt.</span><span class="sxs-lookup"><span data-stu-id="42cfe-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="42cfe-196">Kunderna rekommenderas att övergå till alternativa tjänster så snart som möjligt.</span><span class="sxs-lookup"><span data-stu-id="42cfe-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="42cfe-197">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="42cfe-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="42cfe-198">Om Az ska användas med PowerShell 5.1 för Windows måste .NET Framework 4.7.2 vara installerat.</span><span class="sxs-lookup"><span data-stu-id="42cfe-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="42cfe-199">För PowerShell Core 6.x och senare krävs inte .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="42cfe-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="42cfe-200">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="42cfe-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="42cfe-201">På grund av ändringar i autentiseringsflödet för .NET Standard tar vi tillfälligt bort användarinloggning med PSCredential.</span><span class="sxs-lookup"><span data-stu-id="42cfe-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="42cfe-202">Funktionen återintroduceras i version 1/15/2019/ av Windows PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="42cfe-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="42cfe-203">Det här diskuteras mer ingående i [det här GitHub-ärendet.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="42cfe-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="42cfe-204">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="42cfe-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="42cfe-205">På grund av ändringar i autentiseringsflödet för .NET Standard använder vi enhetsinloggning som standardinloggningsflöde under interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="42cfe-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="42cfe-206">Webbläsarbaserad webbinloggning återintroduceras som standardfunktion i version 1/15/2019 av PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="42cfe-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="42cfe-207">Då kan användarna välja enhetsinloggning med hjälp av en växlingsparameter.</span><span class="sxs-lookup"><span data-stu-id="42cfe-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="42cfe-208">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="42cfe-208">Module breaking changes</span></span>

<span data-ttu-id="42cfe-209">I det här avsnittet beskriver vi icke-bakåtkompatibla ändringar för enskilda moduler och cmdletar.</span><span class="sxs-lookup"><span data-stu-id="42cfe-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="42cfe-210">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="42cfe-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="42cfe-211">Följande cmdletar togs bort:</span><span class="sxs-lookup"><span data-stu-id="42cfe-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="42cfe-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="42cfe-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="42cfe-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="42cfe-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="42cfe-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="42cfe-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="42cfe-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="42cfe-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="42cfe-216">Använd istället cmdleten **Set-AzApiManagement** för att ställa dessa egenskaper</span><span class="sxs-lookup"><span data-stu-id="42cfe-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="42cfe-217">Följande egenskaper togs bort:</span><span class="sxs-lookup"><span data-stu-id="42cfe-217">Removed the following properties:</span></span>
  - <span data-ttu-id="42cfe-218">Egenskapen `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` och `ScmHostnameConfiguration` av typen `PsApiManagementHostnameConfiguration` har tagits bort från `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="42cfe-219">Använd i stället `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` och `ScmCustomHostnameConfiguration` av typen `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="42cfe-220">Egenskapen `StaticIPs` har tagits bort från PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="42cfe-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="42cfe-221">Egenskapen har delats upp i `PublicIPAddresses` och `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="42cfe-222">Den nödvändiga egenskapen `Location` har tagits bort från cmdleten New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="42cfe-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="42cfe-223">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="42cfe-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="42cfe-224">Parametern `InvoiceName` har tagits bort från cmdleten `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="42cfe-225">Skripten behöver nu använda andra identitetsparametrar för fakturan.</span><span class="sxs-lookup"><span data-stu-id="42cfe-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="42cfe-226">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="42cfe-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="42cfe-227">Parameteruppsättningen `GetSkusWithAccountParamSetName` har tagits bort från cmdleten `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="42cfe-228">Du måste hämta SKU:er efter typ och plats i stället för att använda ResourceGroupName och Account Name.</span><span class="sxs-lookup"><span data-stu-id="42cfe-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="42cfe-229">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="42cfe-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="42cfe-230">`IdentityIds` tas bort från egenskapen `Identity` i objekten `PSVirtualMachine` och `PSVirtualMachineScaleSet` Skripten bör nu inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="42cfe-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="42cfe-231">Typ av `InstanceView`-egenskap för `PSVirtualMachineScaleSetVM`-objekt ändras från `VirtualMachineInstanceView` till `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="42cfe-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="42cfe-232">Egenskaperna `AutoOSUpgradePolicy` och `AutomaticOSUpgrade` tas bort från egenskapen `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="42cfe-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="42cfe-233">Typ av `Sku`-egenskap i `PSSnapshotUpdate`-objekt ändras från `DiskSku` till `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="42cfe-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="42cfe-234">`VmScaleSetVMParameterSet` tas bort från cmdleten `Add-AzVMDataDisk`, och du kan inte längre lägga till en datadisk individuellt till en virtuell ScaleSet-dator.</span><span class="sxs-lookup"><span data-stu-id="42cfe-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="42cfe-235">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="42cfe-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="42cfe-236">Parametern `GatewayName` har blivit obligatorisk i cmdleten `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="42cfe-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="42cfe-237">Cmdleten `New-AzDataFactoryGatewayKey` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="42cfe-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="42cfe-238">Parametern `LinkedServiceName` har tagits bort från cmdleten `Get-AzDataFactoryV2ActivityRun` Skripten ska inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="42cfe-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="42cfe-239">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="42cfe-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="42cfe-240">Följande inaktuella cmdletar har tagits bort: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` och `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="42cfe-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="42cfe-241">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="42cfe-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="42cfe-242">I följande cmdletar har parametern `Encoding` ändrats från typen `FileSystemCmdletProviderEncoding` till `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="42cfe-243">Den här ändringen tar bort kodningsvärdena `String` och `Oem`.</span><span class="sxs-lookup"><span data-stu-id="42cfe-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="42cfe-244">Övriga tidigare kodningsvärden kvarstår.</span><span class="sxs-lookup"><span data-stu-id="42cfe-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="42cfe-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="42cfe-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="42cfe-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="42cfe-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="42cfe-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="42cfe-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="42cfe-248">Det inaktuella egenskapsaliaset `Tags` har tagits bort från cmdletarna `New-AzDataLakeStoreAccount` och `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="42cfe-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="42cfe-249">Skript som använder</span><span class="sxs-lookup"><span data-stu-id="42cfe-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="42cfe-250">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="42cfe-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="42cfe-251">De inaktuella egenskaperna `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` har tagits bort från `PSDataLakeStoreAccountBasic`-objekt.</span><span class="sxs-lookup"><span data-stu-id="42cfe-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="42cfe-252">Alla skript som använder den `PSDatalakeStoreAccount` som returnerades från `Get-AzDataLakeStoreAccount` ska inte längre referera till dessa egenskaper.</span><span class="sxs-lookup"><span data-stu-id="42cfe-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="42cfe-253">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="42cfe-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="42cfe-254">Egenskapen `PurgeDisabled` har tagits bort från `PSKeyVaultKeyAttributes`-, `PSKeyVaultKeyIdentityItem`- och `PSKeyVaultSecretAttributes`-objekt Skript ska inte längre referera till egenskapen ```PurgeDisabled``` för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="42cfe-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="42cfe-255">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="42cfe-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="42cfe-256">Tog bort inaktuellt egenskapsalias `Tags` från skript för cmdleten `New-AzMediaService` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="42cfe-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="42cfe-257">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="42cfe-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="42cfe-258">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="42cfe-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="42cfe-259">Tog bort pluralnamnet `Categories` och parametern `Timegrains` och ersatte med singularparameternamn från cmdlet-skript för `Set-AzDiagnosticSetting` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="42cfe-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="42cfe-260">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="42cfe-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="42cfe-261">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="42cfe-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="42cfe-262">Tog bort den inaktuella parametern `ResourceId` från cmdleten `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="42cfe-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="42cfe-263">Tog bort den inaktuella egenskapen `EnableVmProtection` från objektet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="42cfe-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="42cfe-264">Tog bort den inaktuella cmdleten `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="42cfe-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="42cfe-265">Skript bör inte längre fatta bearbetningsbeslut baserat på värdena för dessa fält.</span><span class="sxs-lookup"><span data-stu-id="42cfe-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="42cfe-266">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="42cfe-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="42cfe-267">Standardparameteruppsättningen för `Get-AzOperationalInsightsDataSource` har tagits bort och `ByWorkspaceNameByKind` är nu standardparameteruppsättning</span><span class="sxs-lookup"><span data-stu-id="42cfe-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="42cfe-268">Skript som listar datakällor med hjälp av</span><span class="sxs-lookup"><span data-stu-id="42cfe-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="42cfe-269">ska ändras så att de anger en typ</span><span class="sxs-lookup"><span data-stu-id="42cfe-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="42cfe-270">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="42cfe-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="42cfe-271">Parametern `Encryption` har tagits bort från cmdleten `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="42cfe-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="42cfe-272">Parametern `TargetStorageAccountName` är nu obligatorisk för hanterade diskåterställningar i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="42cfe-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="42cfe-273">Tog bort parametrarna `StorageAccountName` och `StorageAccountResourceGroupName` i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="42cfe-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="42cfe-274">Tog bort parametern `Name` i cmdleten `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="42cfe-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="42cfe-275">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="42cfe-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="42cfe-276">Parametern `Sku` har tagits bort från cmdleten `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="42cfe-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="42cfe-277">Parametern `Password` har tagits bort från cmdleten `New-AzADServicePrincipal` och `New-AzADSpCredential` Lösenord genereras automatiskt och skript som tillhandahöll lösenordet:</span><span class="sxs-lookup"><span data-stu-id="42cfe-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="42cfe-278">Bör ändras så att de hämtar lösenordet från utdata:</span><span class="sxs-lookup"><span data-stu-id="42cfe-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="42cfe-279">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="42cfe-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="42cfe-280">Följande cmdlet-returtyper har ändrats:</span><span class="sxs-lookup"><span data-stu-id="42cfe-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="42cfe-281">Egenskapen `ServiceTypeHealthPolicies` av typen `ApplicationHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42cfe-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="42cfe-282">Egenskapen `ApplicationHealthPolicies` av typen `ClusterUpgradeDeltaHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42cfe-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="42cfe-283">Egenskapen `OverrideUserUpgradePolicy` av typen `ClusterUpgradePolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="42cfe-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="42cfe-284">Ändringarna påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="42cfe-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="42cfe-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="42cfe-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="42cfe-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="42cfe-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="42cfe-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="42cfe-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="42cfe-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="42cfe-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="42cfe-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="42cfe-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="42cfe-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="42cfe-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="42cfe-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="42cfe-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="42cfe-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="42cfe-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="42cfe-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="42cfe-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="42cfe-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="42cfe-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="42cfe-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="42cfe-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="42cfe-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="42cfe-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="42cfe-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="42cfe-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="42cfe-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="42cfe-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="42cfe-299">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="42cfe-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="42cfe-300">Tog bort parametrarna `State` och `ResourceId` från cmdleten `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="42cfe-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="42cfe-301">Följande inaktuella cmdletar har tagits bort: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="42cfe-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="42cfe-302">Tog bort den inaktuella parametern `Current` från cmdleten `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="42cfe-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="42cfe-303">Tog bort den inaktuella parametern `DatabaseName` från cmdleten `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="42cfe-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="42cfe-304">Tog bort den inaktuella parametern `PrivilegedLogin` från cmdleten `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="42cfe-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="42cfe-305">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="42cfe-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="42cfe-306">Standardparameteruppsättningen har ändrats till `OAuthParameterSet` för att det ska gå att skapa en Oauth-lagringskontext endast med namnet på lagringskontot</span><span class="sxs-lookup"><span data-stu-id="42cfe-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="42cfe-307">Exempel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="42cfe-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="42cfe-308">Parametern `Location` har blivit obligatorisk i cmdleten `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="42cfe-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="42cfe-309">Storage-API-metoderna använder nu TAP (uppgiftsbaserat asynkront mönster) i stället för synkrona API-anrop.</span><span class="sxs-lookup"><span data-stu-id="42cfe-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="42cfe-310">Följande exempel visar de nya asynkrona kommandona:</span><span class="sxs-lookup"><span data-stu-id="42cfe-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="42cfe-311">Blobögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="42cfe-311">Blob Snapshot</span></span>

<span data-ttu-id="42cfe-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="42cfe-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="42cfe-313">Az:</span><span class="sxs-lookup"><span data-stu-id="42cfe-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="42cfe-314">Dela ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="42cfe-314">Share Snapshot</span></span>

<span data-ttu-id="42cfe-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="42cfe-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="42cfe-316">Az:</span><span class="sxs-lookup"><span data-stu-id="42cfe-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="42cfe-317">Ångra borttagning av mjukborttagen blob</span><span class="sxs-lookup"><span data-stu-id="42cfe-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="42cfe-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="42cfe-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="42cfe-319">Az:</span><span class="sxs-lookup"><span data-stu-id="42cfe-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="42cfe-320">Ange blobnivå</span><span class="sxs-lookup"><span data-stu-id="42cfe-320">Set Blob Tier</span></span>

<span data-ttu-id="42cfe-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="42cfe-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="42cfe-322">Az:</span><span class="sxs-lookup"><span data-stu-id="42cfe-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="42cfe-323">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="42cfe-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="42cfe-324">Inaktuella egenskaper har tagits bort från `PSAppServicePlan`-, `PSCertificate`-, `PSCloningInfo`- och `PSSite`-objekten</span><span class="sxs-lookup"><span data-stu-id="42cfe-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
