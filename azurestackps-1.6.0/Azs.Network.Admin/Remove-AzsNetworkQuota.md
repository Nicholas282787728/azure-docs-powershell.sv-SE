---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572243"
---
# <span data-ttu-id="979a5-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="979a5-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="979a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="979a5-102">SYNOPSIS</span></span>
<span data-ttu-id="979a5-103">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="979a5-103">Delete a quota by name.</span></span>

## <span data-ttu-id="979a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="979a5-104">SYNTAX</span></span>

### <span data-ttu-id="979a5-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="979a5-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="979a5-106">ID</span><span class="sxs-lookup"><span data-stu-id="979a5-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="979a5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="979a5-107">DESCRIPTION</span></span>
<span data-ttu-id="979a5-108">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="979a5-108">Delete a quota by name.</span></span>

## <span data-ttu-id="979a5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="979a5-109">EXAMPLES</span></span>

### <span data-ttu-id="979a5-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="979a5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="979a5-111">Ta bort en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="979a5-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="979a5-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="979a5-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="979a5-113">Ta bort en nätverks kvot med en pipe.</span><span class="sxs-lookup"><span data-stu-id="979a5-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="979a5-114">--------------------------EXEMPEL 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="979a5-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="979a5-115">Ta bort en nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="979a5-115">Remove a network quota.</span></span>

## <span data-ttu-id="979a5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="979a5-116">PARAMETERS</span></span>

### <span data-ttu-id="979a5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="979a5-117">-AsJob</span></span>
<span data-ttu-id="979a5-118">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="979a5-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="979a5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="979a5-119">-Force</span></span>
<span data-ttu-id="979a5-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="979a5-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="979a5-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="979a5-121">-Location</span></span>
<span data-ttu-id="979a5-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="979a5-122">Location of the resource.</span></span>

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

### <span data-ttu-id="979a5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="979a5-123">-Name</span></span>
<span data-ttu-id="979a5-124">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="979a5-124">Name of the resource.</span></span>

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

### <span data-ttu-id="979a5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="979a5-125">-ResourceId</span></span>
<span data-ttu-id="979a5-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="979a5-126">The resource id.</span></span>

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

### <span data-ttu-id="979a5-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="979a5-127">-Confirm</span></span>
<span data-ttu-id="979a5-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="979a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="979a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979a5-129">-WhatIf</span></span>
<span data-ttu-id="979a5-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="979a5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="979a5-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="979a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="979a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979a5-132">CommonParameters</span></span>
<span data-ttu-id="979a5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979a5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979a5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="979a5-135">INPUTS</span></span>

## <span data-ttu-id="979a5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="979a5-136">OUTPUTS</span></span>

## <span data-ttu-id="979a5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="979a5-137">NOTES</span></span>

## <span data-ttu-id="979a5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="979a5-138">RELATED LINKS</span></span>

