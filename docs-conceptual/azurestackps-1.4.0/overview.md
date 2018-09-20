# <a name="azure-stack-module-140"></a><span data-ttu-id="6d3f5-101">Modulen Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="6d3f5-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3f5-102">Krav:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-102">Requirements:</span></span>
<span data-ttu-id="6d3f5-103">Lägsta version av Azure Stack som stöds är 1804.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="6d3f5-104">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="6d3f5-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="6d3f5-105">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-105">Known issues:</span></span>

- <span data-ttu-id="6d3f5-106">Stäng avisering kräver Azure Stack version 1803</span><span class="sxs-lookup"><span data-stu-id="6d3f5-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="6d3f5-107">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="6d3f5-108">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="6d3f5-109">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="6d3f5-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="6d3f5-110">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="6d3f5-110">Breaking Changes</span></span>
<span data-ttu-id="6d3f5-111">Det är inga nya ändringar från version 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="6d3f5-112">Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="6d3f5-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="6d3f5-113">Installera</span><span class="sxs-lookup"><span data-stu-id="6d3f5-113">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="6d3f5-114">Viktig information</span><span class="sxs-lookup"><span data-stu-id="6d3f5-114">Release Notes</span></span>
    * <span data-ttu-id="6d3f5-115">Azurestack 1.4.0 har inga nya ändringar från den tidigare versionen 1.3.0</span><span class="sxs-lookup"><span data-stu-id="6d3f5-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="6d3f5-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="6d3f5-117">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="6d3f5-119">Nya parametrar BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays har lagts till i cmdlet:en Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="6d3f5-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="6d3f5-120">En cmdlet, New-EncyptionKeyBase64, har lagts till för att göra det möjligt att skapa en krypteringsnyckel</span><span class="sxs-lookup"><span data-stu-id="6d3f5-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="6d3f5-121">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="6d3f5-123">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="6d3f5-125">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="6d3f5-126">En cmdlet, Add-AzsScaleUnitNode, har lagts till för att administratörer ska kunna lägga till nya skalningsenhetsnoder till azurestack-stämpeln</span><span class="sxs-lookup"><span data-stu-id="6d3f5-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="6d3f5-127">En ny cmdlet, New-AzsScaleUnitNodeObject, har lagts till för att göra det möjligt att skapa parameterobjekt för skalningsenhet</span><span class="sxs-lookup"><span data-stu-id="6d3f5-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="6d3f5-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="6d3f5-129">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="6d3f5-131">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="6d3f5-133">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="6d3f5-135">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="6d3f5-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="6d3f5-137">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6d3f5-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="6d3f5-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="6d3f5-139">En cmdlet, Move-AzsSubscription, har lagts till för flytt av prenumerationer mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="6d3f5-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="6d3f5-140">En cmdlet, Test-AzsMoveSubscription, har lagts till för att validera att användarprenumerationer kan flyttas mellan delegerade providererbjudanden</span><span class="sxs-lookup"><span data-stu-id="6d3f5-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="6d3f5-141">Korrigering för felet som returnerade en enda sida i sidnumrerade resultat</span><span class="sxs-lookup"><span data-stu-id="6d3f5-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="6d3f5-142">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="6d3f5-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="6d3f5-143">Azure Bridge</span></span>
<span data-ttu-id="6d3f5-144">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="6d3f5-145">Backup</span><span class="sxs-lookup"><span data-stu-id="6d3f5-145">Backup</span></span>
<span data-ttu-id="6d3f5-146">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="6d3f5-147">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="6d3f5-147">Configure where backups are stored</span></span>
- <span data-ttu-id="6d3f5-148">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="6d3f5-148">Perform backups</span></span>
- <span data-ttu-id="6d3f5-149">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="6d3f5-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="6d3f5-150">Commerce</span><span class="sxs-lookup"><span data-stu-id="6d3f5-150">Commerce</span></span>
<span data-ttu-id="6d3f5-151">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="6d3f5-152">Compute</span><span class="sxs-lookup"><span data-stu-id="6d3f5-152">Compute</span></span>
<span data-ttu-id="6d3f5-153">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="6d3f5-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="6d3f5-154">Fabric</span></span>
<span data-ttu-id="6d3f5-155">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="6d3f5-156">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="6d3f5-157">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="6d3f5-158">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="6d3f5-159">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="6d3f5-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="6d3f5-160">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="6d3f5-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="6d3f5-161">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="6d3f5-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="6d3f5-162">Galleri</span><span class="sxs-lookup"><span data-stu-id="6d3f5-162">Gallery</span></span>
<span data-ttu-id="6d3f5-163">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="6d3f5-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="6d3f5-164">Infrastructure Insights</span></span>
<span data-ttu-id="6d3f5-165">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="6d3f5-166">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="6d3f5-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="6d3f5-167">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="6d3f5-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="6d3f5-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d3f5-168">KeyVault</span></span>
<span data-ttu-id="6d3f5-169">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="6d3f5-170">Nätverk</span><span class="sxs-lookup"><span data-stu-id="6d3f5-170">Network</span></span>
<span data-ttu-id="6d3f5-171">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="6d3f5-172">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-172">Management of network quotas</span></span>
- <span data-ttu-id="6d3f5-173">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare</span><span class="sxs-lookup"><span data-stu-id="6d3f5-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="6d3f5-174">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="6d3f5-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="6d3f5-175">Storage</span><span class="sxs-lookup"><span data-stu-id="6d3f5-175">Storage</span></span>
<span data-ttu-id="6d3f5-176">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="6d3f5-177">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="6d3f5-178">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-178">Manage storage quotas</span></span>
- <span data-ttu-id="6d3f5-179">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="6d3f5-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="6d3f5-180">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="6d3f5-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="6d3f5-181">Migrering av containrar från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="6d3f5-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="6d3f5-182">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="6d3f5-182">View information about the individual storage components</span></span>
- <span data-ttu-id="6d3f5-183">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="6d3f5-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="6d3f5-184">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="6d3f5-184">Subscription Admin</span></span>
<span data-ttu-id="6d3f5-185">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="6d3f5-186">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="6d3f5-187">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="6d3f5-187">Manage plans and offers</span></span>
- <span data-ttu-id="6d3f5-188">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="6d3f5-188">View usage and performance information</span></span>
- <span data-ttu-id="6d3f5-189">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="6d3f5-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="6d3f5-190">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="6d3f5-190">Subscription</span></span>
<span data-ttu-id="6d3f5-191">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="6d3f5-192">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="6d3f5-193">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="6d3f5-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="6d3f5-194">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="6d3f5-194">Update</span></span>
<span data-ttu-id="6d3f5-195">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="6d3f5-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="6d3f5-196">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="6d3f5-196">In this module administrators can:</span></span>
- <span data-ttu-id="6d3f5-197">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="6d3f5-197">List and install available updates</span></span>
- <span data-ttu-id="6d3f5-198">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="6d3f5-198">Resume interrupted updates</span></span>
- <span data-ttu-id="6d3f5-199">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="6d3f5-199">View installed updates</span></span>
