# <a name="azure-stack-module-130"></a><span data-ttu-id="a963e-101">Modulen Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="a963e-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a963e-102">Krav:</span><span class="sxs-lookup"><span data-stu-id="a963e-102">Requirements:</span></span>
<span data-ttu-id="a963e-103">Lägsta version av Azure Stack som stöds är 1804.</span><span class="sxs-lookup"><span data-stu-id="a963e-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="a963e-104">Obs! Om du använder en tidigare version måste du installera version 1.2.11</span><span class="sxs-lookup"><span data-stu-id="a963e-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="a963e-105">Kända problem:</span><span class="sxs-lookup"><span data-stu-id="a963e-105">Known issues:</span></span>

- <span data-ttu-id="a963e-106">Stäng avisering kräver Azure Stack version 1803</span><span class="sxs-lookup"><span data-stu-id="a963e-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="a963e-107">Vissa cmdletar för Storage kräver Azure Stack version 1804</span><span class="sxs-lookup"><span data-stu-id="a963e-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="a963e-108">Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig.</span><span class="sxs-lookup"><span data-stu-id="a963e-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="a963e-109">Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.</span><span class="sxs-lookup"><span data-stu-id="a963e-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="a963e-110">För att en IP-pool ska kunna tas bort krävs en omdistribution</span><span class="sxs-lookup"><span data-stu-id="a963e-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="a963e-111">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="a963e-111">Breaking Changes</span></span>
<span data-ttu-id="a963e-112">Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="a963e-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="a963e-113">Installera</span><span class="sxs-lookup"><span data-stu-id="a963e-113">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="a963e-114">Innehåll:</span><span class="sxs-lookup"><span data-stu-id="a963e-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="a963e-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="a963e-115">Azure Bridge</span></span>
<span data-ttu-id="a963e-116">Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.</span><span class="sxs-lookup"><span data-stu-id="a963e-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="a963e-117">Backup</span><span class="sxs-lookup"><span data-stu-id="a963e-117">Backup</span></span>
<span data-ttu-id="a963e-118">Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="a963e-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="a963e-119">Konfigurera var säkerhetskopiorna ska lagras</span><span class="sxs-lookup"><span data-stu-id="a963e-119">Configure where backups are stored</span></span>
- <span data-ttu-id="a963e-120">Säkerhetskopiera</span><span class="sxs-lookup"><span data-stu-id="a963e-120">Perform backups</span></span>
- <span data-ttu-id="a963e-121">Lista och återställda slutförda säkerhetskopior</span><span class="sxs-lookup"><span data-stu-id="a963e-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="a963e-122">Commerce</span><span class="sxs-lookup"><span data-stu-id="a963e-122">Commerce</span></span>
<span data-ttu-id="a963e-123">Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.</span><span class="sxs-lookup"><span data-stu-id="a963e-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="a963e-124">Compute</span><span class="sxs-lookup"><span data-stu-id="a963e-124">Compute</span></span>
<span data-ttu-id="a963e-125">Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a963e-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="a963e-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="a963e-126">Fabric</span></span>
<span data-ttu-id="a963e-127">Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:</span><span class="sxs-lookup"><span data-stu-id="a963e-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="a963e-128">Stoppa, starta och stänga ned noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="a963e-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="a963e-129">Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter</span><span class="sxs-lookup"><span data-stu-id="a963e-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="a963e-130">Reparation av noder för skalningsenheter</span><span class="sxs-lookup"><span data-stu-id="a963e-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="a963e-131">Omstart av infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="a963e-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="a963e-132">Stoppa, starta och stänga ned instanser av infrastrukturroller</span><span class="sxs-lookup"><span data-stu-id="a963e-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="a963e-133">Skapa nya IP-pooler</span><span class="sxs-lookup"><span data-stu-id="a963e-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="a963e-134">Galleri</span><span class="sxs-lookup"><span data-stu-id="a963e-134">Gallery</span></span>
<span data-ttu-id="a963e-135">Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="a963e-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="a963e-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="a963e-136">Infrastructure Insights</span></span>
<span data-ttu-id="a963e-137">Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:</span><span class="sxs-lookup"><span data-stu-id="a963e-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="a963e-138">Visa hälsotillstånd för sina stämpelresurser i Azure Stack</span><span class="sxs-lookup"><span data-stu-id="a963e-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="a963e-139">Visa och hantera aviseringar</span><span class="sxs-lookup"><span data-stu-id="a963e-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="a963e-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a963e-140">KeyVault</span></span>
<span data-ttu-id="a963e-141">Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.</span><span class="sxs-lookup"><span data-stu-id="a963e-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="a963e-142">Nätverk</span><span class="sxs-lookup"><span data-stu-id="a963e-142">Network</span></span>
<span data-ttu-id="a963e-143">Förhandsversionen av administratörsmodulen för Network med funktioner för:</span><span class="sxs-lookup"><span data-stu-id="a963e-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="a963e-144">Hantering av nätverkskvoter</span><span class="sxs-lookup"><span data-stu-id="a963e-144">Management of network quotas</span></span>
- <span data-ttu-id="a963e-145">Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="a963e-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="a963e-146">Tillhandahåller en cmdlet som visar en administratörsöversikt</span><span class="sxs-lookup"><span data-stu-id="a963e-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="a963e-147">Storage</span><span class="sxs-lookup"><span data-stu-id="a963e-147">Storage</span></span>
<span data-ttu-id="a963e-148">Förhandsversion av administratörsmodulen Azure Stack Storage.</span><span class="sxs-lookup"><span data-stu-id="a963e-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="a963e-149">I den här versionen tillhandahåller vi funktioner för:</span><span class="sxs-lookup"><span data-stu-id="a963e-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="a963e-150">Hantering av lagringskvoter</span><span class="sxs-lookup"><span data-stu-id="a963e-150">Manage storage quotas</span></span>
- <span data-ttu-id="a963e-151">Skräpinsamling av raderade lagringsresurser</span><span class="sxs-lookup"><span data-stu-id="a963e-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="a963e-152">Återställning av raderade lagringskonton</span><span class="sxs-lookup"><span data-stu-id="a963e-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="a963e-153">Migrering av behållare från en resurs till en annan</span><span class="sxs-lookup"><span data-stu-id="a963e-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="a963e-154">Visning av information om enskilda lagringskomponenter</span><span class="sxs-lookup"><span data-stu-id="a963e-154">View information about the individual storage components</span></span>
- <span data-ttu-id="a963e-155">Visning av information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="a963e-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="a963e-156">Prenumerationsadministration</span><span class="sxs-lookup"><span data-stu-id="a963e-156">Subscription Admin</span></span>
<span data-ttu-id="a963e-157">Förhandsversion av administratörsmodulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="a963e-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="a963e-158">Den här modulen innehåller administratörsfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="a963e-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="a963e-159">Hantera avtal och erbjudanden</span><span class="sxs-lookup"><span data-stu-id="a963e-159">Manage plans and offers</span></span>
- <span data-ttu-id="a963e-160">Visa information om användning och prestanda</span><span class="sxs-lookup"><span data-stu-id="a963e-160">View usage and performance information</span></span>
- <span data-ttu-id="a963e-161">Hantera RBAC</span><span class="sxs-lookup"><span data-stu-id="a963e-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="a963e-162">Prenumeration</span><span class="sxs-lookup"><span data-stu-id="a963e-162">Subscription</span></span>
<span data-ttu-id="a963e-163">Förhandsversion av modulen Azure Stack Subscription.</span><span class="sxs-lookup"><span data-stu-id="a963e-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="a963e-164">Den här modulen innehåller användarfunktioner för att:</span><span class="sxs-lookup"><span data-stu-id="a963e-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="a963e-165">Skapa, ta bort och uppdatera prenumerationer</span><span class="sxs-lookup"><span data-stu-id="a963e-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="a963e-166">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="a963e-166">Update</span></span>
<span data-ttu-id="a963e-167">Förhandsversion av administratörsmodulen Azure Stack Update.</span><span class="sxs-lookup"><span data-stu-id="a963e-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="a963e-168">I den här kan modulen kan administratörer:</span><span class="sxs-lookup"><span data-stu-id="a963e-168">In this module administrators can:</span></span>
- <span data-ttu-id="a963e-169">Lista och installera tillgängliga uppdateringar</span><span class="sxs-lookup"><span data-stu-id="a963e-169">List and install available updates</span></span>
- <span data-ttu-id="a963e-170">Återuppta avbrutna uppdateringar</span><span class="sxs-lookup"><span data-stu-id="a963e-170">Resume interrupted updates</span></span>
- <span data-ttu-id="a963e-171">Visa installerade uppdateringar</span><span class="sxs-lookup"><span data-stu-id="a963e-171">View installed updates</span></span>
