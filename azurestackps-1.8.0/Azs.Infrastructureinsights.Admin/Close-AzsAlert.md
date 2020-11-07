---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921440"
---
# <span data-ttu-id="9488c-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="9488c-101">Close-AzsAlert</span></span>

## <span data-ttu-id="9488c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9488c-102">SYNOPSIS</span></span>
<span data-ttu-id="9488c-103">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="9488c-103">Closes the given alert.</span></span>

## <span data-ttu-id="9488c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9488c-104">SYNTAX</span></span>

### <span data-ttu-id="9488c-105">Close (standard)</span><span class="sxs-lookup"><span data-stu-id="9488c-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9488c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9488c-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9488c-107">ID</span><span class="sxs-lookup"><span data-stu-id="9488c-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9488c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9488c-108">DESCRIPTION</span></span>
<span data-ttu-id="9488c-109">Stänger den angivna varningen.</span><span class="sxs-lookup"><span data-stu-id="9488c-109">Closes the given alert.</span></span>

## <span data-ttu-id="9488c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9488c-110">EXAMPLES</span></span>

### <span data-ttu-id="9488c-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="9488c-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="9488c-112">Stänga en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="9488c-112">Close an alert by Name.</span></span>

### <span data-ttu-id="9488c-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="9488c-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="9488c-114">Stänga en avisering genom att flytta.</span><span class="sxs-lookup"><span data-stu-id="9488c-114">Close an alert through piping.</span></span>

## <span data-ttu-id="9488c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9488c-115">PARAMETERS</span></span>

### <span data-ttu-id="9488c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9488c-116">-Name</span></span>
<span data-ttu-id="9488c-117">Aviserings-ID.</span><span class="sxs-lookup"><span data-stu-id="9488c-117">The alert identifier.</span></span>

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

### <span data-ttu-id="9488c-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="9488c-118">-Location</span></span>
<span data-ttu-id="9488c-119">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="9488c-119">Name of the location.</span></span>

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

### <span data-ttu-id="9488c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9488c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9488c-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9488c-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="9488c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9488c-122">-InputObject</span></span>
<span data-ttu-id="9488c-123">En avisering returnerades från get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="9488c-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="9488c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9488c-124">-ResourceId</span></span>
<span data-ttu-id="9488c-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9488c-125">The resource id.</span></span>

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

### <span data-ttu-id="9488c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9488c-126">-Force</span></span>
<span data-ttu-id="9488c-127">Byt parameter för att inte fråga bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9488c-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="9488c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9488c-128">-WhatIf</span></span>
<span data-ttu-id="9488c-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9488c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9488c-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9488c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9488c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9488c-131">-Confirm</span></span>
<span data-ttu-id="9488c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9488c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9488c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9488c-133">CommonParameters</span></span>
<span data-ttu-id="9488c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9488c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9488c-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9488c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9488c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9488c-136">INPUTS</span></span>

## <span data-ttu-id="9488c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9488c-137">OUTPUTS</span></span>

### <span data-ttu-id="9488c-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="9488c-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="9488c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9488c-139">NOTES</span></span>

## <span data-ttu-id="9488c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9488c-140">RELATED LINKS</span></span>
