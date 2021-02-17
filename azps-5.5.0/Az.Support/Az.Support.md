---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216911"
---
# Az.Support Module
## Beskrivning
Avsnitten i det här avsnittet innehåller Azure PowerShell-cmdlets för att skapa och hantera Azure-supportärenden i Azure Resource Manager-ramverket (ARM). Cmdletarna finns i namnområdet Microsoft.Azure.Commands.Support

## Az.Support-cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Hämtar den aktuella listan över Azure-tjänster som det finns support för. Varje Azure-tjänst har en egen uppsättning kategorier som kallas problemklassificering. Hämta den aktuella listan med problemklassificering för en tjänst med Get-AzSupportProblemClassification. Du kan använda tjänsten och problemklassificerings-GUID för att skapa ett nytt supportärende med hjälp av New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Hämtar den aktuella listan över problemklassificering för en Azure-tjänst. Du kan använda tjänsten och problemklassificerings-GUID för att skapa ett nytt supportärende med hjälp av New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet för helper för att skapa ett kontaktprofilobjekt för support. Du kan använda det här objektet New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Skapar ett nytt Support-ärende för Azure. Den här åtgärden har modellerats på beteendet på sidan för Azure [New support request.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Får listan över supportärenden. Du kan få fullständiga supportärenden efter biljettnamn eller filtrera supportärenden efter *status* eller *CreatedDate.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Uppdatera allvarlighetsgrad, status eller kontaktinformation för ett support ärende.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Får meddelanden för ett support ärende. Du kan också filtrera supportmeddelanden via *CreatedDate eller* *CommunicationType.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Lägger till en ny kundkommunikation i ett Support-ärende i Azure. 



