---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921051"
---
# <span data-ttu-id="0507f-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="0507f-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="0507f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0507f-102">SYNOPSIS</span></span>
<span data-ttu-id="0507f-103">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="0507f-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="0507f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0507f-104">SYNTAX</span></span>

### <span data-ttu-id="0507f-105">UpdateRuns_Rerun (standard)</span><span class="sxs-lookup"><span data-stu-id="0507f-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0507f-106">ID</span><span class="sxs-lookup"><span data-stu-id="0507f-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0507f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0507f-107">DESCRIPTION</span></span>
<span data-ttu-id="0507f-108">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="0507f-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="0507f-109">Återupptade uppdaterings körningar fortsätter vid den tidpunkt då de senast misslyckades.</span><span class="sxs-lookup"><span data-stu-id="0507f-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="0507f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0507f-110">EXAMPLES</span></span>

### <span data-ttu-id="0507f-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0507f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="0507f-112">Återupptar en tidigare startad uppdaterings körning som misslyckades.</span><span class="sxs-lookup"><span data-stu-id="0507f-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="0507f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0507f-113">PARAMETERS</span></span>

### <span data-ttu-id="0507f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0507f-114">-AsJob</span></span>
<span data-ttu-id="0507f-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="0507f-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0507f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0507f-116">-Force</span></span>
<span data-ttu-id="0507f-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0507f-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0507f-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="0507f-118">-Location</span></span>
<span data-ttu-id="0507f-119">Namnet på uppdaterings platsen.</span><span class="sxs-lookup"><span data-stu-id="0507f-119">The name of the update location.</span></span>

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

### <span data-ttu-id="0507f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0507f-120">-Name</span></span>
<span data-ttu-id="0507f-121">Uppdatera kör-ID.</span><span class="sxs-lookup"><span data-stu-id="0507f-121">Update run identifier.</span></span>

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

### <span data-ttu-id="0507f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0507f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0507f-123">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="0507f-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0507f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0507f-124">-ResourceId</span></span>
<span data-ttu-id="0507f-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0507f-125">The resource id.</span></span>

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

### <span data-ttu-id="0507f-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="0507f-126">-UpdateName</span></span>
<span data-ttu-id="0507f-127">Visnings namn för uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="0507f-127">Display name of the update.</span></span>

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

### <span data-ttu-id="0507f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0507f-128">-Confirm</span></span>
<span data-ttu-id="0507f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0507f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0507f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0507f-130">-WhatIf</span></span>
<span data-ttu-id="0507f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0507f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0507f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0507f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0507f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0507f-133">CommonParameters</span></span>
<span data-ttu-id="0507f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0507f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0507f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0507f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0507f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0507f-136">INPUTS</span></span>

## <span data-ttu-id="0507f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0507f-137">OUTPUTS</span></span>

## <span data-ttu-id="0507f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0507f-138">NOTES</span></span>

## <span data-ttu-id="0507f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0507f-139">RELATED LINKS</span></span>

