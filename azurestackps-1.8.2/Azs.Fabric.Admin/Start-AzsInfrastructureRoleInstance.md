---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100070"
---
# <span data-ttu-id="c59ec-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c59ec-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c59ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c59ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c59ec-103">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c59ec-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c59ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c59ec-104">SYNTAX</span></span>

### <span data-ttu-id="c59ec-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="c59ec-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59ec-106">ID</span><span class="sxs-lookup"><span data-stu-id="c59ec-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c59ec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c59ec-107">DESCRIPTION</span></span>
<span data-ttu-id="c59ec-108">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c59ec-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c59ec-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c59ec-109">EXAMPLES</span></span>

### <span data-ttu-id="c59ec-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="c59ec-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="c59ec-111">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c59ec-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c59ec-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c59ec-112">PARAMETERS</span></span>

### <span data-ttu-id="c59ec-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c59ec-113">-Name</span></span>
<span data-ttu-id="c59ec-114">Namn på infrastruktur roll instansen.</span><span class="sxs-lookup"><span data-stu-id="c59ec-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59ec-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="c59ec-115">-Location</span></span>
<span data-ttu-id="c59ec-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c59ec-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="c59ec-118">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="c59ec-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59ec-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c59ec-119">-ResourceId</span></span>
<span data-ttu-id="c59ec-120">Resurs-ID för infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="c59ec-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c59ec-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c59ec-121">-AsJob</span></span>
<span data-ttu-id="c59ec-122">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="c59ec-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c59ec-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c59ec-123">-Force</span></span>
<span data-ttu-id="c59ec-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c59ec-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c59ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59ec-125">-WhatIf</span></span>
<span data-ttu-id="c59ec-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c59ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59ec-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c59ec-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59ec-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c59ec-128">-Confirm</span></span>
<span data-ttu-id="c59ec-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c59ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59ec-130">CommonParameters</span></span>
<span data-ttu-id="c59ec-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59ec-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59ec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59ec-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c59ec-133">INPUTS</span></span>

## <span data-ttu-id="c59ec-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c59ec-134">OUTPUTS</span></span>

## <span data-ttu-id="c59ec-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c59ec-135">NOTES</span></span>

## <span data-ttu-id="c59ec-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c59ec-136">RELATED LINKS</span></span>
