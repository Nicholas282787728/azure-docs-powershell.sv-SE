---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921940"
---
# <span data-ttu-id="e4a0b-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e4a0b-101">New-AzsSubscription</span></span>

## <span data-ttu-id="e4a0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a0b-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="e4a0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4a0b-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e4a0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a0b-106">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="e4a0b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a0b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e4a0b-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="e4a0b-109">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-109">Create a subscription.</span></span>

## <span data-ttu-id="e4a0b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4a0b-110">PARAMETERS</span></span>

### <span data-ttu-id="e4a0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a0b-111">-DefaultProfile</span></span>
<span data-ttu-id="e4a0b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4a0b-113">-DisplayName</span></span>
<span data-ttu-id="e4a0b-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e4a0b-115">-Id</span></span>
<span data-ttu-id="e4a0b-116">Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e4a0b-117">-OfferId</span></span>
<span data-ttu-id="e4a0b-118">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-119">-State</span><span class="sxs-lookup"><span data-stu-id="e4a0b-119">-State</span></span>
<span data-ttu-id="e4a0b-120">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4a0b-121">-SubscriptionId</span></span>
<span data-ttu-id="e4a0b-122">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-123">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e4a0b-123">-TenantId</span></span>
<span data-ttu-id="e4a0b-124">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4a0b-125">-Confirm</span></span>
<span data-ttu-id="e4a0b-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a0b-127">-WhatIf</span></span>
<span data-ttu-id="e4a0b-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a0b-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4a0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a0b-130">CommonParameters</span></span>
<span data-ttu-id="e4a0b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a0b-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4a0b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a0b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4a0b-133">INPUTS</span></span>

## <span data-ttu-id="e4a0b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4a0b-134">OUTPUTS</span></span>

### <span data-ttu-id="e4a0b-135">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="e4a0b-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="e4a0b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4a0b-136">NOTES</span></span>

## <span data-ttu-id="e4a0b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4a0b-137">RELATED LINKS</span></span>

