---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93743284"
---
# <span data-ttu-id="c8aa9-101">Modulen AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="c8aa9-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="c8aa9-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="c8aa9-102">Description</span></span>
<span data-ttu-id="c8aa9-103">Med cmdletar i modulen synkronisering av lagring kan du hantera åtgärder för Azure-filsynkronisering i PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="c8aa9-104">AZ. StorageSync-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c8aa9-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="c8aa9-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c8aa9-106">Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="c8aa9-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c8aa9-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="c8aa9-108">Det här kommandot visar alla synkroniseringsresurser i en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="c8aa9-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c8aa9-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="c8aa9-110">Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="c8aa9-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c8aa9-112">Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="c8aa9-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c8aa9-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="c8aa9-114">Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="c8aa9-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="c8aa9-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="c8aa9-116">Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c8aa9-117">Den kan riktas till hela resursen, undermappen eller uppsättningen filer.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c8aa9-118">Högst 10 000-ändringar kan identifieras.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="c8aa9-119">Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföras snabbt och i en 10 000-ändrings gräns.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="c8aa9-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="c8aa9-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="c8aa9-121">Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="c8aa9-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="c8aa9-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="c8aa9-123">Det här kommandot återställer alla nivåbaserade filer tillbaka till lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="c8aa9-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c8aa9-125">Det här kommandot skapar en Azure File Sync-slutpunkt för moln i en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="c8aa9-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c8aa9-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="c8aa9-127">Det här kommandot skapar en ny synkroniseringsresurs i en angiven synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="c8aa9-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c8aa9-129">Det här kommandot skapar en ny server slut punkt på en registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="c8aa9-130">Då aktive ras den angivna sökvägen på servern för att synkronisera filer med andra slut punkter i synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="c8aa9-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c8aa9-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="c8aa9-132">Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="c8aa9-133">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c8aa9-133">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="c8aa9-134">Det här kommandot registrerar en server i en lagrings tjänst som skapar en förtroende relation.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-134">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="c8aa9-135">PowerShell eller Azure-portalen kan sedan användas för att konfigurera synkronisering på den här servern.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-135">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="c8aa9-136">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-136">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c8aa9-137">Det här kommandot tar bort den angivna moln slut punkten från en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-137">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="c8aa9-138">Utan åtminstone en moln slut punkt kan ingen annan server slut punkter i den här synkroniseringsresursen synkronisera.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-138">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="c8aa9-139">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c8aa9-139">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="c8aa9-140">Det här kommandot tar bort den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-140">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="c8aa9-141">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-141">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c8aa9-142">Det här kommandot tar bort den angivna Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-142">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="c8aa9-143">Synkronisering till den här platsen stoppas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-143">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="c8aa9-144">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c8aa9-144">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="c8aa9-145">Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-145">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="c8aa9-146">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c8aa9-146">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="c8aa9-147">Används endast för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-147">Use for troubleshooting only.</span></span> <span data-ttu-id="c8aa9-148">Det här kommandot återställer Server certifikatet för lagringstester som används för att beskriva Server identiteten för Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-148">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="c8aa9-149">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8aa9-149">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c8aa9-150">Det här kommandot möjliggör ändringar i de justerbara parametrarna för en server slut punkt.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-150">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="c8aa9-151">Avregistrera-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c8aa9-151">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="c8aa9-152">Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-152">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="c8aa9-153">Det här kommandot avregistrerar en server från tjänsten Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="c8aa9-153">This command will unregister a server from it's storage sync service.</span></span>

