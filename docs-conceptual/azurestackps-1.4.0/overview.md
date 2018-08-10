# <a name="azure-stack-module-140"></a><span data-ttu-id="1ed98-101">Modulen Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="1ed98-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed98-102">Krav:</span><span class="sxs-lookup"><span data-stu-id="1ed98-102">Requirements:</span></span>
<span data-ttu-id="1ed98-103">Lägsta version av Azure Stack som stöds är 1804.</span><span class="sxs-lookup"><span data-stu-id="1ed98-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="1ed98-104">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="1ed98-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="1ed98-105">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="1ed98-105">Known issues:</span></span>

- <span data-ttu-id="1ed98-106">Stäng avisering kräver Azure Stack version 1803</span><span class="sxs-lookup"><span data-stu-id="1ed98-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="1ed98-107">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="1ed98-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="1ed98-108">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="1ed98-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="1ed98-109">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="1ed98-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="1ed98-110">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="1ed98-110">Breaking Changes</span></span>
<span data-ttu-id="1ed98-111">Det är inga nya ändringar från version 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="1ed98-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="1ed98-112">Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="1ed98-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="1ed98-113">Installera</span><span class="sxs-lookup"><span data-stu-id="1ed98-113">Install</span></span>
```
# 1.4.0 can be installed side by side with 1.3.0
# Remove previous version 1.2.11
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="1ed98-114">Viktig information</span><span class="sxs-lookup"><span data-stu-id="1ed98-114">Release Notes</span></span>
    * <span data-ttu-id="1ed98-115">Azurestack 1.4.0 har inga nya ändringar från den tidigare versionen 1.3.0</span><span class="sxs-lookup"><span data-stu-id="1ed98-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="1ed98-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="1ed98-117">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="1ed98-119">Nya parametrar BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays har lagts till i cmdlet:en Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="1ed98-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="1ed98-120">En cmdlet, New-EncyptionKeyBase64, har lagts till för att göra det möjligt att skapa en krypteringsnyckel</span><span class="sxs-lookup"><span data-stu-id="1ed98-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="1ed98-121">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="1ed98-123">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="1ed98-125">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="1ed98-126">En cmdlet, Add-AzsScaleUnitNode, har lagts till för att administratörer ska kunna lägga till nya skalningsenhetsnoder till azurestack-stämpeln</span><span class="sxs-lookup"><span data-stu-id="1ed98-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="1ed98-127">En ny cmdlet, New-AzsScaleUnitNodeObject, har lagts till för att göra det möjligt att skapa parameterobjekt för skalningsenhet</span><span class="sxs-lookup"><span data-stu-id="1ed98-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="1ed98-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="1ed98-129">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="1ed98-131">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="1ed98-133">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="1ed98-135">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="1ed98-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="1ed98-137">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="1ed98-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="1ed98-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="1ed98-139">En cmdlet, Move-AzsSubscription, har lagts till för flytt av prenumerationer mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="1ed98-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="1ed98-140">En cmdlet, Test-AzsMoveSubscription, har lagts till för att validera att användarprenumerationer kan flyttas mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="1ed98-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="1ed98-141">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="1ed98-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="1ed98-142">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="1ed98-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="1ed98-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="1ed98-143">Azure Bridge</span></span>
<span data-ttu-id="1ed98-144">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed98-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="1ed98-145">Backup</span><span class="sxs-lookup"><span data-stu-id="1ed98-145">Backup</span></span>
<span data-ttu-id="1ed98-146">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="1ed98-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="1ed98-147">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="1ed98-147">Configure where backups are stored</span></span>
- <span data-ttu-id="1ed98-148">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="1ed98-148">Perform backups</span></span>
- <span data-ttu-id="1ed98-149">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="1ed98-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="1ed98-150">Commerce</span><span class="sxs-lookup"><span data-stu-id="1ed98-150">Commerce</span></span>
<span data-ttu-id="1ed98-151">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="1ed98-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="1ed98-152">Compute</span><span class="sxs-lookup"><span data-stu-id="1ed98-152">Compute</span></span>
<span data-ttu-id="1ed98-153">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="1ed98-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="1ed98-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="1ed98-154">Fabric</span></span>
<span data-ttu-id="1ed98-155">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="1ed98-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="1ed98-156">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="1ed98-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="1ed98-157">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="1ed98-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="1ed98-158">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="1ed98-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="1ed98-159">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="1ed98-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="1ed98-160">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="1ed98-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="1ed98-161">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="1ed98-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="1ed98-162">Galleri</span><span class="sxs-lookup"><span data-stu-id="1ed98-162">Gallery</span></span>
<span data-ttu-id="1ed98-163">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="1ed98-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="1ed98-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="1ed98-164">Infrastructure Insights</span></span>
<span data-ttu-id="1ed98-165">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="1ed98-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="1ed98-166">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="1ed98-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="1ed98-167">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="1ed98-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="1ed98-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ed98-168">KeyVault</span></span>
<span data-ttu-id="1ed98-169">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="1ed98-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="1ed98-170">Nätverk</span><span class="sxs-lookup"><span data-stu-id="1ed98-170">Network</span></span>
<span data-ttu-id="1ed98-171">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="1ed98-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="1ed98-172">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="1ed98-172">Management of network quotas</span></span>
- <span data-ttu-id="1ed98-173">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="1ed98-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="1ed98-174">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="1ed98-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="1ed98-175">Storage</span><span class="sxs-lookup"><span data-stu-id="1ed98-175">Storage</span></span>
<span data-ttu-id="1ed98-176">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="1ed98-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="1ed98-177">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="1ed98-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="1ed98-178">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="1ed98-178">Manage storage quotas</span></span>
- <span data-ttu-id="1ed98-179">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="1ed98-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="1ed98-180">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="1ed98-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="1ed98-181">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="1ed98-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="1ed98-182">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="1ed98-182">View information about the individual storage components</span></span>
- <span data-ttu-id="1ed98-183">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="1ed98-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="1ed98-184">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="1ed98-184">Subscription Admin</span></span>
<span data-ttu-id="1ed98-185">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="1ed98-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="1ed98-186">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="1ed98-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="1ed98-187">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="1ed98-187">Manage plans and offers</span></span>
- <span data-ttu-id="1ed98-188">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="1ed98-188">View usage and performance information</span></span>
- <span data-ttu-id="1ed98-189">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="1ed98-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="1ed98-190">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="1ed98-190">Subscription</span></span>
<span data-ttu-id="1ed98-191">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="1ed98-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="1ed98-192">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="1ed98-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="1ed98-193">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="1ed98-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="1ed98-194">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="1ed98-194">Update</span></span>
<span data-ttu-id="1ed98-195">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="1ed98-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="1ed98-196">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="1ed98-196">In this module administrators can:</span></span>
- <span data-ttu-id="1ed98-197">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="1ed98-197">List and install available updates</span></span>
- <span data-ttu-id="1ed98-198">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="1ed98-198">Resume interrupted updates</span></span>
- <span data-ttu-id="1ed98-199">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="1ed98-199">View installed updates</span></span>
