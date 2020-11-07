---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921911"
---
# <span data-ttu-id="595f4-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="595f4-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="595f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="595f4-102">SYNOPSIS</span></span>
<span data-ttu-id="595f4-103">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="595f4-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="595f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="595f4-104">SYNTAX</span></span>

### <span data-ttu-id="595f4-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="595f4-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595f4-106">ID</span><span class="sxs-lookup"><span data-stu-id="595f4-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="595f4-107">DESCRIPTION</span></span>
<span data-ttu-id="595f4-108">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="595f4-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="595f4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="595f4-109">EXAMPLES</span></span>

### <span data-ttu-id="595f4-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="595f4-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="595f4-111">ProvisioningState: lyckades</span><span class="sxs-lookup"><span data-stu-id="595f4-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="595f4-112">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="595f4-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="595f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="595f4-113">PARAMETERS</span></span>

### <span data-ttu-id="595f4-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="595f4-114">-Name</span></span>
<span data-ttu-id="595f4-115">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="595f4-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="595f4-116">-Location</span></span>
<span data-ttu-id="595f4-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="595f4-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="595f4-119">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="595f4-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="595f4-120">-ResourceId</span></span>
<span data-ttu-id="595f4-121">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="595f4-121">Scale unit node resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="595f4-122">-AsJob</span></span>
<span data-ttu-id="595f4-123">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="595f4-123">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="595f4-124">-Force</span></span>
<span data-ttu-id="595f4-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="595f4-125">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595f4-126">-WhatIf</span></span>
<span data-ttu-id="595f4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="595f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595f4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="595f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595f4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="595f4-129">-Confirm</span></span>
<span data-ttu-id="595f4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="595f4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595f4-131">CommonParameters</span></span>
<span data-ttu-id="595f4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595f4-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595f4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595f4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="595f4-134">INPUTS</span></span>

## <span data-ttu-id="595f4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="595f4-135">OUTPUTS</span></span>

## <span data-ttu-id="595f4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="595f4-136">NOTES</span></span>

## <span data-ttu-id="595f4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="595f4-137">RELATED LINKS</span></span>
