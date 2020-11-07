---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921335"
---
# <span data-ttu-id="d478a-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d478a-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d478a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d478a-102">SYNOPSIS</span></span>
<span data-ttu-id="d478a-103">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d478a-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="d478a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d478a-104">SYNTAX</span></span>

### <span data-ttu-id="d478a-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="d478a-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d478a-106">ID</span><span class="sxs-lookup"><span data-stu-id="d478a-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d478a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d478a-107">DESCRIPTION</span></span>
<span data-ttu-id="d478a-108">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d478a-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="d478a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d478a-109">EXAMPLES</span></span>

### <span data-ttu-id="d478a-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="d478a-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="d478a-111">ProvisioningState: lyckades</span><span class="sxs-lookup"><span data-stu-id="d478a-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="d478a-112">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d478a-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="d478a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d478a-113">PARAMETERS</span></span>

### <span data-ttu-id="d478a-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d478a-114">-Name</span></span>
<span data-ttu-id="d478a-115">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d478a-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="d478a-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="d478a-116">-Location</span></span>
<span data-ttu-id="d478a-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="d478a-117">Location of the resource.</span></span>

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

### <span data-ttu-id="d478a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d478a-118">-ResourceGroupName</span></span>
<span data-ttu-id="d478a-119">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="d478a-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d478a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d478a-120">-ResourceId</span></span>
<span data-ttu-id="d478a-121">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="d478a-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d478a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d478a-122">-AsJob</span></span>
<span data-ttu-id="d478a-123">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="d478a-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d478a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d478a-124">-Force</span></span>
<span data-ttu-id="d478a-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d478a-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d478a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d478a-126">-WhatIf</span></span>
<span data-ttu-id="d478a-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d478a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d478a-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d478a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d478a-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d478a-129">-Confirm</span></span>
<span data-ttu-id="d478a-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d478a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d478a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d478a-131">CommonParameters</span></span>
<span data-ttu-id="d478a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d478a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d478a-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d478a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d478a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d478a-134">INPUTS</span></span>

## <span data-ttu-id="d478a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d478a-135">OUTPUTS</span></span>

## <span data-ttu-id="d478a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d478a-136">NOTES</span></span>

## <span data-ttu-id="d478a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d478a-137">RELATED LINKS</span></span>
