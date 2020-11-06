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
ms.locfileid: "93571944"
---
# <span data-ttu-id="fe49b-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="fe49b-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="fe49b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe49b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe49b-103">Reparerar den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="fe49b-103">Repairs the given alert.</span></span>

## <span data-ttu-id="fe49b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe49b-104">SYNTAX</span></span>

### <span data-ttu-id="fe49b-105">Reparera (standard)</span><span class="sxs-lookup"><span data-stu-id="fe49b-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe49b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe49b-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe49b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe49b-107">DESCRIPTION</span></span>
<span data-ttu-id="fe49b-108">Reparerar den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="fe49b-108">Repairs the given alert.</span></span>

## <span data-ttu-id="fe49b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe49b-109">EXAMPLES</span></span>

### <span data-ttu-id="fe49b-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe49b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="fe49b-111">Reparerar en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="fe49b-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="fe49b-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe49b-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="fe49b-113">Reparerar en avisering genom rörledningar.</span><span class="sxs-lookup"><span data-stu-id="fe49b-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="fe49b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe49b-114">PARAMETERS</span></span>

### <span data-ttu-id="fe49b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fe49b-115">-Force</span></span>
<span data-ttu-id="fe49b-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fe49b-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fe49b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe49b-117">-InputObject</span></span>
<span data-ttu-id="fe49b-118">En avisering returnerades från get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="fe49b-118">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="fe49b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe49b-119">-Location</span></span>
<span data-ttu-id="fe49b-120">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="fe49b-120">Name of the location.</span></span>

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

### <span data-ttu-id="fe49b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe49b-121">-Name</span></span>
<span data-ttu-id="fe49b-122">Aviserings-ID.</span><span class="sxs-lookup"><span data-stu-id="fe49b-122">The alert identifier.</span></span>

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

### <span data-ttu-id="fe49b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe49b-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe49b-124">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="fe49b-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="fe49b-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe49b-125">-Confirm</span></span>
<span data-ttu-id="fe49b-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe49b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe49b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe49b-127">-WhatIf</span></span>
<span data-ttu-id="fe49b-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe49b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe49b-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe49b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe49b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe49b-130">CommonParameters</span></span>
<span data-ttu-id="fe49b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe49b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe49b-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe49b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe49b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe49b-133">INPUTS</span></span>

## <span data-ttu-id="fe49b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe49b-134">OUTPUTS</span></span>

## <span data-ttu-id="fe49b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe49b-135">NOTES</span></span>

## <span data-ttu-id="fe49b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe49b-136">RELATED LINKS</span></span>

