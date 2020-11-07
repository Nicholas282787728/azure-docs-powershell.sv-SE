---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93743314"
---
# <span data-ttu-id="8c166-101">Modulen AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8c166-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="8c166-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="8c166-102">Description</span></span>
<span data-ttu-id="8c166-103">Den här funktionen används av kunder med hanterade tjänste leverantörer (MSPs).</span><span class="sxs-lookup"><span data-stu-id="8c166-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="8c166-104">Kunderna ger en MSP möjlighet att hantera sin prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8c166-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="8c166-105">Förutom att bevilja åtkomst kan kunden också ta bort åtkomst eller Visa befintliga åtkomst delegeringar.</span><span class="sxs-lookup"><span data-stu-id="8c166-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="8c166-106">MSPs kan visa en lista över kunder som har beviljat dem åtkomst till prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="8c166-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="8c166-107">Det finns två objekt i den här processen: en registrerings definition som identifierar MSP och roll definitioner som beviljats till MSP.</span><span class="sxs-lookup"><span data-stu-id="8c166-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="8c166-108">En MSP kan även definiera det här objektet med hjälp av en marknads plats för hantering med åtkomst tilldelningar som associerar en prenumeration med definitionen.</span><span class="sxs-lookup"><span data-stu-id="8c166-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="8c166-109">AZ. ManagedServices-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8c166-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="8c166-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8c166-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="8c166-111">Hämtar en lista över registrerings tilldelningarna.</span><span class="sxs-lookup"><span data-stu-id="8c166-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="8c166-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8c166-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="8c166-113">Hämtar en lista över registrerings definitionerna.</span><span class="sxs-lookup"><span data-stu-id="8c166-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="8c166-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8c166-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="8c166-115">Skapar en registrerings tilldelning.</span><span class="sxs-lookup"><span data-stu-id="8c166-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="8c166-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8c166-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="8c166-117">Skapar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="8c166-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="8c166-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8c166-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="8c166-119">Tar bort registrerings tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="8c166-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="8c166-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8c166-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="8c166-121">Tar bort registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="8c166-121">Deletes the registration definition.</span></span>

