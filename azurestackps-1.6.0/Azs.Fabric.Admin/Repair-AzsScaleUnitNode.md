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
ms.locfileid: "93571360"
---
# <span data-ttu-id="becad-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="becad-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="becad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="becad-102">SYNOPSIS</span></span>
<span data-ttu-id="becad-103">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="becad-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="becad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="becad-104">SYNTAX</span></span>

### <span data-ttu-id="becad-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="becad-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="becad-106">ID</span><span class="sxs-lookup"><span data-stu-id="becad-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="becad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="becad-107">DESCRIPTION</span></span>
<span data-ttu-id="becad-108">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="becad-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="becad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="becad-109">EXAMPLES</span></span>

### <span data-ttu-id="becad-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="becad-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="becad-111">Reparera en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="becad-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="becad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="becad-112">PARAMETERS</span></span>

### <span data-ttu-id="becad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="becad-113">-AsJob</span></span>
<span data-ttu-id="becad-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="becad-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="becad-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="becad-115">-BMCIPv4Address</span></span>
<span data-ttu-id="becad-116">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="becad-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="becad-117">-Force</span><span class="sxs-lookup"><span data-stu-id="becad-117">-Force</span></span>
<span data-ttu-id="becad-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="becad-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="becad-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="becad-119">-Location</span></span>
<span data-ttu-id="becad-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="becad-120">Location of the resource.</span></span>

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

### <span data-ttu-id="becad-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="becad-121">-Name</span></span>
<span data-ttu-id="becad-122">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="becad-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="becad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="becad-123">-ResourceGroupName</span></span>
<span data-ttu-id="becad-124">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="becad-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="becad-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="becad-125">-ResourceId</span></span>
<span data-ttu-id="becad-126">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="becad-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="becad-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="becad-127">-Confirm</span></span>
<span data-ttu-id="becad-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="becad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becad-129">-WhatIf</span></span>
<span data-ttu-id="becad-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="becad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="becad-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="becad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="becad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becad-132">CommonParameters</span></span>
<span data-ttu-id="becad-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="becad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becad-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="becad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becad-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="becad-135">INPUTS</span></span>

## <span data-ttu-id="becad-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="becad-136">OUTPUTS</span></span>

## <span data-ttu-id="becad-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="becad-137">NOTES</span></span>

## <span data-ttu-id="becad-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="becad-138">RELATED LINKS</span></span>

