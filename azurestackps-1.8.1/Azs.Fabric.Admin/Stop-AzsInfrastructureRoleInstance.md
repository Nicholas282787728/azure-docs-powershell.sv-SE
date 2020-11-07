---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921853"
---
# <span data-ttu-id="7ee95-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7ee95-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="7ee95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ee95-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee95-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7ee95-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7ee95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ee95-104">SYNTAX</span></span>

### <span data-ttu-id="7ee95-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="7ee95-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee95-106">ID</span><span class="sxs-lookup"><span data-stu-id="7ee95-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ee95-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ee95-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee95-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7ee95-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7ee95-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ee95-109">EXAMPLES</span></span>

### <span data-ttu-id="7ee95-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="7ee95-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="7ee95-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7ee95-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="7ee95-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ee95-112">PARAMETERS</span></span>

### <span data-ttu-id="7ee95-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ee95-113">-Name</span></span>
<span data-ttu-id="7ee95-114">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7ee95-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee95-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="7ee95-115">-Location</span></span>
<span data-ttu-id="7ee95-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="7ee95-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee95-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ee95-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="7ee95-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee95-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee95-119">-ResourceId</span></span>
<span data-ttu-id="7ee95-120">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7ee95-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="7ee95-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ee95-121">-AsJob</span></span>
<span data-ttu-id="7ee95-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="7ee95-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7ee95-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7ee95-123">-Force</span></span>
<span data-ttu-id="7ee95-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7ee95-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7ee95-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee95-125">-WhatIf</span></span>
<span data-ttu-id="7ee95-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ee95-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee95-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ee95-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee95-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ee95-128">-Confirm</span></span>
<span data-ttu-id="7ee95-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ee95-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee95-130">CommonParameters</span></span>
<span data-ttu-id="7ee95-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee95-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee95-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee95-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ee95-133">INPUTS</span></span>

## <span data-ttu-id="7ee95-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ee95-134">OUTPUTS</span></span>

## <span data-ttu-id="7ee95-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ee95-135">NOTES</span></span>

## <span data-ttu-id="7ee95-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ee95-136">RELATED LINKS</span></span>
