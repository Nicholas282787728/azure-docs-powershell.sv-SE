---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921722"
---
# <span data-ttu-id="72e7a-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="72e7a-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="72e7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="72e7a-103">Starta underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="72e7a-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="72e7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e7a-104">SYNTAX</span></span>

### <span data-ttu-id="72e7a-105">Inaktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="72e7a-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e7a-106">ID</span><span class="sxs-lookup"><span data-stu-id="72e7a-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e7a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="72e7a-108">Starta underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="72e7a-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="72e7a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="72e7a-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="72e7a-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="72e7a-111">Aktivera underhålls läge för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="72e7a-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="72e7a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e7a-112">PARAMETERS</span></span>

### <span data-ttu-id="72e7a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="72e7a-113">-Name</span></span>
<span data-ttu-id="72e7a-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="72e7a-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e7a-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="72e7a-115">-Location</span></span>
<span data-ttu-id="72e7a-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="72e7a-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e7a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e7a-117">-ResourceGroupName</span></span>
<span data-ttu-id="72e7a-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="72e7a-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e7a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e7a-119">-ResourceId</span></span>
<span data-ttu-id="72e7a-120">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="72e7a-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="72e7a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72e7a-121">-AsJob</span></span>
<span data-ttu-id="72e7a-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="72e7a-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="72e7a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="72e7a-123">-Force</span></span>
<span data-ttu-id="72e7a-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="72e7a-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="72e7a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e7a-125">-WhatIf</span></span>
<span data-ttu-id="72e7a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72e7a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e7a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72e7a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e7a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72e7a-128">-Confirm</span></span>
<span data-ttu-id="72e7a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72e7a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e7a-130">CommonParameters</span></span>
<span data-ttu-id="72e7a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e7a-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e7a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e7a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e7a-133">INPUTS</span></span>

## <span data-ttu-id="72e7a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e7a-134">OUTPUTS</span></span>

## <span data-ttu-id="72e7a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e7a-135">NOTES</span></span>

## <span data-ttu-id="72e7a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e7a-136">RELATED LINKS</span></span>