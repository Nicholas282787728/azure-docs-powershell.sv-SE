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
# <span data-ttu-id="8983a-101">AZ. support-modul</span><span class="sxs-lookup"><span data-stu-id="8983a-101">Az.Support Module</span></span>
## <span data-ttu-id="8983a-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="8983a-102">Description</span></span>
<span data-ttu-id="8983a-103">Ämnena i det här avsnittet dokumenterar Azure PowerShell-cmdletar för att skapa och hantera Azure support biljetter i ramverket Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="8983a-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="8983a-104">Det finns cmdlets i Microsoft. Azure. commands. support-namnrymd</span><span class="sxs-lookup"><span data-stu-id="8983a-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="8983a-105">AZ. support-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8983a-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="8983a-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="8983a-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="8983a-107">Hämtar den aktuella listan med Azure-tjänster som stöder support.</span><span class="sxs-lookup"><span data-stu-id="8983a-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="8983a-108">Varje Azure-tjänst har sin egen uppsättning kategorier som kallas problem klassificering.</span><span class="sxs-lookup"><span data-stu-id="8983a-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="8983a-109">Hämta den aktuella listan över problem klassificering för en tjänst med Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="8983a-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="8983a-110">Du kan använda tjänst-och problem klassificerings-GUID för att skapa ett nytt support ärende med hjälp av New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8983a-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="8983a-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="8983a-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="8983a-112">Hämtar den aktuella listan över problem klassificering för en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="8983a-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="8983a-113">Du kan använda tjänst-och problem klassificerings-GUID för att skapa ett nytt support ärende med hjälp av New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8983a-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="8983a-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="8983a-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="8983a-115">Hjälp-cmdlet för att skapa ett profil objekt för support kontakt.</span><span class="sxs-lookup"><span data-stu-id="8983a-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="8983a-116">Du kan använda det här objektet för New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8983a-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="8983a-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8983a-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="8983a-118">Skapar ett nytt Azure support-biljett.</span><span class="sxs-lookup"><span data-stu-id="8983a-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="8983a-119">Denna åtgärd är förenligt med sidan för Azure [New Support Request](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span><span class="sxs-lookup"><span data-stu-id="8983a-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="8983a-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8983a-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="8983a-121">Hämtar listan med support biljetter.</span><span class="sxs-lookup"><span data-stu-id="8983a-121">Gets the list of support tickets.</span></span> <span data-ttu-id="8983a-122">Du kan få fullständiga support uppgifter efter biljett namn eller filtrera support biljetter efter *status* eller *CreatedDate*.</span><span class="sxs-lookup"><span data-stu-id="8983a-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="8983a-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8983a-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="8983a-124">Uppdatera support ärendets allvarlighets grad, status eller kund kontakt uppgifter.</span><span class="sxs-lookup"><span data-stu-id="8983a-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="8983a-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8983a-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="8983a-126">Får ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="8983a-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="8983a-127">Du kan också filtrera support meddelande kommunikation via *CreatedDate*   eller *CommunicationType*.</span><span class="sxs-lookup"><span data-stu-id="8983a-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="8983a-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="8983a-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="8983a-129">Lägger till en ny kund kommunikation till en Azure support-biljett.</span><span class="sxs-lookup"><span data-stu-id="8983a-129">Adds a new customer communication to an Azure support ticket.</span></span> 



