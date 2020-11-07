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
ms.locfileid: "93920955"
---
# <span data-ttu-id="6a7c6-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6a7c6-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="6a7c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7c6-103">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-103">Delete a quota by name.</span></span>

## <span data-ttu-id="6a7c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a7c6-104">SYNTAX</span></span>

### <span data-ttu-id="6a7c6-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="6a7c6-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a7c6-106">ID</span><span class="sxs-lookup"><span data-stu-id="6a7c6-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a7c6-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7c6-108">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-108">Delete a quota by name.</span></span>

## <span data-ttu-id="6a7c6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a7c6-109">EXAMPLES</span></span>

### <span data-ttu-id="6a7c6-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a7c6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6a7c6-111">Ta bort en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="6a7c6-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a7c6-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="6a7c6-113">Ta bort en nätverks kvot med en pipe.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="6a7c6-114">--------------------------EXEMPEL 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a7c6-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6a7c6-115">Ta bort en nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-115">Remove a network quota.</span></span>

## <span data-ttu-id="6a7c6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a7c6-116">PARAMETERS</span></span>

### <span data-ttu-id="6a7c6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a7c6-117">-AsJob</span></span>
<span data-ttu-id="6a7c6-118">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6a7c6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6a7c6-119">-Force</span></span>
<span data-ttu-id="6a7c6-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6a7c6-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a7c6-121">-Location</span></span>
<span data-ttu-id="6a7c6-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-122">Location of the resource.</span></span>

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

### <span data-ttu-id="6a7c6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a7c6-123">-Name</span></span>
<span data-ttu-id="6a7c6-124">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-124">Name of the resource.</span></span>

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

### <span data-ttu-id="6a7c6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7c6-125">-ResourceId</span></span>
<span data-ttu-id="6a7c6-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-126">The resource id.</span></span>

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

### <span data-ttu-id="6a7c6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a7c6-127">-Confirm</span></span>
<span data-ttu-id="6a7c6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7c6-129">-WhatIf</span></span>
<span data-ttu-id="6a7c6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7c6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7c6-132">CommonParameters</span></span>
<span data-ttu-id="6a7c6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7c6-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7c6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7c6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a7c6-135">INPUTS</span></span>

## <span data-ttu-id="6a7c6-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a7c6-136">OUTPUTS</span></span>

## <span data-ttu-id="6a7c6-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a7c6-137">NOTES</span></span>

## <span data-ttu-id="6a7c6-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a7c6-138">RELATED LINKS</span></span>

