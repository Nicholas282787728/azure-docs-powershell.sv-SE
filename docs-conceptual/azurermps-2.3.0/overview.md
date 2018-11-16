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
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575424"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="b3311-103">AzureRM-modul 2.3.0</span><span class="sxs-lookup"><span data-stu-id="b3311-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b3311-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="b3311-104">Requirements:</span></span>
<span data-ttu-id="b3311-105">Den lägsta versionen av Azure Stack som stöds är 1808.</span><span class="sxs-lookup"><span data-stu-id="b3311-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="b3311-106">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="b3311-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="b3311-107">Installera</span><span class="sxs-lookup"><span data-stu-id="b3311-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="b3311-108">Viktig information</span><span class="sxs-lookup"><span data-stu-id="b3311-108">Release Notes</span></span>
* <span data-ttu-id="b3311-109">Version 2.3.0 omfattar en lista över icke-bakåtkompatibla ändringar.</span><span class="sxs-lookup"><span data-stu-id="b3311-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="b3311-110">Om du vill uppgradera från version 1.2.11 har vi skapat en migreringsguide här: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="b3311-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="b3311-111">Den här versionen motsvarar den azurestack-specifika API-profilen 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="b3311-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="b3311-112">Alla moduler använder större eller lika stort beroende på modulen AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="b3311-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="b3311-113">API-versionen som stöds av alla moduler har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b3311-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="b3311-114">Compute – 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="b3311-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="b3311-115">Nätverk – 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="b3311-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="b3311-116">Storage – 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="b3311-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="b3311-117">Resurser – 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="b3311-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="b3311-118">KeyVault – 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="b3311-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="b3311-119">DNS – 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="b3311-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="b3311-120">Den fullständiga kartan över API-versioner för var och en av resurstyperna finns på https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="b3311-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="b3311-121">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="b3311-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="b3311-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="b3311-122">Azure Bridge</span></span>
<span data-ttu-id="b3311-123">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="b3311-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="b3311-124">Backup</span><span class="sxs-lookup"><span data-stu-id="b3311-124">Backup</span></span>
<span data-ttu-id="b3311-125">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="b3311-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="b3311-126">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="b3311-126">Configure where backups are stored</span></span>
- <span data-ttu-id="b3311-127">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="b3311-127">Perform backups</span></span>
- <span data-ttu-id="b3311-128">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="b3311-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="b3311-129">Commerce</span><span class="sxs-lookup"><span data-stu-id="b3311-129">Commerce</span></span>
<span data-ttu-id="b3311-130">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="b3311-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="b3311-131">Compute</span><span class="sxs-lookup"><span data-stu-id="b3311-131">Compute</span></span>
<span data-ttu-id="b3311-132">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder, hanterade diskar och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="b3311-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="b3311-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="b3311-133">Fabric</span></span>
<span data-ttu-id="b3311-134">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="b3311-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="b3311-135">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="b3311-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="b3311-136">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="b3311-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="b3311-137">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="b3311-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="b3311-138">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="b3311-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="b3311-139">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="b3311-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="b3311-140">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="b3311-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="b3311-141">Galleri</span><span class="sxs-lookup"><span data-stu-id="b3311-141">Gallery</span></span>
<span data-ttu-id="b3311-142">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="b3311-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="b3311-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="b3311-143">Infrastructure Insights</span></span>
<span data-ttu-id="b3311-144">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="b3311-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="b3311-145">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="b3311-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="b3311-146">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="b3311-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="b3311-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3311-147">KeyVault</span></span>
<span data-ttu-id="b3311-148">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="b3311-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="b3311-149">Nätverk</span><span class="sxs-lookup"><span data-stu-id="b3311-149">Network</span></span>
<span data-ttu-id="b3311-150">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="b3311-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="b3311-151">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="b3311-151">Management of network quotas</span></span>
- <span data-ttu-id="b3311-152">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="b3311-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="b3311-153">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="b3311-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="b3311-154">Storage</span><span class="sxs-lookup"><span data-stu-id="b3311-154">Storage</span></span>
<span data-ttu-id="b3311-155">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="b3311-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="b3311-156">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="b3311-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="b3311-157">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="b3311-157">Manage storage quotas</span></span>
- <span data-ttu-id="b3311-158">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="b3311-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="b3311-159">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="b3311-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="b3311-160">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="b3311-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="b3311-161">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="b3311-161">View information about the individual storage components</span></span>
- <span data-ttu-id="b3311-162">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="b3311-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="b3311-163">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="b3311-163">Subscription Admin</span></span>
<span data-ttu-id="b3311-164">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="b3311-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="b3311-165">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="b3311-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="b3311-166">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="b3311-166">Manage plans and offers</span></span>
- <span data-ttu-id="b3311-167">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="b3311-167">View usage and performance information</span></span>
- <span data-ttu-id="b3311-168">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="b3311-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="b3311-169">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="b3311-169">Subscription</span></span>
<span data-ttu-id="b3311-170">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="b3311-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="b3311-171">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="b3311-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="b3311-172">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="b3311-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="b3311-173">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="b3311-173">Update</span></span>
<span data-ttu-id="b3311-174">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="b3311-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="b3311-175">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="b3311-175">In this module administrators can:</span></span>
- <span data-ttu-id="b3311-176">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="b3311-176">List and install available updates</span></span>
- <span data-ttu-id="b3311-177">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="b3311-177">Resume interrupted updates</span></span>
- <span data-ttu-id="b3311-178">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="b3311-178">View installed updates</span></span>
