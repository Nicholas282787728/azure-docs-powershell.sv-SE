---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921386"
---
# <span data-ttu-id="50954-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="50954-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="50954-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50954-102">SYNOPSIS</span></span>
<span data-ttu-id="50954-103">Starta underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="50954-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="50954-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50954-104">SYNTAX</span></span>

### <span data-ttu-id="50954-105">Inaktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="50954-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50954-106">ID</span><span class="sxs-lookup"><span data-stu-id="50954-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50954-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50954-107">DESCRIPTION</span></span>
<span data-ttu-id="50954-108">Starta underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="50954-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="50954-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50954-109">EXAMPLES</span></span>

### <span data-ttu-id="50954-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="50954-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="50954-111">Aktivera underhålls läge för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="50954-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="50954-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50954-112">PARAMETERS</span></span>

### <span data-ttu-id="50954-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="50954-113">-Name</span></span>
<span data-ttu-id="50954-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="50954-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="50954-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="50954-115">-Location</span></span>
<span data-ttu-id="50954-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="50954-116">Location of the resource.</span></span>

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

### <span data-ttu-id="50954-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50954-117">-ResourceGroupName</span></span>
<span data-ttu-id="50954-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="50954-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="50954-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50954-119">-ResourceId</span></span>
<span data-ttu-id="50954-120">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="50954-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="50954-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50954-121">-AsJob</span></span>
<span data-ttu-id="50954-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="50954-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="50954-123">-Force</span><span class="sxs-lookup"><span data-stu-id="50954-123">-Force</span></span>
<span data-ttu-id="50954-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50954-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="50954-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50954-125">-WhatIf</span></span>
<span data-ttu-id="50954-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50954-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50954-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50954-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50954-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50954-128">-Confirm</span></span>
<span data-ttu-id="50954-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50954-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50954-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50954-130">CommonParameters</span></span>
<span data-ttu-id="50954-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50954-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50954-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50954-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50954-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50954-133">INPUTS</span></span>

## <span data-ttu-id="50954-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50954-134">OUTPUTS</span></span>

## <span data-ttu-id="50954-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50954-135">NOTES</span></span>

## <span data-ttu-id="50954-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50954-136">RELATED LINKS</span></span>
