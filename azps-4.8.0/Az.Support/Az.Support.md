---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258967"
---
# AZ. support-modul
## Problembeskrivning
Ämnena i det här avsnittet dokumenterar Azure PowerShell-cmdletar för att skapa och hantera Azure support biljetter i ramverket Azure Resource Manager (ARM). Det finns cmdlets i Microsoft. Azure. commands. support-namnrymd

## AZ. support-cmdletar
### [Get-AzSupportService](Get-AzSupportService.md)
Hämtar den aktuella listan med Azure-tjänster som stöder support. Varje Azure-tjänst har sin egen uppsättning kategorier som kallas problem klassificering. Hämta den aktuella listan över problem klassificering för en tjänst med Get-AzSupportProblemClassification. Du kan använda tjänst-och problem klassificerings-GUID för att skapa ett nytt support ärende med hjälp av New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Hämtar den aktuella listan över problem klassificering för en Azure-tjänst. Du kan använda tjänst-och problem klassificerings-GUID för att skapa ett nytt support ärende med hjälp av New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Hjälp-cmdlet för att skapa ett profil objekt för support kontakt. Du kan använda det här objektet för New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Skapar ett nytt Azure support-biljett. Denna åtgärd är förenligt med sidan för Azure [New Support Request](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Hämtar listan med support biljetter. Du kan få fullständiga support uppgifter efter biljett namn eller filtrera support biljetter efter *status* eller *CreatedDate*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Uppdatera support ärendets allvarlighets grad, status eller kund kontakt uppgifter.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Får ett support ärende. Du kan också filtrera support meddelande kommunikation via *CreatedDate*   eller *CommunicationType*. 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Lägger till en ny kund kommunikation till en Azure support-biljett. 



