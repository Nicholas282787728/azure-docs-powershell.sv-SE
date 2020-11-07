---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921343"
---
# <span data-ttu-id="38f59-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="38f59-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="38f59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38f59-102">SYNOPSIS</span></span>
<span data-ttu-id="38f59-103">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="38f59-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="38f59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38f59-104">SYNTAX</span></span>

### <span data-ttu-id="38f59-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="38f59-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f59-106">ID</span><span class="sxs-lookup"><span data-stu-id="38f59-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38f59-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38f59-107">DESCRIPTION</span></span>
<span data-ttu-id="38f59-108">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="38f59-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="38f59-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38f59-109">EXAMPLES</span></span>

### <span data-ttu-id="38f59-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="38f59-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="38f59-111">Reparera en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="38f59-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="38f59-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38f59-112">PARAMETERS</span></span>

### <span data-ttu-id="38f59-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="38f59-113">-Name</span></span>
<span data-ttu-id="38f59-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="38f59-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="38f59-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="38f59-115">-BMCIPv4Address</span></span>
<span data-ttu-id="38f59-116">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="38f59-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="38f59-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="38f59-117">-Location</span></span>
<span data-ttu-id="38f59-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="38f59-118">Location of the resource.</span></span>

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

### <span data-ttu-id="38f59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f59-119">-ResourceGroupName</span></span>
<span data-ttu-id="38f59-120">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="38f59-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="38f59-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38f59-121">-ResourceId</span></span>
<span data-ttu-id="38f59-122">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="38f59-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="38f59-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38f59-123">-AsJob</span></span>
<span data-ttu-id="38f59-124">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="38f59-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="38f59-125">-Force</span><span class="sxs-lookup"><span data-stu-id="38f59-125">-Force</span></span>
<span data-ttu-id="38f59-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="38f59-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="38f59-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f59-127">-WhatIf</span></span>
<span data-ttu-id="38f59-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38f59-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f59-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38f59-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f59-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38f59-130">-Confirm</span></span>
<span data-ttu-id="38f59-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38f59-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f59-132">CommonParameters</span></span>
<span data-ttu-id="38f59-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f59-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f59-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f59-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38f59-135">INPUTS</span></span>

## <span data-ttu-id="38f59-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38f59-136">OUTPUTS</span></span>

## <span data-ttu-id="38f59-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38f59-137">NOTES</span></span>

## <span data-ttu-id="38f59-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38f59-138">RELATED LINKS</span></span>
