---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571747"
---
# <span data-ttu-id="a4b5c-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a4b5c-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="a4b5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b5c-103">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a4b5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4b5c-104">SYNTAX</span></span>

### <span data-ttu-id="a4b5c-105">ListByIdInTenant (standard)</span><span class="sxs-lookup"><span data-stu-id="a4b5c-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="a4b5c-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="a4b5c-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4b5c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4b5c-107">DESCRIPTION</span></span>
<span data-ttu-id="a4b5c-108">Get-AzureRmSubscription cmdlet får prenumerations-ID, prenumerations namn och hem klient organisation för abonnemang som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a4b5c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4b5c-109">EXAMPLES</span></span>

### <span data-ttu-id="a4b5c-110">Exempel 1: Hämta alla prenumerationer i alla innehavare</span><span class="sxs-lookup"><span data-stu-id="a4b5c-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a4b5c-111">Det här kommandot får alla prenumerationer i alla innehavare som är godkända för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a4b5c-112">Exempel 2: Hämta alla prenumerationer för en viss klient organisation</span><span class="sxs-lookup"><span data-stu-id="a4b5c-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a4b5c-113">Lista alla prenumerationer i den klient organisation som är behörig för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a4b5c-114">Exempel 3: Hämta alla prenumerationer i den aktuella innehavaren</span><span class="sxs-lookup"><span data-stu-id="a4b5c-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a4b5c-115">Det här kommandot får alla prenumerationer i den aktuella innehavaren som är behörig för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a4b5c-116">Exempel 4: ändra den aktuella kontexten till att använda ett visst abonnemang</span><span class="sxs-lookup"><span data-stu-id="a4b5c-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a4b5c-117">Det här kommandot hämtar det angivna abonnemanget och anger sedan den aktuella kontexten för att använda den.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="a4b5c-118">Alla efterföljande cmdlets i den här sessionen använder det nya abonnemanget (contoso-abonnemang 1) som standard.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a4b5c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4b5c-119">PARAMETERS</span></span>

### <span data-ttu-id="a4b5c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4b5c-120">-SubscriptionId</span></span>
<span data-ttu-id="a4b5c-121">Anger ID för det abonnemang du vill ha.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5c-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a4b5c-122">-SubscriptionName</span></span>
<span data-ttu-id="a4b5c-123">Anger namnet på den prenumeration du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5c-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a4b5c-124">-TenantId</span></span>
<span data-ttu-id="a4b5c-125">Anger ID för den klient organisation som innehåller prenumerationer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b5c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b5c-126">CommonParameters</span></span>
<span data-ttu-id="a4b5c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b5c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b5c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b5c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b5c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4b5c-129">INPUTS</span></span>

## <span data-ttu-id="a4b5c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4b5c-130">OUTPUTS</span></span>

### <span data-ttu-id="a4b5c-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a4b5c-131">PSAzureSubscription</span></span>

## <span data-ttu-id="a4b5c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4b5c-132">NOTES</span></span>

## <span data-ttu-id="a4b5c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4b5c-133">RELATED LINKS</span></span>

