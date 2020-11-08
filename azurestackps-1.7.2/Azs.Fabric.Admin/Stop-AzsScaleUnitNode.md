---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921196"
---
# <span data-ttu-id="23782-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="23782-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="23782-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23782-102">SYNOPSIS</span></span>
<span data-ttu-id="23782-103">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="23782-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="23782-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23782-104">SYNTAX</span></span>

### <span data-ttu-id="23782-105">Stopp (standard)</span><span class="sxs-lookup"><span data-stu-id="23782-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23782-106">ID</span><span class="sxs-lookup"><span data-stu-id="23782-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23782-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23782-107">DESCRIPTION</span></span>
<span data-ttu-id="23782-108">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="23782-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="23782-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23782-109">EXAMPLES</span></span>

### <span data-ttu-id="23782-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="23782-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="23782-111">Avsluta en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="23782-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="23782-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="23782-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="23782-113">Stänga av en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="23782-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="23782-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23782-114">PARAMETERS</span></span>

### <span data-ttu-id="23782-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23782-115">-AsJob</span></span>
<span data-ttu-id="23782-116">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="23782-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="23782-117">-Force</span><span class="sxs-lookup"><span data-stu-id="23782-117">-Force</span></span>
<span data-ttu-id="23782-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="23782-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="23782-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="23782-119">-Location</span></span>
<span data-ttu-id="23782-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="23782-120">Location of the resource.</span></span>

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

### <span data-ttu-id="23782-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="23782-121">-Name</span></span>
<span data-ttu-id="23782-122">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="23782-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="23782-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23782-123">-ResourceGroupName</span></span>
<span data-ttu-id="23782-124">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="23782-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="23782-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23782-125">-ResourceId</span></span>
<span data-ttu-id="23782-126">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="23782-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="23782-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="23782-127">-Shutdown</span></span>
<span data-ttu-id="23782-128">Om du har avaktiverat Stäng av noden Scale Unit i övrigt stänger du av noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="23782-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="23782-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23782-129">-Confirm</span></span>
<span data-ttu-id="23782-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23782-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23782-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23782-131">-WhatIf</span></span>
<span data-ttu-id="23782-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23782-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23782-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23782-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23782-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23782-134">CommonParameters</span></span>
<span data-ttu-id="23782-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23782-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23782-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23782-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23782-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23782-137">INPUTS</span></span>

## <span data-ttu-id="23782-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23782-138">OUTPUTS</span></span>

## <span data-ttu-id="23782-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23782-139">NOTES</span></span>

## <span data-ttu-id="23782-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23782-140">RELATED LINKS</span></span>
