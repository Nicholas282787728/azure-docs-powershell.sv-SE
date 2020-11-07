---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921908"
---
# <span data-ttu-id="9c441-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9c441-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9c441-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c441-102">SYNOPSIS</span></span>
<span data-ttu-id="9c441-103">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="9c441-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="9c441-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c441-104">SYNTAX</span></span>

### <span data-ttu-id="9c441-105">Stopp (standard)</span><span class="sxs-lookup"><span data-stu-id="9c441-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c441-106">ID</span><span class="sxs-lookup"><span data-stu-id="9c441-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c441-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c441-107">DESCRIPTION</span></span>
<span data-ttu-id="9c441-108">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="9c441-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="9c441-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c441-109">EXAMPLES</span></span>

### <span data-ttu-id="9c441-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="9c441-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="9c441-111">Avsluta en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="9c441-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="9c441-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="9c441-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="9c441-113">Stänga av en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9c441-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="9c441-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c441-114">PARAMETERS</span></span>

### <span data-ttu-id="9c441-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c441-115">-Name</span></span>
<span data-ttu-id="9c441-116">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9c441-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c441-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c441-117">-Location</span></span>
<span data-ttu-id="9c441-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="9c441-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c441-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c441-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c441-120">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="9c441-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c441-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c441-121">-ResourceId</span></span>
<span data-ttu-id="9c441-122">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="9c441-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="9c441-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="9c441-123">-Shutdown</span></span>
<span data-ttu-id="9c441-124">Om du har avaktiverat Stäng av noden Scale Unit i övrigt stänger du av noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9c441-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="9c441-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c441-125">-AsJob</span></span>
<span data-ttu-id="9c441-126">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="9c441-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9c441-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9c441-127">-Force</span></span>
<span data-ttu-id="9c441-128">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9c441-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9c441-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c441-129">-WhatIf</span></span>
<span data-ttu-id="9c441-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c441-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c441-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c441-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c441-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c441-132">-Confirm</span></span>
<span data-ttu-id="9c441-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c441-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c441-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c441-134">CommonParameters</span></span>
<span data-ttu-id="9c441-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c441-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c441-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c441-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c441-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c441-137">INPUTS</span></span>

## <span data-ttu-id="9c441-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c441-138">OUTPUTS</span></span>

## <span data-ttu-id="9c441-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c441-139">NOTES</span></span>

## <span data-ttu-id="9c441-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c441-140">RELATED LINKS</span></span>
