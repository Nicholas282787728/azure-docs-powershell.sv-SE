---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571476"
---
# <span data-ttu-id="1acde-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1acde-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1acde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1acde-102">SYNOPSIS</span></span>
<span data-ttu-id="1acde-103">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="1acde-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="1acde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1acde-104">SYNTAX</span></span>

### <span data-ttu-id="1acde-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="1acde-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1acde-106">ID</span><span class="sxs-lookup"><span data-stu-id="1acde-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1acde-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1acde-107">DESCRIPTION</span></span>
<span data-ttu-id="1acde-108">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="1acde-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="1acde-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1acde-109">EXAMPLES</span></span>

### <span data-ttu-id="1acde-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1acde-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="1acde-111">Reparera en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="1acde-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="1acde-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1acde-112">PARAMETERS</span></span>

### <span data-ttu-id="1acde-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1acde-113">-AsJob</span></span>
<span data-ttu-id="1acde-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="1acde-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1acde-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="1acde-115">-BMCIPv4Address</span></span>
<span data-ttu-id="1acde-116">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="1acde-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1acde-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1acde-117">-Force</span></span>
<span data-ttu-id="1acde-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1acde-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1acde-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="1acde-119">-Location</span></span>
<span data-ttu-id="1acde-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1acde-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1acde-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1acde-121">-Name</span></span>
<span data-ttu-id="1acde-122">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1acde-122">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1acde-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1acde-123">-ResourceGroupName</span></span>
<span data-ttu-id="1acde-124">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1acde-124">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1acde-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1acde-125">-ResourceId</span></span>
<span data-ttu-id="1acde-126">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="1acde-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1acde-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1acde-127">-Confirm</span></span>
<span data-ttu-id="1acde-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1acde-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1acde-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1acde-129">-WhatIf</span></span>
<span data-ttu-id="1acde-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1acde-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1acde-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1acde-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1acde-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acde-132">CommonParameters</span></span>
<span data-ttu-id="1acde-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acde-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acde-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1acde-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acde-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1acde-135">INPUTS</span></span>

## <span data-ttu-id="1acde-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1acde-136">OUTPUTS</span></span>

## <span data-ttu-id="1acde-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1acde-137">NOTES</span></span>

## <span data-ttu-id="1acde-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1acde-138">RELATED LINKS</span></span>

