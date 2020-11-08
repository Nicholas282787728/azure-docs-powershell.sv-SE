---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100068"
---
# <span data-ttu-id="cbb3f-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="cbb3f-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="cbb3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb3f-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="cbb3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbb3f-104">SYNTAX</span></span>

### <span data-ttu-id="cbb3f-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="cbb3f-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbb3f-106">ID</span><span class="sxs-lookup"><span data-stu-id="cbb3f-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbb3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbb3f-107">DESCRIPTION</span></span>
<span data-ttu-id="cbb3f-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="cbb3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbb3f-109">EXAMPLES</span></span>

### <span data-ttu-id="cbb3f-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="cbb3f-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="cbb3f-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="cbb3f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbb3f-112">PARAMETERS</span></span>

### <span data-ttu-id="cbb3f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbb3f-113">-Name</span></span>
<span data-ttu-id="cbb3f-114">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="cbb3f-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="cbb3f-115">-Location</span></span>
<span data-ttu-id="cbb3f-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-116">Location of the resource.</span></span>

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

### <span data-ttu-id="cbb3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbb3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="cbb3f-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="cbb3f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbb3f-119">-ResourceId</span></span>
<span data-ttu-id="cbb3f-120">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="cbb3f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbb3f-121">-AsJob</span></span>
<span data-ttu-id="cbb3f-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cbb3f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cbb3f-123">-Force</span></span>
<span data-ttu-id="cbb3f-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cbb3f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbb3f-125">-WhatIf</span></span>
<span data-ttu-id="cbb3f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbb3f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbb3f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbb3f-128">-Confirm</span></span>
<span data-ttu-id="cbb3f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbb3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb3f-130">CommonParameters</span></span>
<span data-ttu-id="cbb3f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb3f-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb3f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb3f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbb3f-133">INPUTS</span></span>

## <span data-ttu-id="cbb3f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbb3f-134">OUTPUTS</span></span>

## <span data-ttu-id="cbb3f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbb3f-135">NOTES</span></span>

## <span data-ttu-id="cbb3f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbb3f-136">RELATED LINKS</span></span>
