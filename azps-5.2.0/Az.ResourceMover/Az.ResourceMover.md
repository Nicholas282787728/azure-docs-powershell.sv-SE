---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410080"
---
# <span data-ttu-id="ee614-101">Modulen AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="ee614-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="ee614-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="ee614-102">Description</span></span>
<span data-ttu-id="ee614-103">Microsoft Azure PowerShell: ResourceMover-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ee614-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="ee614-104">AZ. ResourceMover-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ee614-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="ee614-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ee614-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="ee614-106">Skapar eller uppdaterar en flytt resurs i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="ee614-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="ee614-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="ee614-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="ee614-108">Hämtar flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="ee614-108">Gets the move collection.</span></span>

### [<span data-ttu-id="ee614-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ee614-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="ee614-110">Hämtar den flyttade resursen.</span><span class="sxs-lookup"><span data-stu-id="ee614-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="ee614-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="ee614-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="ee614-112">Hämtar en lista med olösta samband.</span><span class="sxs-lookup"><span data-stu-id="ee614-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="ee614-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="ee614-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="ee614-114">Aktiverar den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="ee614-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="ee614-115">Commit-åtgärden utlöses på moveResources i moveState "CommitPending" eller "CommitFailed" efter en lyckad slut för ande är moveResource moveState en över gång till bekräftat.</span><span class="sxs-lookup"><span data-stu-id="ee614-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="ee614-116">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="ee614-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="ee614-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="ee614-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="ee614-118">Tar bort den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="ee614-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="ee614-119">Åtgärden ta bort utlöses på moveResources i moveState "CommitPending" eller "DiscardFailed" efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="ee614-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ee614-120">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="ee614-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="ee614-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="ee614-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="ee614-122">Flyttar den uppsättning resurser som ingår i bröd texten.</span><span class="sxs-lookup"><span data-stu-id="ee614-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ee614-123">Flytt åtgärden utlöses efter att moveResources finns i moveState "MovePending" eller "MoveFailed" efter en lyckad slut för ande är moveResource moveState en över gång till CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ee614-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ee614-124">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="ee614-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="ee614-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="ee614-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="ee614-126">Initierar förberedelse för den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="ee614-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="ee614-127">Förberedelse åtgärden är på moveResources som finns i moveState "PreparePending" eller "PrepareFailed", efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="ee614-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ee614-128">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="ee614-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="ee614-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="ee614-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="ee614-130">Skapar eller uppdaterar en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="ee614-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="ee614-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="ee614-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="ee614-132">Tar bort en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="ee614-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="ee614-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ee614-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="ee614-134">Tar bort en flytt resurs från flytt samlingen.</span><span class="sxs-lookup"><span data-stu-id="ee614-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="ee614-135">Lös-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="ee614-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="ee614-136">Beräknar, löser och validerar beroendena för moveResources i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="ee614-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

