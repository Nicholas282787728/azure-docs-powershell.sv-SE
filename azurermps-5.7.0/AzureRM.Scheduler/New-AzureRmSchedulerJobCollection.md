---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: dfec2d79d092a5f119daa558b1d383f1a1d71df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576415"
---
# <span data-ttu-id="fddf4-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="fddf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fddf4-102">SYNOPSIS</span></span>
<span data-ttu-id="fddf4-103">Skapar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="fddf4-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fddf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fddf4-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fddf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fddf4-105">DESCRIPTION</span></span>
<span data-ttu-id="fddf4-106">Cmdleten **New-AzureRmSchedulerJobCollection** skapar en jobb samling i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="fddf4-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="fddf4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fddf4-107">EXAMPLES</span></span>

## <span data-ttu-id="fddf4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fddf4-108">PARAMETERS</span></span>

### <span data-ttu-id="fddf4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddf4-109">-DefaultProfile</span></span>
<span data-ttu-id="fddf4-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fddf4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-111">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="fddf4-111">-Frequency</span></span>
<span data-ttu-id="fddf4-112">Anger den maximala frekvens som du kan ange för alla jobb i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="fddf4-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fddf4-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fddf4-114">Minut</span><span class="sxs-lookup"><span data-stu-id="fddf4-114">Minute</span></span> 
- <span data-ttu-id="fddf4-115">Timme</span><span class="sxs-lookup"><span data-stu-id="fddf4-115">Hour</span></span> 
- <span data-ttu-id="fddf4-116">Day</span><span class="sxs-lookup"><span data-stu-id="fddf4-116">Day</span></span> 
- <span data-ttu-id="fddf4-117">Fjorton</span><span class="sxs-lookup"><span data-stu-id="fddf4-117">Week</span></span> 
- <span data-ttu-id="fddf4-118">Månad</span><span class="sxs-lookup"><span data-stu-id="fddf4-118">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-119">-Intervall</span><span class="sxs-lookup"><span data-stu-id="fddf4-119">-Interval</span></span>
<span data-ttu-id="fddf4-120">Anger ett intervall för återkommande.</span><span class="sxs-lookup"><span data-stu-id="fddf4-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fddf4-121">-JobCollectionName</span></span>
<span data-ttu-id="fddf4-122">Anger ett namn för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-122">Specifies a name for the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="fddf4-123">-Location</span></span>
<span data-ttu-id="fddf4-124">Anger det Azure-område där den här cmdleten skapar jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="fddf4-125">-MaxJobCount</span></span>
<span data-ttu-id="fddf4-126">Anger maximalt antal jobb som du kan skapa i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="fddf4-127">Det maximala värdet beror på det abonnemang som anges i *plan* parametern.</span><span class="sxs-lookup"><span data-stu-id="fddf4-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-128">-Planera</span><span class="sxs-lookup"><span data-stu-id="fddf4-128">-Plan</span></span>
<span data-ttu-id="fddf4-129">Anger projektplanen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="fddf4-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fddf4-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fddf4-131">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="fddf4-131">Free</span></span> 
- <span data-ttu-id="fddf4-132">Standar</span><span class="sxs-lookup"><span data-stu-id="fddf4-132">Standard</span></span> 
- <span data-ttu-id="fddf4-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="fddf4-133">P10Premium</span></span> 
- <span data-ttu-id="fddf4-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="fddf4-134">P20Premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddf4-135">-ResourceGroupName</span></span>
<span data-ttu-id="fddf4-136">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="fddf4-136">Specifies the resource group for the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fddf4-137">-Confirm</span></span>
<span data-ttu-id="fddf4-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fddf4-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fddf4-139">-WhatIf</span></span>
<span data-ttu-id="fddf4-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fddf4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fddf4-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fddf4-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddf4-142">CommonParameters</span></span>
<span data-ttu-id="fddf4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fddf4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddf4-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fddf4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddf4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fddf4-145">INPUTS</span></span>

### <span data-ttu-id="fddf4-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="fddf4-146">None</span></span>
<span data-ttu-id="fddf4-147">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fddf4-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fddf4-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fddf4-148">OUTPUTS</span></span>

### <span data-ttu-id="fddf4-149">Microsoft. Azure. commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="fddf4-149">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="fddf4-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fddf4-150">NOTES</span></span>

## <span data-ttu-id="fddf4-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fddf4-151">RELATED LINKS</span></span>

[<span data-ttu-id="fddf4-152">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-152">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fddf4-153">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-153">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fddf4-154">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-154">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fddf4-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fddf4-156">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fddf4-156">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


