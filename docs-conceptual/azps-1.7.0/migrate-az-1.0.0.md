---
title: Icke-bakåtkompatibla ändringar för Microsoft Azure PowerShell Az 1.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 1 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/18/2019
ms.locfileid: "59364248"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="7732a-103">Migreringsguide för Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7732a-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="7732a-104">I det här dokumentet beskrivs ändringarna mellan 6.x-versionerna av AzureRM och Az version 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="7732a-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="7732a-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="7732a-105">Table of Contents</span></span>
- [<span data-ttu-id="7732a-106">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7732a-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="7732a-107">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="7732a-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="7732a-108">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="7732a-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="7732a-109">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="7732a-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="7732a-110">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="7732a-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="7732a-111">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="7732a-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="7732a-112">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="7732a-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="7732a-113">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7732a-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="7732a-114">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="7732a-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="7732a-115">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="7732a-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="7732a-116">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="7732a-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="7732a-117">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="7732a-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="7732a-118">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="7732a-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="7732a-119">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="7732a-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="7732a-120">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="7732a-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="7732a-121">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="7732a-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="7732a-122">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="7732a-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="7732a-123">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="7732a-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="7732a-124">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="7732a-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="7732a-125">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="7732a-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="7732a-126">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="7732a-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="7732a-127">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="7732a-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="7732a-128">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="7732a-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="7732a-129">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="7732a-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="7732a-130">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="7732a-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="7732a-131">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="7732a-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="7732a-132">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7732a-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="7732a-133">Ändringar av substantivprefix i cmdlet</span><span class="sxs-lookup"><span data-stu-id="7732a-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="7732a-134">I AzureRM använder cmdletarna antingen ”AzureRM” eller ”Azure” som substantivprefix.</span><span class="sxs-lookup"><span data-stu-id="7732a-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="7732a-135">Az förenklar och normaliserar cmndlet-namn så att ”Az” används som cmdlet-substantivprefix för alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7732a-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="7732a-136">Exempel:</span><span class="sxs-lookup"><span data-stu-id="7732a-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="7732a-137">Har ändrats till</span><span class="sxs-lookup"><span data-stu-id="7732a-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="7732a-138">För att göra övergången till de nya cmdlet-namnen enklare introduceras två nya cmdletar i Az, ```Enable-AzureRmAlias``` och ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="7732a-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="7732a-139">```Enable-AzureRmAlias``` skapar alias från de äldre cmdlet-namnen i AzureRM till de nyare cmdlet-namnen i Az.</span><span class="sxs-lookup"><span data-stu-id="7732a-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="7732a-140">Cmdleten tillåter att alias skapas i den aktuella sessionen eller i samtliga sessioner genom att användar- eller datorprofilen ändras.</span><span class="sxs-lookup"><span data-stu-id="7732a-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="7732a-141">Till exempel kan följande skript i AzureRM:</span><span class="sxs-lookup"><span data-stu-id="7732a-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="7732a-142">köras med minimala ändringar med ```Enable-AzureRmAlias```:</span><span class="sxs-lookup"><span data-stu-id="7732a-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="7732a-143">När ```Enable-AzureRmAlias -Scope CurrentUser``` körs kan alias aktiveras för alla powershell-sessioner som du öppnar, så när denna cmdlet har körts behöver ett skript som detta inte ändras alls:</span><span class="sxs-lookup"><span data-stu-id="7732a-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="7732a-144">Om du vill ha information om användning av alias-cmdletarna kör du ```Get-Help -Online Enable-AzureRmAlias``` från powershell-prompten.</span><span class="sxs-lookup"><span data-stu-id="7732a-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="7732a-145">```Disable-AzureRmAlias``` tar bort de alias för AzureRM-cmdlet som skapats av ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="7732a-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="7732a-146">Om du vill ha mer information kör du ```Get-Help -Online Disable-AzureRmAlias``` från powershell-prompten.</span><span class="sxs-lookup"><span data-stu-id="7732a-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="7732a-147">Ändringar av modulnamn</span><span class="sxs-lookup"><span data-stu-id="7732a-147">Module Name Changes</span></span>
- <span data-ttu-id="7732a-148">Modulnamnen har ändrats från `AzureRM.*` till `Az.*`, förutom följande moduler:</span><span class="sxs-lookup"><span data-stu-id="7732a-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="7732a-149">Ändringarna i modulnamnen innebär att alla skript som använder ```#Requires``` eller ```Import-Module``` för att läsa in specifika moduler måste ändras så att de använder den nya modulen i stället.</span><span class="sxs-lookup"><span data-stu-id="7732a-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="7732a-150">Migrera #Requires-instruktioner</span><span class="sxs-lookup"><span data-stu-id="7732a-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="7732a-151">Skript som använder #Requires för att deklarera beroende av AzureRM-moduler måste uppdateras så att de nya modulnamnen används</span><span class="sxs-lookup"><span data-stu-id="7732a-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="7732a-152">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="7732a-153">Migrera Import-Module-instruktioner</span><span class="sxs-lookup"><span data-stu-id="7732a-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="7732a-154">Skript som använder ```Import-Module``` för att läsa in AzureRM-moduler måste uppdateras med de nya modulnamnen.</span><span class="sxs-lookup"><span data-stu-id="7732a-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="7732a-155">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="7732a-156">Migrera fullständigt kvalificerade cmdlet-anrop</span><span class="sxs-lookup"><span data-stu-id="7732a-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="7732a-157">Skript som använder modulkvalificerade cmdlet-anrop som</span><span class="sxs-lookup"><span data-stu-id="7732a-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="7732a-158">Ska ändras så att de nya modul- och cmdlet-namnen används</span><span class="sxs-lookup"><span data-stu-id="7732a-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="7732a-159">Migrera modulmanifestberoenden</span><span class="sxs-lookup"><span data-stu-id="7732a-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="7732a-160">För moduler som uttrycker beroenden av AzureRM-moduler via en modulmanifestfil (.psd1) behöver modulnamnen uppdateras i avsnittet ”RequiredModules”</span><span class="sxs-lookup"><span data-stu-id="7732a-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="7732a-161">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="7732a-162">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="7732a-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="7732a-163">Verktyg för de här tjänsterna stöds inte längre aktivt.</span><span class="sxs-lookup"><span data-stu-id="7732a-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="7732a-164">Kunderna rekommenderas att övergå till alternativa tjänster så snart som möjligt.</span><span class="sxs-lookup"><span data-stu-id="7732a-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="7732a-165">Windows PowerShell 5.1 och .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="7732a-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="7732a-166">Om Az ska användas med Windows PowerShell 5.1 måste .NET 4.7.2 installeras.</span><span class="sxs-lookup"><span data-stu-id="7732a-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="7732a-167">Om Az ska användas med PowerShell Core behövs inte .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="7732a-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="7732a-168">Tillfällig borttagning av användarinloggning med PSCredential</span><span class="sxs-lookup"><span data-stu-id="7732a-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="7732a-169">På grund av ändringar i autentiseringsflödet för .NET Standard tar vi tillfälligt bort användarinloggning med PSCredential.</span><span class="sxs-lookup"><span data-stu-id="7732a-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="7732a-170">Funktionen kommer att återintroduceras i version 1/15/2019/ av Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7732a-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="7732a-171">Detta diskuteras mer ingående i [detta ärende.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="7732a-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="7732a-172">Inloggning med standardenhetskod i stället för med webbläsarfråga</span><span class="sxs-lookup"><span data-stu-id="7732a-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="7732a-173">På grund av ändringar i autentiseringsflödet för .NET Standard använder vi enhetsinloggning som standardinloggningsflöde under interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="7732a-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="7732a-174">Webbläsarbaserad webbinloggning kommer att återintroduceras som standard i version 1/15/2019 av Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7732a-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="7732a-175">Då kan användarna välja enhetsinloggning med hjälp av en växlingsparameter.</span><span class="sxs-lookup"><span data-stu-id="7732a-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="7732a-176">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="7732a-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="7732a-177">Az.ApiManagement (tidigare AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="7732a-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="7732a-178">Följande cmdletar tas bort:</span><span class="sxs-lookup"><span data-stu-id="7732a-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="7732a-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7732a-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="7732a-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="7732a-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="7732a-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="7732a-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="7732a-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="7732a-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="7732a-183">Använd cmdleten **Set-AzApiManagement** för att ställa in dessa egenskaper istället</span><span class="sxs-lookup"><span data-stu-id="7732a-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="7732a-184">Följande egenskaper har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7732a-184">Following properties were removed</span></span>
  - <span data-ttu-id="7732a-185">Egenskapen `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` och `ScmHostnameConfiguration` av typen `PsApiManagementHostnameConfiguration` har tagits bort från `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="7732a-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="7732a-186">Använd i stället `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` och `ScmCustomHostnameConfiguration` av typen `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7732a-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="7732a-187">Egenskapen `StaticIPs` har tagits bort från PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7732a-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="7732a-188">Egenskapen har delats upp i `PublicIPAddresses` och `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="7732a-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="7732a-189">Den nödvändiga egenskapen `Location` har tagits bort från cmdleten New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="7732a-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="7732a-190">Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="7732a-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="7732a-191">Parametern `InvoiceName` har tagits bort från cmdleten `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="7732a-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="7732a-192">Skripten behöver nu använda andra identitetsparametrar för fakturan.</span><span class="sxs-lookup"><span data-stu-id="7732a-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="7732a-193">Az.CognitiveServices (tidigare AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="7732a-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="7732a-194">Parameteruppsättningen `GetSkusWithAccountParamSetName` har tagits bort från cmdleten `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="7732a-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="7732a-195">Du måste hämta SKU:er efter typ och plats i stället för att använda ResourceGroupName och Account Name.</span><span class="sxs-lookup"><span data-stu-id="7732a-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="7732a-196">Az.Compute (tidigare AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="7732a-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="7732a-197">`IdentityIds` tas bort från egenskapen `Identity` i objekten `PSVirtualMachine` och `PSVirtualMachineScaleSet` Skripten bör nu inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="7732a-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="7732a-198">Typ av `InstanceView`-egenskap för `PSVirtualMachineScaleSetVM`-objekt ändras från `VirtualMachineInstanceView` till `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="7732a-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="7732a-199">Egenskaperna `AutoOSUpgradePolicy` och `AutomaticOSUpgrade` tas bort från egenskapen `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="7732a-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="7732a-200">Typ av `Sku`-egenskap i `PSSnapshotUpdate`-objekt ändras från `DiskSku` till `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="7732a-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="7732a-201">`VmScaleSetVMParameterSet` tas bort från cmdleten `Add-AzVMDataDisk`, och du kan inte längre lägga till en datadisk individuellt till en virtuell ScaleSet-dator.</span><span class="sxs-lookup"><span data-stu-id="7732a-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="7732a-202">Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="7732a-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="7732a-203">Parametern `GatewayName` har blivit obligatorisk i cmdleten `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="7732a-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="7732a-204">Cmdleten `New-AzDataFactoryGatewayKey` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7732a-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="7732a-205">Parametern `LinkedServiceName` har tagits bort från cmdleten `Get-AzDataFactoryV2ActivityRun` Skripten ska inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="7732a-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="7732a-206">Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="7732a-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="7732a-207">Följande inaktuella cmdletar har tagits bort: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` och `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="7732a-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="7732a-208">Az.DataLakeStore (tidigare AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="7732a-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="7732a-209">I följande cmdletar har parametern `Encoding` ändrats från typen `FileSystemCmdletProviderEncoding` till `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="7732a-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="7732a-210">Den här ändringen tar bort kodningsvärdena `String` och `Oem`.</span><span class="sxs-lookup"><span data-stu-id="7732a-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="7732a-211">Övriga tidigare kodningsvärden kvarstår.</span><span class="sxs-lookup"><span data-stu-id="7732a-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="7732a-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7732a-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="7732a-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="7732a-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="7732a-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="7732a-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="7732a-215">Det inaktuella egenskapsaliaset `Tags` har tagits bort från cmdletarna `New-AzDataLakeStoreAccount` och `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="7732a-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="7732a-216">Skript som använder</span><span class="sxs-lookup"><span data-stu-id="7732a-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="7732a-217">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="7732a-218">De inaktuella egenskaperna ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` har tagits bort från ```PSDataLakeStoreAccountBasic```-objekt.</span><span class="sxs-lookup"><span data-stu-id="7732a-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="7732a-219">Alla skript som använder den ```PSDatalakeStoreAccount``` som returnerades från ```Get-AzDataLakeStoreAccount``` ska inte längre referera till dessa egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7732a-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="7732a-220">Az.KeyVault (tidigare AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="7732a-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="7732a-221">Egenskapen `PurgeDisabled` har tagits bort från `PSKeyVaultKeyAttributes`-, `PSKeyVaultKeyIdentityItem`- och `PSKeyVaultSecretAttributes`-objekt Skripten ska inte längre referera till egenskapen ```PurgeDisabled``` för att fatta bearbetningsbeslut.</span><span class="sxs-lookup"><span data-stu-id="7732a-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="7732a-222">Az.Media (tidigare AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="7732a-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="7732a-223">Tog bort inaktuellt egenskapsalias `Tags` från skript för cmdleten `New-AzMediaService` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="7732a-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="7732a-224">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="7732a-225">Az.Monitor (tidigare AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="7732a-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="7732a-226">Tog bort pluralnamnet `Categories` och parametern `Timegrains` och ersatte med singularparameternamn från cmdlet-skript för `Set-AzDiagnosticSetting` med hjälp av</span><span class="sxs-lookup"><span data-stu-id="7732a-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="7732a-227">Ska ändras till</span><span class="sxs-lookup"><span data-stu-id="7732a-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="7732a-228">Az.Network (tidigare AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="7732a-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="7732a-229">Tog bort den inaktuella parametern `ResourceId` från cmdleten `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="7732a-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="7732a-230">Tog bort den inaktuella egenskapen `EnableVmProtection` från objektet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="7732a-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="7732a-231">Tog bort den inaktuella cmdleten `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="7732a-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="7732a-232">Skript bör inte längre fatta bearbetningsbeslut baserat på värdena för dessa fält.</span><span class="sxs-lookup"><span data-stu-id="7732a-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="7732a-233">Az.OperationalInsights (tidigare AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="7732a-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="7732a-234">Standardparameteruppsättningen för `Get-AzOperationalInsightsDataSource` har tagits bort och `ByWorkspaceNameByKind` är nu standardparameteruppsättning</span><span class="sxs-lookup"><span data-stu-id="7732a-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="7732a-235">Skript som listar datakällor med hjälp av</span><span class="sxs-lookup"><span data-stu-id="7732a-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="7732a-236">ska ändras så att de anger en typ</span><span class="sxs-lookup"><span data-stu-id="7732a-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="7732a-237">Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="7732a-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="7732a-238">Parametern `Encryption` har tagits bort från cmdleten `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="7732a-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="7732a-239">Parametern `TargetStorageAccountName` är nu obligatorisk för hanterade diskåterställningar i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="7732a-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="7732a-240">Tog bort parametrarna `StorageAccountName` och `StorageAccountResourceGroupName` i cmdleten `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="7732a-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="7732a-241">Tog bort parametern `Name` i cmdleten `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="7732a-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="7732a-242">Az.Resources (tidigare AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="7732a-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="7732a-243">Parametern `Sku` har tagits bort från cmdleten `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="7732a-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="7732a-244">Parametern `Password` har tagits bort från cmdleten `New-AzADServicePrincipal` och `New-AzADSpCredential` Lösenord genereras automatiskt och skript som tillhandahöll lösenordet:</span><span class="sxs-lookup"><span data-stu-id="7732a-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="7732a-245">bör ändras så att de hämtar lösenordet från utdata:</span><span class="sxs-lookup"><span data-stu-id="7732a-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="7732a-246">Az.ServiceFabric (tidigare AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="7732a-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="7732a-247">Följande cmdlet-returtyper har ändrats:</span><span class="sxs-lookup"><span data-stu-id="7732a-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="7732a-248">Egenskapen `SerivceTypeHealthPolicies` av typen `ApplicationHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7732a-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="7732a-249">Egenskapen `ApplicationHealthPolicies` av typen `ClusterUpgradeDeltaHealthPolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7732a-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="7732a-250">Egenskapen `OverrideUserUpgradePolicy` av typen `ClusterUpgradePolicy` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7732a-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="7732a-251">Ändringarna påverkar följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="7732a-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="7732a-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7732a-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="7732a-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7732a-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="7732a-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7732a-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="7732a-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="7732a-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="7732a-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7732a-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="7732a-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7732a-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="7732a-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7732a-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="7732a-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7732a-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="7732a-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="7732a-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="7732a-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="7732a-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="7732a-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="7732a-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="7732a-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="7732a-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="7732a-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="7732a-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="7732a-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="7732a-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="7732a-266">Az.Sql (tidigare AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="7732a-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="7732a-267">Tog bort parametrarna `State` och `ResourceId` från cmdleten `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="7732a-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="7732a-268">Följande inaktuella cmdletar har tagits bort: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="7732a-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="7732a-269">Tog bort den inaktuella parametern `Current` från cmdleten `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="7732a-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="7732a-270">Tog bort den inaktuella parametern `DatabaseName` från cmdleten `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="7732a-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="7732a-271">Tog bort den inaktuella parametern `PrivilegedLogin` från cmdleten `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="7732a-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="7732a-272">Az.Storage (tidigare Azure.Storage och AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="7732a-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="7732a-273">Standardparameteruppsättningen har ändrats till `OAuthParameterSet` för att det ska gå att skapa en Oauth-lagringskontext endast med namnet på lagringskontot</span><span class="sxs-lookup"><span data-stu-id="7732a-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="7732a-274">Exempel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="7732a-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="7732a-275">Parametern `Location` har blivit obligatorisk i cmdleten `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="7732a-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="7732a-276">Storage-API-metoderna använder nu TAP (uppgiftsbaserat asynkront mönster) i stället för synkrona API-anrop.</span><span class="sxs-lookup"><span data-stu-id="7732a-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="7732a-277">1. Blobögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="7732a-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="7732a-278">Innan:</span><span class="sxs-lookup"><span data-stu-id="7732a-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="7732a-279">Efter:</span><span class="sxs-lookup"><span data-stu-id="7732a-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="7732a-280">2. Dela ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="7732a-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="7732a-281">Innan:</span><span class="sxs-lookup"><span data-stu-id="7732a-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="7732a-282">Efter:</span><span class="sxs-lookup"><span data-stu-id="7732a-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="7732a-283">3. Ångra borttagning av en blob med mjuk borttagning</span><span class="sxs-lookup"><span data-stu-id="7732a-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="7732a-284">Innan:</span><span class="sxs-lookup"><span data-stu-id="7732a-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="7732a-285">Efter:</span><span class="sxs-lookup"><span data-stu-id="7732a-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="7732a-286">4. Ange blobnivå</span><span class="sxs-lookup"><span data-stu-id="7732a-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="7732a-287">Innan:</span><span class="sxs-lookup"><span data-stu-id="7732a-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="7732a-288">Efter:</span><span class="sxs-lookup"><span data-stu-id="7732a-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="7732a-289">Az.Websites (tidigare AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="7732a-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="7732a-290">Inaktuella egenskaper har tagits bort från `PSAppServicePlan`-, `PSCertificate`-, `PSCloningInfo`- och `PSSite`-objekten</span><span class="sxs-lookup"><span data-stu-id="7732a-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>