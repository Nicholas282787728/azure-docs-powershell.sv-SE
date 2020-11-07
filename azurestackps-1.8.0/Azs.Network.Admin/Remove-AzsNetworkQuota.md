---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921529"
---
# <span data-ttu-id="89d9f-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="89d9f-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="89d9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="89d9f-103">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="89d9f-103">Delete a quota by name.</span></span>

## <span data-ttu-id="89d9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89d9f-104">SYNTAX</span></span>

### <span data-ttu-id="89d9f-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="89d9f-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89d9f-106">ID</span><span class="sxs-lookup"><span data-stu-id="89d9f-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89d9f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="89d9f-108">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="89d9f-108">Delete a quota by name.</span></span>

## <span data-ttu-id="89d9f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="89d9f-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="89d9f-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="89d9f-111">Ta bort en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="89d9f-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="89d9f-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="89d9f-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="89d9f-113">Ta bort en nätverks kvot med en pipe.</span><span class="sxs-lookup"><span data-stu-id="89d9f-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="89d9f-114">EXEMPEL 3</span><span class="sxs-lookup"><span data-stu-id="89d9f-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="89d9f-115">Ta bort en nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="89d9f-115">Remove a network quota.</span></span>

## <span data-ttu-id="89d9f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89d9f-116">PARAMETERS</span></span>

### <span data-ttu-id="89d9f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="89d9f-117">-Name</span></span>
<span data-ttu-id="89d9f-118">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="89d9f-118">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d9f-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="89d9f-119">-Location</span></span>
<span data-ttu-id="89d9f-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="89d9f-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d9f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89d9f-121">-ResourceId</span></span>
<span data-ttu-id="89d9f-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="89d9f-122">The resource id.</span></span>

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

### <span data-ttu-id="89d9f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89d9f-123">-AsJob</span></span>
<span data-ttu-id="89d9f-124">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="89d9f-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="89d9f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="89d9f-125">-Force</span></span>
<span data-ttu-id="89d9f-126">Byt parameter för att inte fråga bekräfta.</span><span class="sxs-lookup"><span data-stu-id="89d9f-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="89d9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d9f-127">-WhatIf</span></span>
<span data-ttu-id="89d9f-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89d9f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d9f-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89d9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d9f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89d9f-130">-Confirm</span></span>
<span data-ttu-id="89d9f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89d9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d9f-132">CommonParameters</span></span>
<span data-ttu-id="89d9f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d9f-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d9f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d9f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89d9f-135">INPUTS</span></span>

## <span data-ttu-id="89d9f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89d9f-136">OUTPUTS</span></span>

## <span data-ttu-id="89d9f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89d9f-137">NOTES</span></span>

## <span data-ttu-id="89d9f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89d9f-138">RELATED LINKS</span></span>
