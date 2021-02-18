---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253252"
---
# Az.ResourceMover-modul
## Beskrivning
Microsoft Azure PowerShell: ResourceMover-cmdlets

## Az.ResourceMover-cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Skapar eller uppdaterar en flyttresurs i flyttningssamlingen.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Hämtar flyttningssamlingen.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Hämtar flyttresursen.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Får en lista över omatchade beroenden.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Åtar sig den uppsättning resurser som ingår i begärans brödtext.
Commit-åtgärden utlöses för moveResources i moveState 'CommitPending' eller 'CommitFailed'. När moveResource moveState har slutförts gör moveResource moveState en övergång till Committed.
För att hjälpa användaren att göra en nödvändiga åtgärd kan klienten anropa åtgärden med egenskapen ValidateOnly inställd på sant.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Tar bort uppsättningen resurser som ingår i begärans brödtext.
Åtgärden discard utlöses för moveResources i moveState 'CommitPending' eller 'DiscardFailed', och när moveResource moveState har slutförts gör moveResource moveState en övergång till MovePending.
För att hjälpa användaren att göra en nödvändiga åtgärd kan klienten anropa åtgärden med egenskapen ValidateOnly inställd på sant.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Flyttar den uppsättning resurser som ingår i begärans brödtext.
Flyttningsåtgärden utlöses när moveResources ligger i moveState 'MovePending' eller 'MoveFailed', och moveResource moveState har slutförts gör moveResource moveState en övergång till CommitPending.
För att hjälpa användaren att göra en nödvändiga åtgärd kan klienten anropa åtgärden med egenskapen ValidateOnly inställd på sant.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Initierar förberedelse för uppsättningen resurser som ingår i begärans brödtext.
Förberedelseåtgärden är på de moveResources som finns i moveState 'PreparePending' eller 'PrepareFailed', när moveResource moveState har slutförts gör moveResource moveState en övergång till MovePending.
För att hjälpa användaren att göra en nödvändiga åtgärd kan klienten anropa åtgärden med egenskapen ValidateOnly inställd på sant.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Skapar eller uppdaterar en flyttningssamling.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Tar bort en flyttningssamling.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Tar bort en flytta resurs från flyttningssamlingen.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Beräknar, löser och verifierar sambanden för moveResources i flyttningssamlingen.

