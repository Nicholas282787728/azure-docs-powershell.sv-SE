---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100232"
---
# <span data-ttu-id="945d8-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="945d8-101">Set-AzsPlan</span></span>

## <span data-ttu-id="945d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="945d8-102">SYNOPSIS</span></span>
<span data-ttu-id="945d8-103">Uppdaterar angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="945d8-103">Updates the specified plan</span></span>

## <span data-ttu-id="945d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="945d8-104">SYNTAX</span></span>

### <span data-ttu-id="945d8-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="945d8-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="945d8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="945d8-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="945d8-107">ID</span><span class="sxs-lookup"><span data-stu-id="945d8-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="945d8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="945d8-108">DESCRIPTION</span></span>
<span data-ttu-id="945d8-109">Uppdaterar angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="945d8-109">Updates the specified plan</span></span>

## <span data-ttu-id="945d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="945d8-110">EXAMPLES</span></span>

### <span data-ttu-id="945d8-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="945d8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="945d8-112">Uppdaterar angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="945d8-112">Updates the specified plan</span></span>

## <span data-ttu-id="945d8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="945d8-113">PARAMETERS</span></span>

### <span data-ttu-id="945d8-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="945d8-114">-Description</span></span>
<span data-ttu-id="945d8-115">Beskrivning av planen.</span><span class="sxs-lookup"><span data-stu-id="945d8-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="945d8-116">-DisplayName</span></span>
<span data-ttu-id="945d8-117">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="945d8-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="945d8-118">-ExternalReferenceId</span></span>
<span data-ttu-id="945d8-119">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="945d8-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="945d8-120">-InputObject</span></span>
<span data-ttu-id="945d8-121">Indatavärdet av typen Microsoft. AzureStack. Management. abonnemang. admin. Models. plan.</span><span class="sxs-lookup"><span data-stu-id="945d8-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="945d8-122">-Location</span></span>
<span data-ttu-id="945d8-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="945d8-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="945d8-124">-Name</span></span>
<span data-ttu-id="945d8-125">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="945d8-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="945d8-126">-QuotaIds</span></span>
<span data-ttu-id="945d8-127">Kvot-ID: n under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="945d8-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="945d8-129">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="945d8-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="945d8-130">-ResourceId</span></span>
<span data-ttu-id="945d8-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="945d8-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="945d8-132">-SkuIds</span></span>
<span data-ttu-id="945d8-133">SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="945d8-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="945d8-134">-SubscriptionCount</span></span>
<span data-ttu-id="945d8-135">Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="945d8-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945d8-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="945d8-136">-Confirm</span></span>
<span data-ttu-id="945d8-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="945d8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="945d8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="945d8-138">-WhatIf</span></span>
<span data-ttu-id="945d8-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="945d8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="945d8-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="945d8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="945d8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945d8-141">CommonParameters</span></span>
<span data-ttu-id="945d8-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945d8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945d8-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945d8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945d8-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="945d8-144">INPUTS</span></span>

## <span data-ttu-id="945d8-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="945d8-145">OUTPUTS</span></span>

### <span data-ttu-id="945d8-146">Microsoft. AzureStack. Management. abonnemang. admin. Models. plan</span><span class="sxs-lookup"><span data-stu-id="945d8-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="945d8-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="945d8-147">NOTES</span></span>

## <span data-ttu-id="945d8-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="945d8-148">RELATED LINKS</span></span>

