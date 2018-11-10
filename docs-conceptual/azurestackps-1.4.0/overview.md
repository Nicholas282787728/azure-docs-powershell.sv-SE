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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211850"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="e9e31-103">Modulen Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="e9e31-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e31-104">Krav:</span><span class="sxs-lookup"><span data-stu-id="e9e31-104">Requirements:</span></span>
<span data-ttu-id="e9e31-105">Lägsta version av Azure Stack som stöds är 1804.</span><span class="sxs-lookup"><span data-stu-id="e9e31-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="e9e31-106">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="e9e31-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="e9e31-107">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="e9e31-107">Known issues:</span></span>

- <span data-ttu-id="e9e31-108">Stäng avisering kräver Azure Stack version 1803</span><span class="sxs-lookup"><span data-stu-id="e9e31-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="e9e31-109">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="e9e31-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="e9e31-110">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="e9e31-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="e9e31-111">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="e9e31-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="e9e31-112">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="e9e31-112">Breaking Changes</span></span>
<span data-ttu-id="e9e31-113">Det är inga nya ändringar från version 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="e9e31-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="e9e31-114">Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="e9e31-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="e9e31-115">Installera</span><span class="sxs-lookup"><span data-stu-id="e9e31-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="e9e31-116">Viktig information</span><span class="sxs-lookup"><span data-stu-id="e9e31-116">Release Notes</span></span>
    * <span data-ttu-id="e9e31-117">Azurestack 1.4.0 har inga nya ändringar från den tidigare versionen 1.3.0</span><span class="sxs-lookup"><span data-stu-id="e9e31-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="e9e31-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="e9e31-119">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="e9e31-121">Nya parametrar BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays har lagts till i cmdlet:en Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="e9e31-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="e9e31-122">En cmdlet, New-EncyptionKeyBase64, har lagts till för att göra det möjligt att skapa en krypteringsnyckel</span><span class="sxs-lookup"><span data-stu-id="e9e31-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="e9e31-123">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="e9e31-125">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="e9e31-127">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="e9e31-128">En cmdlet, Add-AzsScaleUnitNode, har lagts till för att administratörer ska kunna lägga till nya skalningsenhetsnoder till azurestack-stämpeln</span><span class="sxs-lookup"><span data-stu-id="e9e31-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="e9e31-129">En ny cmdlet, New-AzsScaleUnitNodeObject, har lagts till för att göra det möjligt att skapa parameterobjekt för skalningsenhet</span><span class="sxs-lookup"><span data-stu-id="e9e31-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="e9e31-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="e9e31-131">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="e9e31-133">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="e9e31-135">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="e9e31-137">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="e9e31-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="e9e31-139">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="e9e31-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="e9e31-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="e9e31-141">En cmdlet, Move-AzsSubscription, har lagts till för flytt av prenumerationer mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="e9e31-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="e9e31-142">En cmdlet, Test-AzsMoveSubscription, har lagts till för att validera att användarprenumerationer kan flyttas mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="e9e31-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="e9e31-143">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="e9e31-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="e9e31-144">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="e9e31-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="e9e31-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="e9e31-145">Azure Bridge</span></span>
<span data-ttu-id="e9e31-146">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e31-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="e9e31-147">Backup</span><span class="sxs-lookup"><span data-stu-id="e9e31-147">Backup</span></span>
<span data-ttu-id="e9e31-148">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="e9e31-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="e9e31-149">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="e9e31-149">Configure where backups are stored</span></span>
- <span data-ttu-id="e9e31-150">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="e9e31-150">Perform backups</span></span>
- <span data-ttu-id="e9e31-151">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="e9e31-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="e9e31-152">Commerce</span><span class="sxs-lookup"><span data-stu-id="e9e31-152">Commerce</span></span>
<span data-ttu-id="e9e31-153">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="e9e31-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="e9e31-154">Compute</span><span class="sxs-lookup"><span data-stu-id="e9e31-154">Compute</span></span>
<span data-ttu-id="e9e31-155">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="e9e31-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="e9e31-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="e9e31-156">Fabric</span></span>
<span data-ttu-id="e9e31-157">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="e9e31-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="e9e31-158">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="e9e31-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="e9e31-159">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="e9e31-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="e9e31-160">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="e9e31-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="e9e31-161">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="e9e31-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="e9e31-162">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="e9e31-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="e9e31-163">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="e9e31-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="e9e31-164">Galleri</span><span class="sxs-lookup"><span data-stu-id="e9e31-164">Gallery</span></span>
<span data-ttu-id="e9e31-165">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e9e31-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="e9e31-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="e9e31-166">Infrastructure Insights</span></span>
<span data-ttu-id="e9e31-167">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="e9e31-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="e9e31-168">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="e9e31-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="e9e31-169">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="e9e31-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="e9e31-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9e31-170">KeyVault</span></span>
<span data-ttu-id="e9e31-171">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="e9e31-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="e9e31-172">Nätverk</span><span class="sxs-lookup"><span data-stu-id="e9e31-172">Network</span></span>
<span data-ttu-id="e9e31-173">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="e9e31-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="e9e31-174">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="e9e31-174">Management of network quotas</span></span>
- <span data-ttu-id="e9e31-175">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="e9e31-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="e9e31-176">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="e9e31-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="e9e31-177">Storage</span><span class="sxs-lookup"><span data-stu-id="e9e31-177">Storage</span></span>
<span data-ttu-id="e9e31-178">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="e9e31-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="e9e31-179">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="e9e31-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="e9e31-180">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="e9e31-180">Manage storage quotas</span></span>
- <span data-ttu-id="e9e31-181">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="e9e31-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="e9e31-182">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="e9e31-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="e9e31-183">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="e9e31-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="e9e31-184">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="e9e31-184">View information about the individual storage components</span></span>
- <span data-ttu-id="e9e31-185">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="e9e31-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="e9e31-186">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="e9e31-186">Subscription Admin</span></span>
<span data-ttu-id="e9e31-187">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="e9e31-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="e9e31-188">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="e9e31-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="e9e31-189">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="e9e31-189">Manage plans and offers</span></span>
- <span data-ttu-id="e9e31-190">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="e9e31-190">View usage and performance information</span></span>
- <span data-ttu-id="e9e31-191">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="e9e31-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="e9e31-192">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="e9e31-192">Subscription</span></span>
<span data-ttu-id="e9e31-193">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="e9e31-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="e9e31-194">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="e9e31-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="e9e31-195">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="e9e31-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="e9e31-196">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="e9e31-196">Update</span></span>
<span data-ttu-id="e9e31-197">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="e9e31-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="e9e31-198">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="e9e31-198">In this module administrators can:</span></span>
- <span data-ttu-id="e9e31-199">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="e9e31-199">List and install available updates</span></span>
- <span data-ttu-id="e9e31-200">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="e9e31-200">Resume interrupted updates</span></span>
- <span data-ttu-id="e9e31-201">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="e9e31-201">View installed updates</span></span>
