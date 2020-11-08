---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099879"
---
# <span data-ttu-id="1b096-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1b096-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1b096-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b096-102">SYNOPSIS</span></span>
<span data-ttu-id="1b096-103">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1b096-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1b096-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b096-104">SYNTAX</span></span>

### <span data-ttu-id="1b096-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="1b096-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b096-106">ID</span><span class="sxs-lookup"><span data-stu-id="1b096-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b096-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b096-107">DESCRIPTION</span></span>
<span data-ttu-id="1b096-108">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1b096-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1b096-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b096-109">EXAMPLES</span></span>

### <span data-ttu-id="1b096-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="1b096-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="1b096-111">Stoppa underhålls läget på en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1b096-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="1b096-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b096-112">PARAMETERS</span></span>

### <span data-ttu-id="1b096-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b096-113">-Name</span></span>
<span data-ttu-id="1b096-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1b096-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1b096-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="1b096-115">-Location</span></span>
<span data-ttu-id="1b096-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1b096-116">Location of the resource.</span></span>

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

### <span data-ttu-id="1b096-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b096-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b096-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1b096-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1b096-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b096-119">-ResourceId</span></span>
<span data-ttu-id="1b096-120">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="1b096-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1b096-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b096-121">-AsJob</span></span>
<span data-ttu-id="1b096-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="1b096-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1b096-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1b096-123">-Force</span></span>
<span data-ttu-id="1b096-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1b096-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1b096-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b096-125">-WhatIf</span></span>
<span data-ttu-id="1b096-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b096-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b096-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b096-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b096-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b096-128">-Confirm</span></span>
<span data-ttu-id="1b096-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b096-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b096-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b096-130">CommonParameters</span></span>
<span data-ttu-id="1b096-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b096-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b096-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b096-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b096-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b096-133">INPUTS</span></span>

## <span data-ttu-id="1b096-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b096-134">OUTPUTS</span></span>

## <span data-ttu-id="1b096-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b096-135">NOTES</span></span>

## <span data-ttu-id="1b096-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b096-136">RELATED LINKS</span></span>
