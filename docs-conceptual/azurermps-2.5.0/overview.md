---
title: Översikt över Azure Stack PowerShell | Microsoft Docs
description: En översikt över Azure Stack PowerShell med anvisningar för installation och konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67038201"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="00a4d-103">AzureRM-modul 2.5.0</span><span class="sxs-lookup"><span data-stu-id="00a4d-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="00a4d-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="00a4d-104">Requirements:</span></span>
<span data-ttu-id="00a4d-105">Den lägsta versionen av Azure Stack som stöds är 1904.</span><span class="sxs-lookup"><span data-stu-id="00a4d-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="00a4d-106">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="00a4d-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="00a4d-107">Installera</span><span class="sxs-lookup"><span data-stu-id="00a4d-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="00a4d-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="00a4d-108">Release Notes</span></span>
* <span data-ttu-id="00a4d-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="00a4d-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="00a4d-110">Den nya Resources-modulen har stöd för API-versionen 2018-05-01 med profilen 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="00a4d-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="00a4d-111">Åtgärderna PolicyDefinition(2016-12-01) och PolicyAssisgment (2017-06-01-preview) använder fortfarande äldre API-versioner</span><span class="sxs-lookup"><span data-stu-id="00a4d-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="00a4d-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="00a4d-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="00a4d-113">Ny beräkningsmodul med stöd för API-versionen 2017-12-01.</span><span class="sxs-lookup"><span data-stu-id="00a4d-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="00a4d-114">Den här versionen motsvarar API-profilen 2019-03-01-hybrid som är specifik för Azure Stack</span><span class="sxs-lookup"><span data-stu-id="00a4d-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="00a4d-115">Alla moduler använder större eller lika stort beroende på modulen AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="00a4d-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="00a4d-116">API-versionen som stöds av alla moduler har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="00a4d-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="00a4d-117">Compute – 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="00a4d-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="00a4d-118">Nätverk – 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="00a4d-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="00a4d-119">Storage – 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="00a4d-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="00a4d-120">Resurser – 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="00a4d-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="00a4d-121">KeyVault – 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="00a4d-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="00a4d-122">DNS – 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="00a4d-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="00a4d-123">Den fullständiga kartan över API-versioner för var och en av resurstyperna finns på https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="00a4d-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="00a4d-124">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="00a4d-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="00a4d-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="00a4d-125">Azure Bridge</span></span>
<span data-ttu-id="00a4d-126">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="00a4d-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="00a4d-127">Säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="00a4d-127">Backup</span></span>
<span data-ttu-id="00a4d-128">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="00a4d-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="00a4d-129">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="00a4d-129">Configure where backups are stored</span></span>
- <span data-ttu-id="00a4d-130">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="00a4d-130">Perform backups</span></span>
- <span data-ttu-id="00a4d-131">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="00a4d-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="00a4d-132">Commerce</span><span class="sxs-lookup"><span data-stu-id="00a4d-132">Commerce</span></span>
<span data-ttu-id="00a4d-133">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="00a4d-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="00a4d-134">Compute</span><span class="sxs-lookup"><span data-stu-id="00a4d-134">Compute</span></span>
<span data-ttu-id="00a4d-135">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder, hanterade diskar och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="00a4d-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="00a4d-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="00a4d-136">Fabric</span></span>
<span data-ttu-id="00a4d-137">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="00a4d-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="00a4d-138">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="00a4d-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="00a4d-139">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="00a4d-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="00a4d-140">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="00a4d-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="00a4d-141">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="00a4d-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="00a4d-142">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="00a4d-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="00a4d-143">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="00a4d-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="00a4d-144">Galleri</span><span class="sxs-lookup"><span data-stu-id="00a4d-144">Gallery</span></span>
<span data-ttu-id="00a4d-145">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="00a4d-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="00a4d-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="00a4d-146">Infrastructure Insights</span></span>
<span data-ttu-id="00a4d-147">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="00a4d-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="00a4d-148">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="00a4d-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="00a4d-149">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="00a4d-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="00a4d-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="00a4d-150">KeyVault</span></span>
<span data-ttu-id="00a4d-151">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="00a4d-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="00a4d-152">Nätverk</span><span class="sxs-lookup"><span data-stu-id="00a4d-152">Network</span></span>
<span data-ttu-id="00a4d-153">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="00a4d-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="00a4d-154">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="00a4d-154">Management of network quotas</span></span>
- <span data-ttu-id="00a4d-155">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="00a4d-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="00a4d-156">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="00a4d-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="00a4d-157">Storage</span><span class="sxs-lookup"><span data-stu-id="00a4d-157">Storage</span></span>
<span data-ttu-id="00a4d-158">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="00a4d-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="00a4d-159">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="00a4d-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="00a4d-160">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="00a4d-160">Manage storage quotas</span></span>
- <span data-ttu-id="00a4d-161">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="00a4d-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="00a4d-162">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="00a4d-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="00a4d-163">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="00a4d-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="00a4d-164">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="00a4d-164">View information about the individual storage components</span></span>
- <span data-ttu-id="00a4d-165">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="00a4d-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="00a4d-166">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="00a4d-166">Subscription Admin</span></span>
<span data-ttu-id="00a4d-167">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="00a4d-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="00a4d-168">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="00a4d-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="00a4d-169">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="00a4d-169">Manage plans and offers</span></span>
- <span data-ttu-id="00a4d-170">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="00a4d-170">View usage and performance information</span></span>
- <span data-ttu-id="00a4d-171">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="00a4d-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="00a4d-172">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="00a4d-172">Subscription</span></span>
<span data-ttu-id="00a4d-173">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="00a4d-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="00a4d-174">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="00a4d-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="00a4d-175">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="00a4d-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="00a4d-176">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="00a4d-176">Update</span></span>
<span data-ttu-id="00a4d-177">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="00a4d-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="00a4d-178">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="00a4d-178">In this module administrators can:</span></span>
- <span data-ttu-id="00a4d-179">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="00a4d-179">List and install available updates</span></span>
- <span data-ttu-id="00a4d-180">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="00a4d-180">Resume interrupted updates</span></span>
- <span data-ttu-id="00a4d-181">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="00a4d-181">View installed updates</span></span>
