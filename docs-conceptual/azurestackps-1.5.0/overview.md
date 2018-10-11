---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882647"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="728fe-103">Modulen Azure Stack 1.5.0</span><span class="sxs-lookup"><span data-stu-id="728fe-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="728fe-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="728fe-104">Requirements:</span></span>
<span data-ttu-id="728fe-105">Den lägsta versionen av Azure Stack som stöds är 1808.</span><span class="sxs-lookup"><span data-stu-id="728fe-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="728fe-106">Obs! Om du använder en tidigare version så måste du installera version 1.4.0</span><span class="sxs-lookup"><span data-stu-id="728fe-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="728fe-107">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="728fe-107">Known issues:</span></span>

- <span data-ttu-id="728fe-108">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="728fe-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="728fe-109">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="728fe-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="728fe-110">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="728fe-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="728fe-111">Installera</span><span class="sxs-lookup"><span data-stu-id="728fe-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a><span data-ttu-id="728fe-112">Viktig information</span><span class="sxs-lookup"><span data-stu-id="728fe-112">Release Notes</span></span>
* <span data-ttu-id="728fe-113">Alla administratörsmoduler i Azure Stack har uppdaterats för större eller lika stort beroende på modulen AzureRm.Profile</span><span class="sxs-lookup"><span data-stu-id="728fe-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="728fe-114">Stöd för hantering av kapslade resursnamn i alla moduler</span><span class="sxs-lookup"><span data-stu-id="728fe-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="728fe-115">Ett fel i alla moduler där ErrorActionPreference har åsidosattes för att bli Stop har korrigerats</span><span class="sxs-lookup"><span data-stu-id="728fe-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="728fe-116">Administratörsmodul för Azs.Compute</span><span class="sxs-lookup"><span data-stu-id="728fe-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="728fe-117">Nya kvotegenskaper har lagts till för att stödja hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="728fe-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="728fe-118">Cmdletar som rör diskmigrering har lagts till</span><span class="sxs-lookup"><span data-stu-id="728fe-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="728fe-119">Ytterligare egenskaper i objekt för plattformsavbildningen och VM-tilläggen</span><span class="sxs-lookup"><span data-stu-id="728fe-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="728fe-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="728fe-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="728fe-121">Ny cmdlet för att lägga till nod för skalningsenhet</span><span class="sxs-lookup"><span data-stu-id="728fe-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="728fe-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="728fe-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="728fe-123">Set-AzsBackupShare är nu ett alias till cmdleten Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="728fe-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="728fe-124">Get-AzsBackupLocation är nu ett alias till cmdleten Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="728fe-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="728fe-125">Set-AzsBackupConfiguration, parametern BackupShare är nu ett alias för parametersökvägen</span><span class="sxs-lookup"><span data-stu-id="728fe-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="728fe-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="728fe-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="728fe-127">Get-AzsDelegatedProviderOffer, parametern OfferName är nu ett alias för Offer</span><span class="sxs-lookup"><span data-stu-id="728fe-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="728fe-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="728fe-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="728fe-129">Get-AzsDelegatedProviderOffer, parametern OfferName är nu ett alias för Offer</span><span class="sxs-lookup"><span data-stu-id="728fe-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="728fe-130">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="728fe-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="728fe-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="728fe-131">Azure Bridge</span></span>
<span data-ttu-id="728fe-132">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="728fe-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="728fe-133">Backup</span><span class="sxs-lookup"><span data-stu-id="728fe-133">Backup</span></span>
<span data-ttu-id="728fe-134">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="728fe-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="728fe-135">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="728fe-135">Configure where backups are stored</span></span>
- <span data-ttu-id="728fe-136">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="728fe-136">Perform backups</span></span>
- <span data-ttu-id="728fe-137">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="728fe-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="728fe-138">Commerce</span><span class="sxs-lookup"><span data-stu-id="728fe-138">Commerce</span></span>
<span data-ttu-id="728fe-139">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="728fe-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="728fe-140">Compute</span><span class="sxs-lookup"><span data-stu-id="728fe-140">Compute</span></span>
<span data-ttu-id="728fe-141">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder, hanterade diskar och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="728fe-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="728fe-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="728fe-142">Fabric</span></span>
<span data-ttu-id="728fe-143">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="728fe-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="728fe-144">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="728fe-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="728fe-145">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="728fe-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="728fe-146">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="728fe-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="728fe-147">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="728fe-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="728fe-148">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="728fe-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="728fe-149">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="728fe-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="728fe-150">Galleri</span><span class="sxs-lookup"><span data-stu-id="728fe-150">Gallery</span></span>
<span data-ttu-id="728fe-151">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="728fe-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="728fe-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="728fe-152">Infrastructure Insights</span></span>
<span data-ttu-id="728fe-153">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="728fe-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="728fe-154">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="728fe-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="728fe-155">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="728fe-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="728fe-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="728fe-156">KeyVault</span></span>
<span data-ttu-id="728fe-157">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="728fe-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="728fe-158">Nätverk</span><span class="sxs-lookup"><span data-stu-id="728fe-158">Network</span></span>
<span data-ttu-id="728fe-159">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="728fe-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="728fe-160">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="728fe-160">Management of network quotas</span></span>
- <span data-ttu-id="728fe-161">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="728fe-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="728fe-162">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="728fe-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="728fe-163">Storage</span><span class="sxs-lookup"><span data-stu-id="728fe-163">Storage</span></span>
<span data-ttu-id="728fe-164">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="728fe-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="728fe-165">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="728fe-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="728fe-166">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="728fe-166">Manage storage quotas</span></span>
- <span data-ttu-id="728fe-167">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="728fe-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="728fe-168">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="728fe-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="728fe-169">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="728fe-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="728fe-170">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="728fe-170">View information about the individual storage components</span></span>
- <span data-ttu-id="728fe-171">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="728fe-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="728fe-172">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="728fe-172">Subscription Admin</span></span>
<span data-ttu-id="728fe-173">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="728fe-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="728fe-174">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="728fe-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="728fe-175">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="728fe-175">Manage plans and offers</span></span>
- <span data-ttu-id="728fe-176">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="728fe-176">View usage and performance information</span></span>
- <span data-ttu-id="728fe-177">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="728fe-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="728fe-178">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="728fe-178">Subscription</span></span>
<span data-ttu-id="728fe-179">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="728fe-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="728fe-180">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="728fe-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="728fe-181">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="728fe-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="728fe-182">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="728fe-182">Update</span></span>
<span data-ttu-id="728fe-183">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="728fe-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="728fe-184">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="728fe-184">In this module administrators can:</span></span>
- <span data-ttu-id="728fe-185">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="728fe-185">List and install available updates</span></span>
- <span data-ttu-id="728fe-186">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="728fe-186">Resume interrupted updates</span></span>
- <span data-ttu-id="728fe-187">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="728fe-187">View installed updates</span></span>
