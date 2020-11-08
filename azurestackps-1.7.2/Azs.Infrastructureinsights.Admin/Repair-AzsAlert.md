---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921275"
---
# <span data-ttu-id="e94e4-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="e94e4-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="e94e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e94e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e94e4-103">Reparerar den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="e94e4-103">Repairs the given alert.</span></span>

## <span data-ttu-id="e94e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e94e4-104">SYNTAX</span></span>

### <span data-ttu-id="e94e4-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="e94e4-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e94e4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e94e4-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94e4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e94e4-107">DESCRIPTION</span></span>
<span data-ttu-id="e94e4-108">Reparerar den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="e94e4-108">Repairs the given alert.</span></span>

## <span data-ttu-id="e94e4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e94e4-109">EXAMPLES</span></span>

### <span data-ttu-id="e94e4-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e94e4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="e94e4-111">Reparerar en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="e94e4-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="e94e4-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e94e4-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="e94e4-113">Reparerar en avisering genom rörledningar.</span><span class="sxs-lookup"><span data-stu-id="e94e4-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="e94e4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e94e4-114">PARAMETERS</span></span>

### <span data-ttu-id="e94e4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e94e4-115">-Force</span></span>
<span data-ttu-id="e94e4-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e94e4-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e94e4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e94e4-117">-InputObject</span></span>
<span data-ttu-id="e94e4-118">En avisering returnerades från get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="e94e4-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e94e4-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="e94e4-119">-Location</span></span>
<span data-ttu-id="e94e4-120">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="e94e4-120">Name of the location.</span></span>

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

### <span data-ttu-id="e94e4-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e94e4-121">-Name</span></span>
<span data-ttu-id="e94e4-122">Aviserings-ID.</span><span class="sxs-lookup"><span data-stu-id="e94e4-122">The alert identifier.</span></span>

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

### <span data-ttu-id="e94e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="e94e4-124">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="e94e4-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="e94e4-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e94e4-125">-Confirm</span></span>
<span data-ttu-id="e94e4-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e94e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94e4-127">-WhatIf</span></span>
<span data-ttu-id="e94e4-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e94e4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94e4-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e94e4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94e4-130">CommonParameters</span></span>
<span data-ttu-id="e94e4-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94e4-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94e4-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e94e4-133">INPUTS</span></span>

## <span data-ttu-id="e94e4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e94e4-134">OUTPUTS</span></span>

## <span data-ttu-id="e94e4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e94e4-135">NOTES</span></span>

## <span data-ttu-id="e94e4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e94e4-136">RELATED LINKS</span></span>
