---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cddc7e5b3e0d9c7181248e024982293d1418e680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754940"
---
# <span data-ttu-id="88621-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="88621-101">New-AzsPlan</span></span>

## <span data-ttu-id="88621-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88621-102">SYNOPSIS</span></span>
<span data-ttu-id="88621-103">Skapar en ny plan</span><span class="sxs-lookup"><span data-stu-id="88621-103">Creates a new plan</span></span>

## <span data-ttu-id="88621-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88621-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88621-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88621-105">DESCRIPTION</span></span>
<span data-ttu-id="88621-106">Skapar en ny plan</span><span class="sxs-lookup"><span data-stu-id="88621-106">Creates a new plan</span></span>

## <span data-ttu-id="88621-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88621-107">EXAMPLES</span></span>

### <span data-ttu-id="88621-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="88621-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="88621-109">Skapar en ny plan</span><span class="sxs-lookup"><span data-stu-id="88621-109">Creates a new plan</span></span>

## <span data-ttu-id="88621-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88621-110">PARAMETERS</span></span>

### <span data-ttu-id="88621-111">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="88621-111">-Description</span></span>
<span data-ttu-id="88621-112">Beskrivning av planen.</span><span class="sxs-lookup"><span data-stu-id="88621-112">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="88621-113">-DisplayName</span></span>
<span data-ttu-id="88621-114">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="88621-114">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="88621-115">-ExternalReferenceId</span></span>
<span data-ttu-id="88621-116">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="88621-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="88621-117">-Location</span></span>
<span data-ttu-id="88621-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="88621-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="88621-119">-Name</span></span>
<span data-ttu-id="88621-120">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="88621-120">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="88621-121">-QuotaIds</span></span>
<span data-ttu-id="88621-122">Kvot-ID: n under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="88621-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88621-123">-ResourceGroupName</span></span>
<span data-ttu-id="88621-124">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="88621-124">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="88621-125">-SkuIds</span></span>
<span data-ttu-id="88621-126">SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="88621-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="88621-127">-SubscriptionCount</span></span>
<span data-ttu-id="88621-128">Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="88621-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88621-129">-Confirm</span></span>
<span data-ttu-id="88621-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88621-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88621-131">-WhatIf</span></span>
<span data-ttu-id="88621-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88621-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88621-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88621-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88621-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88621-134">CommonParameters</span></span>
<span data-ttu-id="88621-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88621-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88621-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88621-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88621-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88621-137">INPUTS</span></span>

## <span data-ttu-id="88621-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88621-138">OUTPUTS</span></span>

### <span data-ttu-id="88621-139">Microsoft. AzureStack. Management. abonnemang. admin. Models. plan</span><span class="sxs-lookup"><span data-stu-id="88621-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="88621-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88621-140">NOTES</span></span>

## <span data-ttu-id="88621-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88621-141">RELATED LINKS</span></span>
