---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571500"
---
# <span data-ttu-id="52b2e-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="52b2e-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="52b2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="52b2e-103">Startar om den begärda infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="52b2e-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="52b2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52b2e-104">SYNTAX</span></span>

### <span data-ttu-id="52b2e-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="52b2e-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b2e-106">ID</span><span class="sxs-lookup"><span data-stu-id="52b2e-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b2e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52b2e-107">DESCRIPTION</span></span>
<span data-ttu-id="52b2e-108">Startar om den begärda infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="52b2e-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="52b2e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52b2e-109">EXAMPLES</span></span>

### <span data-ttu-id="52b2e-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52b2e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="52b2e-111">Starta om en infrastruktur roll som har kraschat.</span><span class="sxs-lookup"><span data-stu-id="52b2e-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="52b2e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52b2e-112">PARAMETERS</span></span>

### <span data-ttu-id="52b2e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52b2e-113">-AsJob</span></span>
<span data-ttu-id="52b2e-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="52b2e-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="52b2e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="52b2e-115">-Force</span></span>
<span data-ttu-id="52b2e-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="52b2e-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="52b2e-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="52b2e-117">-Location</span></span>
<span data-ttu-id="52b2e-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="52b2e-118">Location of the resource.</span></span>

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

### <span data-ttu-id="52b2e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="52b2e-119">-Name</span></span>
<span data-ttu-id="52b2e-120">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="52b2e-120">Infrastructure role name.</span></span>

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

### <span data-ttu-id="52b2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="52b2e-122">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="52b2e-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="52b2e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52b2e-123">-ResourceId</span></span>
<span data-ttu-id="52b2e-124">Resurs-ID för infrastruktur roll.</span><span class="sxs-lookup"><span data-stu-id="52b2e-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="52b2e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52b2e-125">-Confirm</span></span>
<span data-ttu-id="52b2e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52b2e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b2e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b2e-127">-WhatIf</span></span>
<span data-ttu-id="52b2e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52b2e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b2e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52b2e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b2e-130">CommonParameters</span></span>
<span data-ttu-id="52b2e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b2e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b2e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b2e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52b2e-133">INPUTS</span></span>

## <span data-ttu-id="52b2e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52b2e-134">OUTPUTS</span></span>

## <span data-ttu-id="52b2e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52b2e-135">NOTES</span></span>

## <span data-ttu-id="52b2e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52b2e-136">RELATED LINKS</span></span>

