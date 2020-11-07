---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921195"
---
# <span data-ttu-id="b3166-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b3166-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="b3166-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3166-102">SYNOPSIS</span></span>
<span data-ttu-id="b3166-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b3166-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="b3166-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3166-104">SYNTAX</span></span>

### <span data-ttu-id="b3166-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="b3166-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3166-106">ID</span><span class="sxs-lookup"><span data-stu-id="b3166-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3166-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3166-107">DESCRIPTION</span></span>
<span data-ttu-id="b3166-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b3166-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="b3166-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3166-109">EXAMPLES</span></span>

### <span data-ttu-id="b3166-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3166-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="b3166-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b3166-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="b3166-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3166-112">PARAMETERS</span></span>

### <span data-ttu-id="b3166-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3166-113">-AsJob</span></span>
<span data-ttu-id="b3166-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="b3166-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b3166-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3166-115">-Force</span></span>
<span data-ttu-id="b3166-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b3166-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b3166-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="b3166-117">-Location</span></span>
<span data-ttu-id="b3166-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b3166-118">Location of the resource.</span></span>

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

### <span data-ttu-id="b3166-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3166-119">-Name</span></span>
<span data-ttu-id="b3166-120">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b3166-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="b3166-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3166-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3166-122">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="b3166-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b3166-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3166-123">-ResourceId</span></span>
<span data-ttu-id="b3166-124">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b3166-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="b3166-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3166-125">-Confirm</span></span>
<span data-ttu-id="b3166-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3166-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3166-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3166-127">-WhatIf</span></span>
<span data-ttu-id="b3166-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3166-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3166-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3166-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3166-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3166-130">CommonParameters</span></span>
<span data-ttu-id="b3166-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3166-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3166-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3166-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3166-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3166-133">INPUTS</span></span>

## <span data-ttu-id="b3166-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3166-134">OUTPUTS</span></span>

## <span data-ttu-id="b3166-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3166-135">NOTES</span></span>

## <span data-ttu-id="b3166-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3166-136">RELATED LINKS</span></span>

