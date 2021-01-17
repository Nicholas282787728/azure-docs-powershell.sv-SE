---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415483"
---
# <span data-ttu-id="0940d-101">Modulen AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0940d-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="0940d-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="0940d-102">Description</span></span>
<span data-ttu-id="0940d-103">Den här funktionen används av kunder med hanterade tjänste leverantörer (MSPs).</span><span class="sxs-lookup"><span data-stu-id="0940d-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="0940d-104">Kunderna ger en MSP möjlighet att hantera deras abonnemang eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0940d-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="0940d-105">Förutom att bevilja åtkomst kan kunden också ta bort åtkomst eller Visa befintlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="0940d-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="0940d-106">MSPs kan visa en lista över kunder som har beviljat dem åtkomst till prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0940d-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="0940d-107">Det finns två objekt i den här processen: en registrerings definition som identifierar MSP och roll definitioner som beviljats till MSP-användare.</span><span class="sxs-lookup"><span data-stu-id="0940d-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="0940d-108">En MSP kan även definiera det här objektet med hjälp av en marknads plats för hantering med åtkomst tilldelningar som associerar en prenumeration med definitionen.</span><span class="sxs-lookup"><span data-stu-id="0940d-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="0940d-109">AZ. ManagedServices-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0940d-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="0940d-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0940d-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="0940d-111">Hämtar en specifik registrerings uppgift eller en lista med registrerings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="0940d-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="0940d-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0940d-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="0940d-113">Hämtar en särskild registrerings definition eller en lista med registrerings definitioner.</span><span class="sxs-lookup"><span data-stu-id="0940d-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="0940d-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0940d-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="0940d-115">Skapar eller uppdaterar en registrering.</span><span class="sxs-lookup"><span data-stu-id="0940d-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="0940d-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0940d-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="0940d-117">Skapar eller uppdaterar en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="0940d-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="0940d-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0940d-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="0940d-119">Tar bort en registrerings tilldelning.</span><span class="sxs-lookup"><span data-stu-id="0940d-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="0940d-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0940d-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="0940d-121">Tar bort en registrerings definition.</span><span class="sxs-lookup"><span data-stu-id="0940d-121">Removes a registration definition.</span></span>
