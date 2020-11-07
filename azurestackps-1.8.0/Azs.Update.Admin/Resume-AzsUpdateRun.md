---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921288"
---
# <span data-ttu-id="cee6b-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="cee6b-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="cee6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cee6b-103">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cee6b-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="cee6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cee6b-104">SYNTAX</span></span>

### <span data-ttu-id="cee6b-105">UpdateRuns_Rerun (standard)</span><span class="sxs-lookup"><span data-stu-id="cee6b-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee6b-106">ID</span><span class="sxs-lookup"><span data-stu-id="cee6b-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee6b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cee6b-107">DESCRIPTION</span></span>
<span data-ttu-id="cee6b-108">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cee6b-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="cee6b-109">Återupptade uppdaterings körningar fortsätter vid den tidpunkt då de senast misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cee6b-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="cee6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cee6b-110">EXAMPLES</span></span>

### <span data-ttu-id="cee6b-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="cee6b-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="cee6b-112">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="cee6b-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="cee6b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cee6b-113">PARAMETERS</span></span>

### <span data-ttu-id="cee6b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="cee6b-114">-Name</span></span>
<span data-ttu-id="cee6b-115">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="cee6b-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee6b-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="cee6b-116">-Location</span></span>
<span data-ttu-id="cee6b-117">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="cee6b-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee6b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee6b-118">-ResourceGroupName</span></span>
<span data-ttu-id="cee6b-119">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="cee6b-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee6b-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="cee6b-120">-UpdateName</span></span>
<span data-ttu-id="cee6b-121">Visnings namn för uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="cee6b-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee6b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cee6b-122">-AsJob</span></span>
<span data-ttu-id="cee6b-123">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="cee6b-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cee6b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cee6b-124">-ResourceId</span></span>
<span data-ttu-id="cee6b-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cee6b-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cee6b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cee6b-126">-Force</span></span>
<span data-ttu-id="cee6b-127">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cee6b-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="cee6b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee6b-128">-WhatIf</span></span>
<span data-ttu-id="cee6b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cee6b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee6b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cee6b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee6b-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cee6b-131">-Confirm</span></span>
<span data-ttu-id="cee6b-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cee6b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee6b-133">CommonParameters</span></span>
<span data-ttu-id="cee6b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee6b-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee6b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee6b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cee6b-136">INPUTS</span></span>

## <span data-ttu-id="cee6b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cee6b-137">OUTPUTS</span></span>

## <span data-ttu-id="cee6b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cee6b-138">NOTES</span></span>

## <span data-ttu-id="cee6b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cee6b-139">RELATED LINKS</span></span>
