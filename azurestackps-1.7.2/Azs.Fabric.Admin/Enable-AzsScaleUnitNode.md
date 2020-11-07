---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921228"
---
# <span data-ttu-id="2022c-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2022c-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2022c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2022c-102">SYNOPSIS</span></span>
<span data-ttu-id="2022c-103">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2022c-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="2022c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2022c-104">SYNTAX</span></span>

### <span data-ttu-id="2022c-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="2022c-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2022c-106">ID</span><span class="sxs-lookup"><span data-stu-id="2022c-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2022c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2022c-107">DESCRIPTION</span></span>
<span data-ttu-id="2022c-108">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2022c-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="2022c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2022c-109">EXAMPLES</span></span>

### <span data-ttu-id="2022c-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2022c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="2022c-111">Stoppa underhålls läget på en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2022c-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="2022c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2022c-112">PARAMETERS</span></span>

### <span data-ttu-id="2022c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2022c-113">-AsJob</span></span>
<span data-ttu-id="2022c-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="2022c-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2022c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2022c-115">-Force</span></span>
<span data-ttu-id="2022c-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2022c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2022c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="2022c-117">-Location</span></span>
<span data-ttu-id="2022c-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="2022c-118">Location of the resource.</span></span>

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

### <span data-ttu-id="2022c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2022c-119">-Name</span></span>
<span data-ttu-id="2022c-120">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2022c-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="2022c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2022c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2022c-122">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="2022c-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2022c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2022c-123">-ResourceId</span></span>
<span data-ttu-id="2022c-124">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="2022c-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="2022c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2022c-125">-Confirm</span></span>
<span data-ttu-id="2022c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2022c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2022c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2022c-127">-WhatIf</span></span>
<span data-ttu-id="2022c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2022c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2022c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2022c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2022c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2022c-130">CommonParameters</span></span>
<span data-ttu-id="2022c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2022c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2022c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2022c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2022c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2022c-133">INPUTS</span></span>

## <span data-ttu-id="2022c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2022c-134">OUTPUTS</span></span>

## <span data-ttu-id="2022c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2022c-135">NOTES</span></span>

## <span data-ttu-id="2022c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2022c-136">RELATED LINKS</span></span>

