---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921194"
---
# <span data-ttu-id="fbec3-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="fbec3-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="fbec3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbec3-102">SYNOPSIS</span></span>
<span data-ttu-id="fbec3-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbec3-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="fbec3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbec3-104">SYNTAX</span></span>

### <span data-ttu-id="fbec3-105">Shutdown (standard)</span><span class="sxs-lookup"><span data-stu-id="fbec3-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbec3-106">ID</span><span class="sxs-lookup"><span data-stu-id="fbec3-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbec3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbec3-107">DESCRIPTION</span></span>
<span data-ttu-id="fbec3-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbec3-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="fbec3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbec3-109">EXAMPLES</span></span>

### <span data-ttu-id="fbec3-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fbec3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="fbec3-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbec3-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="fbec3-112">Vid ett fel uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="fbec3-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="fbec3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbec3-113">PARAMETERS</span></span>

### <span data-ttu-id="fbec3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbec3-114">-AsJob</span></span>
<span data-ttu-id="fbec3-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="fbec3-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fbec3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fbec3-116">-Force</span></span>
<span data-ttu-id="fbec3-117">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="fbec3-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="fbec3-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="fbec3-118">-Location</span></span>
<span data-ttu-id="fbec3-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="fbec3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="fbec3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbec3-120">-Name</span></span>
<span data-ttu-id="fbec3-121">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbec3-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="fbec3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbec3-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbec3-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="fbec3-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fbec3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbec3-124">-ResourceId</span></span>
<span data-ttu-id="fbec3-125">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbec3-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="fbec3-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbec3-126">-Confirm</span></span>
<span data-ttu-id="fbec3-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbec3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbec3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbec3-128">-WhatIf</span></span>
<span data-ttu-id="fbec3-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbec3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbec3-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbec3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbec3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbec3-131">CommonParameters</span></span>
<span data-ttu-id="fbec3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbec3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbec3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbec3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbec3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbec3-134">INPUTS</span></span>

## <span data-ttu-id="fbec3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbec3-135">OUTPUTS</span></span>

## <span data-ttu-id="fbec3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbec3-136">NOTES</span></span>

## <span data-ttu-id="fbec3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbec3-137">RELATED LINKS</span></span>

