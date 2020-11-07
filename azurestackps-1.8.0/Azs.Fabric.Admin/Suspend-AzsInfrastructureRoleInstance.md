---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921452"
---
# <span data-ttu-id="c4369-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c4369-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c4369-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4369-102">SYNOPSIS</span></span>
<span data-ttu-id="c4369-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c4369-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c4369-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4369-104">SYNTAX</span></span>

### <span data-ttu-id="c4369-105">Shutdown (standard)</span><span class="sxs-lookup"><span data-stu-id="c4369-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4369-106">ID</span><span class="sxs-lookup"><span data-stu-id="c4369-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4369-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4369-107">DESCRIPTION</span></span>
<span data-ttu-id="c4369-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c4369-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c4369-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4369-109">EXAMPLES</span></span>

### <span data-ttu-id="c4369-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="c4369-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="c4369-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c4369-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="c4369-112">Vid ett fel uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="c4369-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="c4369-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4369-113">PARAMETERS</span></span>

### <span data-ttu-id="c4369-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4369-114">-Name</span></span>
<span data-ttu-id="c4369-115">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c4369-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4369-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4369-116">-Location</span></span>
<span data-ttu-id="c4369-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c4369-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4369-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4369-118">-ResourceGroupName</span></span>
<span data-ttu-id="c4369-119">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="c4369-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4369-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4369-120">-ResourceId</span></span>
<span data-ttu-id="c4369-121">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c4369-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c4369-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4369-122">-AsJob</span></span>
<span data-ttu-id="c4369-123">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="c4369-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c4369-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c4369-124">-Force</span></span>
<span data-ttu-id="c4369-125">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="c4369-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="c4369-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4369-126">-WhatIf</span></span>
<span data-ttu-id="c4369-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4369-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4369-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4369-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4369-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4369-129">-Confirm</span></span>
<span data-ttu-id="c4369-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4369-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4369-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4369-131">CommonParameters</span></span>
<span data-ttu-id="c4369-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4369-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4369-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4369-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4369-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4369-134">INPUTS</span></span>

## <span data-ttu-id="c4369-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4369-135">OUTPUTS</span></span>

## <span data-ttu-id="c4369-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4369-136">NOTES</span></span>

## <span data-ttu-id="c4369-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4369-137">RELATED LINKS</span></span>
