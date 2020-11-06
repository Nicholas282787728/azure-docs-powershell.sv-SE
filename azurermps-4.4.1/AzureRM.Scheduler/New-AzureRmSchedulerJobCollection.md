---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582204"
---
# <span data-ttu-id="71aee-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="71aee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71aee-102">SYNOPSIS</span></span>
<span data-ttu-id="71aee-103">Skapar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="71aee-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71aee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71aee-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71aee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71aee-105">DESCRIPTION</span></span>
<span data-ttu-id="71aee-106">Cmdleten **New-AzureRmSchedulerJobCollection** skapar en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="71aee-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="71aee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71aee-107">EXAMPLES</span></span>

## <span data-ttu-id="71aee-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71aee-108">PARAMETERS</span></span>

### <span data-ttu-id="71aee-109">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="71aee-109">-Frequency</span></span>
<span data-ttu-id="71aee-110">Anger den maximala frekvens som du kan ange för alla jobb i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="71aee-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="71aee-111">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71aee-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71aee-112">Minut</span><span class="sxs-lookup"><span data-stu-id="71aee-112">Minute</span></span> 
- <span data-ttu-id="71aee-113">Timme</span><span class="sxs-lookup"><span data-stu-id="71aee-113">Hour</span></span> 
- <span data-ttu-id="71aee-114">Day</span><span class="sxs-lookup"><span data-stu-id="71aee-114">Day</span></span> 
- <span data-ttu-id="71aee-115">Fjorton</span><span class="sxs-lookup"><span data-stu-id="71aee-115">Week</span></span> 
- <span data-ttu-id="71aee-116">Månad</span><span class="sxs-lookup"><span data-stu-id="71aee-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-117">-Intervall</span><span class="sxs-lookup"><span data-stu-id="71aee-117">-Interval</span></span>
<span data-ttu-id="71aee-118">Anger ett intervall för återkommande.</span><span class="sxs-lookup"><span data-stu-id="71aee-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="71aee-119">-JobCollectionName</span></span>
<span data-ttu-id="71aee-120">Anger ett namn för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="71aee-120">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="71aee-121">-Location</span></span>
<span data-ttu-id="71aee-122">Anger det Azure-område där den här cmdleten skapar jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="71aee-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="71aee-123">-MaxJobCount</span></span>
<span data-ttu-id="71aee-124">Anger maximalt antal jobb som du kan skapa i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="71aee-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="71aee-125">Det maximala värdet beror på det abonnemang som anges i *plan* parametern.</span><span class="sxs-lookup"><span data-stu-id="71aee-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-126">-Planera</span><span class="sxs-lookup"><span data-stu-id="71aee-126">-Plan</span></span>
<span data-ttu-id="71aee-127">Anger projektplanen.</span><span class="sxs-lookup"><span data-stu-id="71aee-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="71aee-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71aee-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71aee-129">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="71aee-129">Free</span></span> 
- <span data-ttu-id="71aee-130">Standar</span><span class="sxs-lookup"><span data-stu-id="71aee-130">Standard</span></span> 
- <span data-ttu-id="71aee-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="71aee-131">P10Premium</span></span> 
- <span data-ttu-id="71aee-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="71aee-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71aee-133">-ResourceGroupName</span></span>
<span data-ttu-id="71aee-134">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="71aee-134">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71aee-135">-Confirm</span></span>
<span data-ttu-id="71aee-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71aee-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71aee-137">-WhatIf</span></span>
<span data-ttu-id="71aee-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71aee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71aee-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71aee-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71aee-140">-DefaultProfile</span></span>
<span data-ttu-id="71aee-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71aee-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71aee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71aee-142">CommonParameters</span></span>
<span data-ttu-id="71aee-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71aee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71aee-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71aee-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71aee-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71aee-145">INPUTS</span></span>

## <span data-ttu-id="71aee-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71aee-146">OUTPUTS</span></span>

### <span data-ttu-id="71aee-147">Microsoft. Azure. commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="71aee-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="71aee-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71aee-148">NOTES</span></span>

## <span data-ttu-id="71aee-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71aee-149">RELATED LINKS</span></span>

[<span data-ttu-id="71aee-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="71aee-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="71aee-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="71aee-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="71aee-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="71aee-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


