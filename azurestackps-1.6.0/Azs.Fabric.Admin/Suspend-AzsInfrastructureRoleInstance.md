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
ms.locfileid: "93571968"
---
# <span data-ttu-id="c2c5a-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c2c5a-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c2c5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c5a-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c2c5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2c5a-104">SYNTAX</span></span>

### <span data-ttu-id="c2c5a-105">Shutdown (standard)</span><span class="sxs-lookup"><span data-stu-id="c2c5a-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c5a-106">ID</span><span class="sxs-lookup"><span data-stu-id="c2c5a-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c5a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c5a-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c2c5a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="c2c5a-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2c5a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="c2c5a-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="c2c5a-112">Vid ett fel uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="c2c5a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2c5a-113">PARAMETERS</span></span>

### <span data-ttu-id="c2c5a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2c5a-114">-AsJob</span></span>
<span data-ttu-id="c2c5a-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c2c5a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c2c5a-116">-Force</span></span>
<span data-ttu-id="c2c5a-117">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="c2c5a-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="c2c5a-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="c2c5a-118">-Location</span></span>
<span data-ttu-id="c2c5a-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c2c5a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2c5a-120">-Name</span></span>
<span data-ttu-id="c2c5a-121">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="c2c5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2c5a-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c2c5a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c5a-124">-ResourceId</span></span>
<span data-ttu-id="c2c5a-125">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c2c5a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2c5a-126">-Confirm</span></span>
<span data-ttu-id="c2c5a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c5a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c5a-128">-WhatIf</span></span>
<span data-ttu-id="c2c5a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c5a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c5a-131">CommonParameters</span></span>
<span data-ttu-id="c2c5a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c5a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c5a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c5a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2c5a-134">INPUTS</span></span>

## <span data-ttu-id="c2c5a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2c5a-135">OUTPUTS</span></span>

## <span data-ttu-id="c2c5a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2c5a-136">NOTES</span></span>

## <span data-ttu-id="c2c5a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2c5a-137">RELATED LINKS</span></span>

