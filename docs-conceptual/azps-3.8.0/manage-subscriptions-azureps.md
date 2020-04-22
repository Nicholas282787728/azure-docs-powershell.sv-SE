---
title: Hantera Azure-prenumerationer med Azure PowerShell
description: Hantera Azure-prenumerationer med Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740175"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="a71df-103">Använda flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="a71df-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="a71df-104">De flesta Azure-användare har bara en enstaka prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a71df-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="a71df-105">Om du däremot är en del av mer än en organisation eller om din organisation har delat upp åtkomst till vissa resurser i grupper kan du ha flera prenumerationer i Azure.</span><span class="sxs-lookup"><span data-stu-id="a71df-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="a71df-106">CLI har stöd för att välja en prenumeration både globalt och per kommando.</span><span class="sxs-lookup"><span data-stu-id="a71df-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="a71df-107">Detaljerad information om prenumerationer, fakturering och kostnadshantering finns i [dokumentationen om fakturering och kostnadshantering](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="a71df-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="a71df-108">Klienter, användare och prenumerationer</span><span class="sxs-lookup"><span data-stu-id="a71df-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="a71df-109">Du kanske funderar över skillnaden mellan klienter, användare och prenumerationer i Azure.</span><span class="sxs-lookup"><span data-stu-id="a71df-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="a71df-110">En _klient_ är den Azure Active Directory-enhet som omfattar hela organisationen.</span><span class="sxs-lookup"><span data-stu-id="a71df-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="a71df-111">Klienten har minst en _prenumeration_ och _användare_.</span><span class="sxs-lookup"><span data-stu-id="a71df-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="a71df-112">En användare är en person och är endast associerad till en klient, vilken är organisationen som användaren tillhör.</span><span class="sxs-lookup"><span data-stu-id="a71df-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="a71df-113">Användare är de konton som loggar in på Azure för att skapa, hantera och använda resurser.</span><span class="sxs-lookup"><span data-stu-id="a71df-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="a71df-114">En användare kan ha åtkomst till flera _prenumerationer_, som är avtal med Microsoft för användning av molntjänster, inklusive Azure.</span><span class="sxs-lookup"><span data-stu-id="a71df-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="a71df-115">Varje resurs är associerad med en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a71df-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="a71df-116">Om du vill veta mer om skillnaderna mellan klienter, användare och prenumerationer kan du läsa [ordlistan för molnterminologi i Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="a71df-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="a71df-117">Om du vill lära dig att lägga till en ny prenumeration till din Azure Active Directory-klient läser du [Så här lägger du till en prenumeration i din Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="a71df-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="a71df-118">Information om hur du loggar in på en specifik klient finns i [Logga in med Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="a71df-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="a71df-119">Ändra den aktiva prenumerationen</span><span class="sxs-lookup"><span data-stu-id="a71df-119">Change the active subscription</span></span>

<span data-ttu-id="a71df-120">Du måste ändra prenumerationen som är associerad med den aktuella Azure-sessionen för att få tillgång till resurserna för en prenumeration i Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a71df-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="a71df-121">Du gör detta genom att ändra den aktiva sessionens kontext, det vill säga informationen om vilken klientorganisation, prenumeration, samt användar-cmdletar som ska köras.</span><span class="sxs-lookup"><span data-stu-id="a71df-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="a71df-122">Om du vill ändra prenumeration måste ett Azure PowerShell-kontextobjekt först hämtas med [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) och sedan måste den nuvarande kontexten ändras med [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="a71df-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="a71df-123">Följande exempel visar hur du skaffar en prenumeration i den aktiva klientorganisationen och ställer in den som den aktiva sessionen:</span><span class="sxs-lookup"><span data-stu-id="a71df-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="a71df-124">Läs informationen om att [spara autentiseringsuppgifter med Azure PowerShell-kontexter](context-persistence.md) för att lära dig mer om Azure PowerShell-kontexter, inklusive hur du sparar dem och snabbt växlar mellan dem för att arbeta med flera prenumerationer på ett enkelt sätt.</span><span class="sxs-lookup"><span data-stu-id="a71df-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
