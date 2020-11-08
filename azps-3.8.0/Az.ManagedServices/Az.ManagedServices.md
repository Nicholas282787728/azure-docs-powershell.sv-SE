---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091928"
---
# <span data-ttu-id="7a96c-101">Modulen AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7a96c-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="7a96c-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="7a96c-102">Description</span></span>
<span data-ttu-id="7a96c-103">Den här funktionen används av kunder med hanterade tjänste leverantörer (MSPs).</span><span class="sxs-lookup"><span data-stu-id="7a96c-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="7a96c-104">Kunderna ger en MSP möjlighet att hantera sin prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7a96c-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="7a96c-105">Förutom att bevilja åtkomst kan kunden också ta bort åtkomst eller Visa befintliga åtkomst delegeringar.</span><span class="sxs-lookup"><span data-stu-id="7a96c-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="7a96c-106">MSPs kan visa en lista över kunder som har beviljat dem åtkomst till prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="7a96c-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="7a96c-107">Det finns två objekt i den här processen: en registrerings definition som identifierar MSP och roll definitioner som beviljats till MSP.</span><span class="sxs-lookup"><span data-stu-id="7a96c-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="7a96c-108">En MSP kan även definiera det här objektet med hjälp av en marknads plats för hantering med åtkomst tilldelningar som associerar en prenumeration med definitionen.</span><span class="sxs-lookup"><span data-stu-id="7a96c-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="7a96c-109">AZ. ManagedServices-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7a96c-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="7a96c-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a96c-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="7a96c-111">Hämtar en lista över registrerings tilldelningarna.</span><span class="sxs-lookup"><span data-stu-id="7a96c-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="7a96c-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a96c-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="7a96c-113">Hämtar en lista över registrerings definitionerna.</span><span class="sxs-lookup"><span data-stu-id="7a96c-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="7a96c-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a96c-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="7a96c-115">Skapar en registrerings tilldelning.</span><span class="sxs-lookup"><span data-stu-id="7a96c-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="7a96c-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a96c-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="7a96c-117">Skapar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="7a96c-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="7a96c-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a96c-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="7a96c-119">Tar bort registrerings tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="7a96c-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="7a96c-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a96c-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="7a96c-121">Tar bort registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="7a96c-121">Deletes the registration definition.</span></span>

