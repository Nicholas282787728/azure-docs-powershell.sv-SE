---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921627"
---
# <span data-ttu-id="b8169-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b8169-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b8169-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8169-102">SYNOPSIS</span></span>
<span data-ttu-id="b8169-103">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="b8169-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="b8169-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8169-104">SYNTAX</span></span>

### <span data-ttu-id="b8169-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="b8169-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8169-106">ID</span><span class="sxs-lookup"><span data-stu-id="b8169-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8169-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8169-107">DESCRIPTION</span></span>
<span data-ttu-id="b8169-108">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="b8169-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="b8169-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8169-109">EXAMPLES</span></span>

### <span data-ttu-id="b8169-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b8169-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="b8169-111">Reparera en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="b8169-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="b8169-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8169-112">PARAMETERS</span></span>

### <span data-ttu-id="b8169-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8169-113">-Name</span></span>
<span data-ttu-id="b8169-114">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b8169-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b8169-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b8169-115">-BMCIPv4Address</span></span>
<span data-ttu-id="b8169-116">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="b8169-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="b8169-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="b8169-117">-Location</span></span>
<span data-ttu-id="b8169-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b8169-118">Location of the resource.</span></span>

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

### <span data-ttu-id="b8169-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8169-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8169-120">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="b8169-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b8169-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8169-121">-ResourceId</span></span>
<span data-ttu-id="b8169-122">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="b8169-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b8169-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8169-123">-AsJob</span></span>
<span data-ttu-id="b8169-124">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="b8169-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b8169-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b8169-125">-Force</span></span>
<span data-ttu-id="b8169-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b8169-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b8169-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8169-127">-WhatIf</span></span>
<span data-ttu-id="b8169-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8169-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8169-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8169-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8169-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8169-130">-Confirm</span></span>
<span data-ttu-id="b8169-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8169-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8169-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8169-132">CommonParameters</span></span>
<span data-ttu-id="b8169-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8169-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8169-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8169-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8169-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8169-135">INPUTS</span></span>

## <span data-ttu-id="b8169-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8169-136">OUTPUTS</span></span>

## <span data-ttu-id="b8169-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8169-137">NOTES</span></span>

## <span data-ttu-id="b8169-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8169-138">RELATED LINKS</span></span>
