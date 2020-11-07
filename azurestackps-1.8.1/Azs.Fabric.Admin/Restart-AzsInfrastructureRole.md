---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921686"
---
# <span data-ttu-id="d3f6d-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="d3f6d-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="d3f6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f6d-103">Startar om den begärande infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="d3f6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3f6d-104">SYNTAX</span></span>

### <span data-ttu-id="d3f6d-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="d3f6d-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f6d-106">ID</span><span class="sxs-lookup"><span data-stu-id="d3f6d-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3f6d-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f6d-108">Startar om den begärande infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="d3f6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3f6d-109">EXAMPLES</span></span>

### <span data-ttu-id="d3f6d-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="d3f6d-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="d3f6d-111">Starta om en infrastruktur roll som har kraschat.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="d3f6d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3f6d-112">PARAMETERS</span></span>

### <span data-ttu-id="d3f6d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3f6d-113">-Name</span></span>
<span data-ttu-id="d3f6d-114">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-114">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f6d-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="d3f6d-115">-Location</span></span>
<span data-ttu-id="d3f6d-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3f6d-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f6d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f6d-119">-ResourceId</span></span>
<span data-ttu-id="d3f6d-120">Resurs-ID för infrastruktur roll.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="d3f6d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3f6d-121">-AsJob</span></span>
<span data-ttu-id="d3f6d-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d3f6d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f6d-123">-Force</span></span>
<span data-ttu-id="d3f6d-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d3f6d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f6d-125">-WhatIf</span></span>
<span data-ttu-id="d3f6d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f6d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f6d-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3f6d-128">-Confirm</span></span>
<span data-ttu-id="d3f6d-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f6d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f6d-130">CommonParameters</span></span>
<span data-ttu-id="d3f6d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f6d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f6d-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f6d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f6d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3f6d-133">INPUTS</span></span>

## <span data-ttu-id="d3f6d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3f6d-134">OUTPUTS</span></span>

## <span data-ttu-id="d3f6d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3f6d-135">NOTES</span></span>

## <span data-ttu-id="d3f6d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3f6d-136">RELATED LINKS</span></span>
