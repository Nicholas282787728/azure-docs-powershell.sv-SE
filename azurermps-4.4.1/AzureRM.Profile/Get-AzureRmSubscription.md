---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577543"
---
# <span data-ttu-id="6a491-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="6a491-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="6a491-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a491-102">SYNOPSIS</span></span>
<span data-ttu-id="6a491-103">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="6a491-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a491-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a491-104">SYNTAX</span></span>

### <span data-ttu-id="6a491-105">ListByIdInTenant (standard)</span><span class="sxs-lookup"><span data-stu-id="6a491-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a491-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="6a491-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a491-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a491-107">DESCRIPTION</span></span>
<span data-ttu-id="6a491-108">Get-AzureRmSubscription cmdlet får prenumerations-ID, prenumerations namn och hem klient organisation för abonnemang som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="6a491-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="6a491-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a491-109">EXAMPLES</span></span>

### <span data-ttu-id="6a491-110">Exempel 1: Hämta alla prenumerationer i alla innehavare</span><span class="sxs-lookup"><span data-stu-id="6a491-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="6a491-111">Det här kommandot får alla prenumerationer i alla innehavare som är godkända för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="6a491-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="6a491-112">Exempel 2: Hämta alla prenumerationer för en viss klient organisation</span><span class="sxs-lookup"><span data-stu-id="6a491-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="6a491-113">Lista alla prenumerationer i den klient organisation som är behörig för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="6a491-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="6a491-114">Exempel 3: Hämta alla prenumerationer i den aktuella innehavaren</span><span class="sxs-lookup"><span data-stu-id="6a491-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="6a491-115">Det här kommandot får alla prenumerationer i den aktuella innehavaren som är behörig för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="6a491-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="6a491-116">Exempel 4: ändra den aktuella kontexten till att använda ett visst abonnemang</span><span class="sxs-lookup"><span data-stu-id="6a491-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="6a491-117">Det här kommandot hämtar det angivna abonnemanget och anger sedan den aktuella kontexten för att använda den.</span><span class="sxs-lookup"><span data-stu-id="6a491-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="6a491-118">Alla efterföljande cmdlets i den här sessionen använder det nya abonnemanget (contoso-abonnemang 1) som standard.</span><span class="sxs-lookup"><span data-stu-id="6a491-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="6a491-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a491-119">PARAMETERS</span></span>

### <span data-ttu-id="6a491-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a491-120">-DefaultProfile</span></span>
<span data-ttu-id="6a491-121">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6a491-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a491-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a491-122">-SubscriptionId</span></span>
<span data-ttu-id="6a491-123">Anger ID för det abonnemang du vill ha.</span><span class="sxs-lookup"><span data-stu-id="6a491-123">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a491-124">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6a491-124">-SubscriptionName</span></span>
<span data-ttu-id="6a491-125">Anger namnet på den prenumeration du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="6a491-125">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a491-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6a491-126">-TenantId</span></span>
<span data-ttu-id="6a491-127">Anger ID för den klient organisation som innehåller prenumerationer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6a491-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a491-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a491-128">CommonParameters</span></span>
<span data-ttu-id="6a491-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a491-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a491-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a491-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a491-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a491-131">INPUTS</span></span>

## <span data-ttu-id="6a491-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a491-132">OUTPUTS</span></span>

### <span data-ttu-id="6a491-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6a491-133">PSAzureSubscription</span></span>

## <span data-ttu-id="6a491-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a491-134">NOTES</span></span>

## <span data-ttu-id="6a491-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a491-135">RELATED LINKS</span></span>

