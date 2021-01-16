---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397128"
---
# <span data-ttu-id="0fb21-101">Modulen AZ. ImportExport</span><span class="sxs-lookup"><span data-stu-id="0fb21-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="0fb21-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="0fb21-102">Description</span></span>
<span data-ttu-id="0fb21-103">Microsoft Azure PowerShell: ImportExport-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0fb21-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="0fb21-104">AZ. ImportExport-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0fb21-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="0fb21-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0fb21-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="0fb21-106">Hämtar information om ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb21-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="0fb21-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="0fb21-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="0fb21-108">Returnerar BitLocker-nycklarna för alla enheter i det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb21-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="0fb21-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="0fb21-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="0fb21-110">Returnerar informationen om en plats där du kan leverera de diskar som är associerade med ett import-eller export jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb21-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="0fb21-111">En plats är ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="0fb21-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="0fb21-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0fb21-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="0fb21-113">Skapar ett nytt jobb eller uppdaterar ett befintligt jobb i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0fb21-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="0fb21-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="0fb21-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="0fb21-115">Skapa ett DriverList-objekt för ImportExport.</span><span class="sxs-lookup"><span data-stu-id="0fb21-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="0fb21-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0fb21-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="0fb21-117">Tar bort ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb21-117">Deletes an existing job.</span></span>
<span data-ttu-id="0fb21-118">Det är bara jobb i tillståndet skapa eller slutfört som kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="0fb21-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="0fb21-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0fb21-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="0fb21-120">Uppdaterar specifika egenskaper för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb21-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="0fb21-121">Du kan ringa den här åtgärden för att meddela import-och export tjänsten att hård diskarna som innehåller import-eller export jobbet har levererats till Microsoft Data Center.</span><span class="sxs-lookup"><span data-stu-id="0fb21-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="0fb21-122">Den kan också användas för att avbryta ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb21-122">It can also be used to cancel an existing job.</span></span>

