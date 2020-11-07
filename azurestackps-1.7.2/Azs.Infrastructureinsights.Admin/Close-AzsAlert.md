---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921184"
---
# <span data-ttu-id="4e03d-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="4e03d-101">Close-AzsAlert</span></span>

## <span data-ttu-id="4e03d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e03d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e03d-103">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="4e03d-103">Closes the given alert.</span></span>

## <span data-ttu-id="4e03d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e03d-104">SYNTAX</span></span>

### <span data-ttu-id="4e03d-105">Close (standard)</span><span class="sxs-lookup"><span data-stu-id="4e03d-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e03d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4e03d-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e03d-107">ID</span><span class="sxs-lookup"><span data-stu-id="4e03d-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e03d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e03d-108">DESCRIPTION</span></span>
<span data-ttu-id="4e03d-109">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="4e03d-109">Closes the given alert.</span></span>

## <span data-ttu-id="4e03d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e03d-110">EXAMPLES</span></span>

### <span data-ttu-id="4e03d-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4e03d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="4e03d-112">Stänga en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="4e03d-112">Close an alert by Name.</span></span>

### <span data-ttu-id="4e03d-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4e03d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="4e03d-114">Stänga en avisering genom att flytta.</span><span class="sxs-lookup"><span data-stu-id="4e03d-114">Close an alert through piping.</span></span>

## <span data-ttu-id="4e03d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e03d-115">PARAMETERS</span></span>

### <span data-ttu-id="4e03d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e03d-116">-Force</span></span>
<span data-ttu-id="4e03d-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4e03d-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4e03d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e03d-118">-InputObject</span></span>
<span data-ttu-id="4e03d-119">En avisering returnerades från get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="4e03d-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="4e03d-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="4e03d-120">-Location</span></span>
<span data-ttu-id="4e03d-121">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="4e03d-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e03d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e03d-122">-Name</span></span>
<span data-ttu-id="4e03d-123">Aviserings-ID.</span><span class="sxs-lookup"><span data-stu-id="4e03d-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e03d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e03d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e03d-125">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="4e03d-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e03d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e03d-126">-ResourceId</span></span>
<span data-ttu-id="4e03d-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4e03d-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e03d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e03d-128">-Confirm</span></span>
<span data-ttu-id="4e03d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e03d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e03d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e03d-130">-WhatIf</span></span>
<span data-ttu-id="4e03d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e03d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e03d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e03d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e03d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e03d-133">CommonParameters</span></span>
<span data-ttu-id="4e03d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e03d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e03d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e03d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e03d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e03d-136">INPUTS</span></span>

## <span data-ttu-id="4e03d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e03d-137">OUTPUTS</span></span>

### <span data-ttu-id="4e03d-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="4e03d-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="4e03d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e03d-139">NOTES</span></span>

## <span data-ttu-id="4e03d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e03d-140">RELATED LINKS</span></span>

