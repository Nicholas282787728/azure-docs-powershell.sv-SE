---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 8b74dd57a85a39403f56840dd0fc54b3f25184f1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921414"
---
# <span data-ttu-id="01a15-101">AZS. Compute. admin-modul</span><span class="sxs-lookup"><span data-stu-id="01a15-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="01a15-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="01a15-102">Description</span></span>
<span data-ttu-id="01a15-103">För hands version av AzureStack Compute-administratör som tillhandahåller funktioner för att hantera beräknings kvoter, plattforms bilder och virtuella dator tillägg samt för hanterade diskar för att balansera lagring.</span><span class="sxs-lookup"><span data-stu-id="01a15-103">Preview release of the AzureStack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="01a15-104">AZS. Compute. admin-cmdletar</span><span class="sxs-lookup"><span data-stu-id="01a15-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="01a15-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="01a15-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="01a15-106">Lägga till en plattform för virtuell dator från en given bild konfiguration.</span><span class="sxs-lookup"><span data-stu-id="01a15-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="01a15-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="01a15-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="01a15-108">Skapa en ny tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01a15-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="01a15-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="01a15-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="01a15-110">Returnerar kvoter som anger kvot gränser för beräkning av objekt.</span><span class="sxs-lookup"><span data-stu-id="01a15-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="01a15-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="01a15-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="01a15-112">Returnerar listan med hanterade diskar som kan migreras i den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="01a15-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="01a15-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="01a15-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="01a15-114">Returnerar listan med hanterade Migreringsverktyg för diskar.</span><span class="sxs-lookup"><span data-stu-id="01a15-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="01a15-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="01a15-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="01a15-116">Returnerar virtuella dator bilder som laddats till plattforms bild lagringen.</span><span class="sxs-lookup"><span data-stu-id="01a15-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="01a15-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="01a15-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="01a15-118">Returnerar befintliga bild tillägg för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01a15-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="01a15-119">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="01a15-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="01a15-120">Skapa en ny Beräknad kvot som används för att begränsa beräknings resurserna.</span><span class="sxs-lookup"><span data-stu-id="01a15-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="01a15-121">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="01a15-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="01a15-122">Startar ett migreringsjobb med hanterade diskar för att migrera hanterade diskar till angiven mål resurs.</span><span class="sxs-lookup"><span data-stu-id="01a15-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="01a15-123">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="01a15-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="01a15-124">Skapar en data disk som används för att skapa en ny plattform för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01a15-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="01a15-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="01a15-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="01a15-126">Tar bort angiven Beräknad kvot.</span><span class="sxs-lookup"><span data-stu-id="01a15-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="01a15-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="01a15-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="01a15-128">Ta bort en virtuell dator bild från Platform image lagring.</span><span class="sxs-lookup"><span data-stu-id="01a15-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="01a15-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="01a15-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="01a15-130">Tar bort en tilläggs bild för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="01a15-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="01a15-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="01a15-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="01a15-132">Uppdatera en befintlig Beräknad kvot med de tillhandahållna parametrarna.</span><span class="sxs-lookup"><span data-stu-id="01a15-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="01a15-133">Stopp-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="01a15-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="01a15-134">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="01a15-134">Cancel a managed disk migration job.</span></span>
