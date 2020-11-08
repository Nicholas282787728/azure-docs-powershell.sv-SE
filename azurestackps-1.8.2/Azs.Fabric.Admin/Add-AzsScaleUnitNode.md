---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100010"
---
# <span data-ttu-id="02ab1-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="02ab1-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="02ab1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="02ab1-103">Lägg till en ny skalen het.</span><span class="sxs-lookup"><span data-stu-id="02ab1-103">Add a new scale unit.</span></span>

## <span data-ttu-id="02ab1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02ab1-104">SYNTAX</span></span>

### <span data-ttu-id="02ab1-105">ScaleY (standard)</span><span class="sxs-lookup"><span data-stu-id="02ab1-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ab1-106">ID</span><span class="sxs-lookup"><span data-stu-id="02ab1-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ab1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="02ab1-108">Lägg till en ny skalen het.</span><span class="sxs-lookup"><span data-stu-id="02ab1-108">Add a new scale unit.</span></span>

## <span data-ttu-id="02ab1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02ab1-109">EXAMPLES</span></span>

### <span data-ttu-id="02ab1-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="02ab1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="02ab1-111">Lägga till en ny nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="02ab1-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="02ab1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02ab1-112">PARAMETERS</span></span>

### <span data-ttu-id="02ab1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ab1-113">-AsJob</span></span>
<span data-ttu-id="02ab1-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="02ab1-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="02ab1-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="02ab1-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="02ab1-116">Flagga anger om åtgärden ska vänta på att lagrings platsen ska konvergera innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="02ab1-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="02ab1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="02ab1-117">-Force</span></span>
<span data-ttu-id="02ab1-118">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="02ab1-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="02ab1-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="02ab1-119">-Location</span></span>
<span data-ttu-id="02ab1-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="02ab1-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab1-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="02ab1-121">-Name</span></span>
<span data-ttu-id="02ab1-122">{{Fyllnings namn beskrivning}}</span><span class="sxs-lookup"><span data-stu-id="02ab1-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab1-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="02ab1-123">-NodeList</span></span>
<span data-ttu-id="02ab1-124">Lista över noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="02ab1-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ab1-125">-ResourceGroupName</span></span>
<span data-ttu-id="02ab1-126">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="02ab1-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ab1-127">-ResourceId</span></span>
<span data-ttu-id="02ab1-128">Resurs-ID för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="02ab1-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="02ab1-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02ab1-129">-Confirm</span></span>
<span data-ttu-id="02ab1-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02ab1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ab1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ab1-131">-WhatIf</span></span>
<span data-ttu-id="02ab1-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02ab1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ab1-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02ab1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ab1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ab1-134">CommonParameters</span></span>
<span data-ttu-id="02ab1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ab1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ab1-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ab1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ab1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02ab1-137">INPUTS</span></span>

## <span data-ttu-id="02ab1-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02ab1-138">OUTPUTS</span></span>

## <span data-ttu-id="02ab1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02ab1-139">NOTES</span></span>

## <span data-ttu-id="02ab1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02ab1-140">RELATED LINKS</span></span>

