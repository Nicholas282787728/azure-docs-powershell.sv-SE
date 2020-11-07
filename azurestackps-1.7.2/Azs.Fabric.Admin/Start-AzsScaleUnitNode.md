---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921198"
---
# <span data-ttu-id="eb016-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="eb016-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="eb016-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb016-102">SYNOPSIS</span></span>
<span data-ttu-id="eb016-103">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="eb016-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="eb016-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb016-104">SYNTAX</span></span>

### <span data-ttu-id="eb016-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="eb016-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb016-106">ID</span><span class="sxs-lookup"><span data-stu-id="eb016-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb016-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb016-107">DESCRIPTION</span></span>
<span data-ttu-id="eb016-108">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="eb016-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="eb016-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb016-109">EXAMPLES</span></span>

### <span data-ttu-id="eb016-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb016-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="eb016-111">ProvisioningState: lyckades</span><span class="sxs-lookup"><span data-stu-id="eb016-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="eb016-112">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="eb016-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="eb016-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb016-113">PARAMETERS</span></span>

### <span data-ttu-id="eb016-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb016-114">-AsJob</span></span>
<span data-ttu-id="eb016-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="eb016-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb016-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eb016-116">-Force</span></span>
<span data-ttu-id="eb016-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="eb016-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eb016-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="eb016-118">-Location</span></span>
<span data-ttu-id="eb016-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="eb016-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb016-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb016-120">-Name</span></span>
<span data-ttu-id="eb016-121">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="eb016-121">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb016-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb016-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb016-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="eb016-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb016-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb016-124">-ResourceId</span></span>
<span data-ttu-id="eb016-125">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="eb016-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="eb016-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb016-126">-Confirm</span></span>
<span data-ttu-id="eb016-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb016-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb016-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb016-128">-WhatIf</span></span>
<span data-ttu-id="eb016-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb016-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb016-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb016-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb016-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb016-131">CommonParameters</span></span>
<span data-ttu-id="eb016-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb016-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb016-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb016-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb016-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb016-134">INPUTS</span></span>

## <span data-ttu-id="eb016-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb016-135">OUTPUTS</span></span>

## <span data-ttu-id="eb016-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb016-136">NOTES</span></span>

## <span data-ttu-id="eb016-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb016-137">RELATED LINKS</span></span>

