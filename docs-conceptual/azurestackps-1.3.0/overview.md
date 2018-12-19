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
ms.openlocfilehash: 3add10651334a9c8a1e4ebfd5c8b9cfbf0cc7981
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218025"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="8fd4a-103">Modulen Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="8fd4a-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd4a-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-104">Requirements:</span></span>
<span data-ttu-id="8fd4a-105">Lägsta version av Azure Stack som stöds är 1804.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="8fd4a-106">Obs! Om du använder en tidigare version så måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="8fd4a-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="8fd4a-107">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-107">Known issues:</span></span>

- <span data-ttu-id="8fd4a-108">Stäng avisering kräver Azure Stack version 1803</span><span class="sxs-lookup"><span data-stu-id="8fd4a-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="8fd4a-109">Vissa cmdletar för Storage kräver Azure Stack version 1804</span><span class="sxs-lookup"><span data-stu-id="8fd4a-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="8fd4a-110">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="8fd4a-111">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="8fd4a-112">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="8fd4a-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="8fd4a-113">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="8fd4a-113">Breaking Changes</span></span>
<span data-ttu-id="8fd4a-114">Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="8fd4a-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="8fd4a-115">Installera</span><span class="sxs-lookup"><span data-stu-id="8fd4a-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="8fd4a-116">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="8fd4a-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="8fd4a-117">Azure Bridge</span></span>
<span data-ttu-id="8fd4a-118">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="8fd4a-119">Backup</span><span class="sxs-lookup"><span data-stu-id="8fd4a-119">Backup</span></span>
<span data-ttu-id="8fd4a-120">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="8fd4a-121">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="8fd4a-121">Configure where backups are stored</span></span>
- <span data-ttu-id="8fd4a-122">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="8fd4a-122">Perform backups</span></span>
- <span data-ttu-id="8fd4a-123">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="8fd4a-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="8fd4a-124">Commerce</span><span class="sxs-lookup"><span data-stu-id="8fd4a-124">Commerce</span></span>
<span data-ttu-id="8fd4a-125">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="8fd4a-126">Compute</span><span class="sxs-lookup"><span data-stu-id="8fd4a-126">Compute</span></span>
<span data-ttu-id="8fd4a-127">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="8fd4a-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="8fd4a-128">Fabric</span></span>
<span data-ttu-id="8fd4a-129">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="8fd4a-130">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="8fd4a-131">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="8fd4a-132">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="8fd4a-133">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="8fd4a-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="8fd4a-134">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="8fd4a-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="8fd4a-135">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="8fd4a-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="8fd4a-136">Galleri</span><span class="sxs-lookup"><span data-stu-id="8fd4a-136">Gallery</span></span>
<span data-ttu-id="8fd4a-137">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="8fd4a-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="8fd4a-138">Infrastructure Insights</span></span>
<span data-ttu-id="8fd4a-139">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="8fd4a-140">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="8fd4a-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="8fd4a-141">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="8fd4a-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="8fd4a-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fd4a-142">KeyVault</span></span>
<span data-ttu-id="8fd4a-143">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="8fd4a-144">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8fd4a-144">Network</span></span>
<span data-ttu-id="8fd4a-145">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="8fd4a-146">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-146">Management of network quotas</span></span>
- <span data-ttu-id="8fd4a-147">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="8fd4a-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="8fd4a-148">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="8fd4a-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="8fd4a-149">Storage</span><span class="sxs-lookup"><span data-stu-id="8fd4a-149">Storage</span></span>
<span data-ttu-id="8fd4a-150">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="8fd4a-151">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="8fd4a-152">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-152">Manage storage quotas</span></span>
- <span data-ttu-id="8fd4a-153">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="8fd4a-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="8fd4a-154">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="8fd4a-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="8fd4a-155">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="8fd4a-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="8fd4a-156">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="8fd4a-156">View information about the individual storage components</span></span>
- <span data-ttu-id="8fd4a-157">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="8fd4a-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="8fd4a-158">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="8fd4a-158">Subscription Admin</span></span>
<span data-ttu-id="8fd4a-159">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="8fd4a-160">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="8fd4a-161">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="8fd4a-161">Manage plans and offers</span></span>
- <span data-ttu-id="8fd4a-162">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="8fd4a-162">View usage and performance information</span></span>
- <span data-ttu-id="8fd4a-163">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="8fd4a-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="8fd4a-164">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="8fd4a-164">Subscription</span></span>
<span data-ttu-id="8fd4a-165">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="8fd4a-166">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="8fd4a-167">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="8fd4a-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="8fd4a-168">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="8fd4a-168">Update</span></span>
<span data-ttu-id="8fd4a-169">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="8fd4a-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="8fd4a-170">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="8fd4a-170">In this module administrators can:</span></span>
- <span data-ttu-id="8fd4a-171">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="8fd4a-171">List and install available updates</span></span>
- <span data-ttu-id="8fd4a-172">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="8fd4a-172">Resume interrupted updates</span></span>
- <span data-ttu-id="8fd4a-173">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="8fd4a-173">View installed updates</span></span>
