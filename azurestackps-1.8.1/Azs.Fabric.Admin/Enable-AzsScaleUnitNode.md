---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921913"
---
# <span data-ttu-id="e6e28-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e6e28-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e6e28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6e28-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e28-103">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e6e28-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e6e28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6e28-104">SYNTAX</span></span>

### <span data-ttu-id="e6e28-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="e6e28-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e28-106">ID</span><span class="sxs-lookup"><span data-stu-id="e6e28-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6e28-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e28-108">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e6e28-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e6e28-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6e28-109">EXAMPLES</span></span>

### <span data-ttu-id="e6e28-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="e6e28-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="e6e28-111">Stoppa underhålls läget på en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e6e28-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="e6e28-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6e28-112">PARAMETERS</span></span>

### <span data-ttu-id="e6e28-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6e28-113">-Name</span></span>
<span data-ttu-id="e6e28-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e6e28-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e28-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="e6e28-115">-Location</span></span>
<span data-ttu-id="e6e28-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e6e28-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e28-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6e28-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="e6e28-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e28-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e28-119">-ResourceId</span></span>
<span data-ttu-id="e6e28-120">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="e6e28-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e6e28-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e28-121">-AsJob</span></span>
<span data-ttu-id="e6e28-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="e6e28-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e6e28-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e6e28-123">-Force</span></span>
<span data-ttu-id="e6e28-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e6e28-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e6e28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e28-125">-WhatIf</span></span>
<span data-ttu-id="e6e28-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6e28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e28-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6e28-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e28-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6e28-128">-Confirm</span></span>
<span data-ttu-id="e6e28-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6e28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e28-130">CommonParameters</span></span>
<span data-ttu-id="e6e28-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e28-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e28-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e28-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6e28-133">INPUTS</span></span>

## <span data-ttu-id="e6e28-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6e28-134">OUTPUTS</span></span>

## <span data-ttu-id="e6e28-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6e28-135">NOTES</span></span>

## <span data-ttu-id="e6e28-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6e28-136">RELATED LINKS</span></span>