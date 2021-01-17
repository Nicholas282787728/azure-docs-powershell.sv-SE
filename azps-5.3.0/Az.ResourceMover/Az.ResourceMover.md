---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421000"
---
# Modulen AZ. ResourceMover
## Problembeskrivning
Microsoft Azure PowerShell: ResourceMover-cmdletar

## AZ. ResourceMover-cmdletar
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Skapar eller uppdaterar en flytt resurs i flytt mängden.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Hämtar flytt mängden.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Hämtar den flyttade resursen.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Hämtar en lista med olösta samband.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Aktiverar den uppsättning resurser som ingår i förfrågnings texten.
Commit-åtgärden utlöses på moveResources i moveState "CommitPending" eller "CommitFailed" efter en lyckad slut för ande är moveResource moveState en över gång till bekräftat.
För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Tar bort den uppsättning resurser som ingår i förfrågnings texten.
Åtgärden ta bort utlöses på moveResources i moveState "CommitPending" eller "DiscardFailed" efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.
För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Flyttar den uppsättning resurser som ingår i bröd texten.
Flytt åtgärden utlöses efter att moveResources finns i moveState "MovePending" eller "MoveFailed" efter en lyckad slut för ande är moveResource moveState en över gång till CommitPending.
För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Initierar förberedelse för den uppsättning resurser som ingår i förfrågnings texten.
Förberedelse åtgärden är på moveResources som finns i moveState "PreparePending" eller "PrepareFailed", efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.
För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Skapar eller uppdaterar en flytt mängd.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Tar bort en flytt mängd.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Tar bort en flytt resurs från flytt samlingen.

### [Lös-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Beräknar, löser och validerar beroendena för moveResources i flytt mängden.

