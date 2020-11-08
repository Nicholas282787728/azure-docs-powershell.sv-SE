---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099966"
---
# <span data-ttu-id="82190-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="82190-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="82190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82190-102">SYNOPSIS</span></span>
<span data-ttu-id="82190-103">Startar om den begärande infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="82190-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="82190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82190-104">SYNTAX</span></span>

### <span data-ttu-id="82190-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="82190-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82190-106">ID</span><span class="sxs-lookup"><span data-stu-id="82190-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82190-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82190-107">DESCRIPTION</span></span>
<span data-ttu-id="82190-108">Startar om den begärande infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="82190-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="82190-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82190-109">EXAMPLES</span></span>

### <span data-ttu-id="82190-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="82190-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="82190-111">Starta om en infrastruktur roll som har kraschat.</span><span class="sxs-lookup"><span data-stu-id="82190-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="82190-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82190-112">PARAMETERS</span></span>

### <span data-ttu-id="82190-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="82190-113">-Name</span></span>
<span data-ttu-id="82190-114">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="82190-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="82190-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="82190-115">-Location</span></span>
<span data-ttu-id="82190-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="82190-116">Location of the resource.</span></span>

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

### <span data-ttu-id="82190-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82190-117">-ResourceGroupName</span></span>
<span data-ttu-id="82190-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="82190-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="82190-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82190-119">-ResourceId</span></span>
<span data-ttu-id="82190-120">Resurs-ID för infrastruktur roll.</span><span class="sxs-lookup"><span data-stu-id="82190-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="82190-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82190-121">-AsJob</span></span>
<span data-ttu-id="82190-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="82190-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="82190-123">-Force</span><span class="sxs-lookup"><span data-stu-id="82190-123">-Force</span></span>
<span data-ttu-id="82190-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="82190-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="82190-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82190-125">-WhatIf</span></span>
<span data-ttu-id="82190-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82190-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82190-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82190-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82190-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82190-128">-Confirm</span></span>
<span data-ttu-id="82190-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82190-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82190-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82190-130">CommonParameters</span></span>
<span data-ttu-id="82190-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82190-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82190-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82190-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82190-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82190-133">INPUTS</span></span>

## <span data-ttu-id="82190-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82190-134">OUTPUTS</span></span>

## <span data-ttu-id="82190-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82190-135">NOTES</span></span>

## <span data-ttu-id="82190-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82190-136">RELATED LINKS</span></span>
