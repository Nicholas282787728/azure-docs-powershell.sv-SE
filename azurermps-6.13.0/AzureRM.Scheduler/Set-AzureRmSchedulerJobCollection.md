---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 535455f73795d85acf05da191694f35dbeee9ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576090"
---
# <span data-ttu-id="27005-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="27005-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27005-102">SYNOPSIS</span></span>
<span data-ttu-id="27005-103">Ändrar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="27005-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27005-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27005-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27005-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27005-105">DESCRIPTION</span></span>
<span data-ttu-id="27005-106">Cmdleten **set-AzureRmSchedulerJobCollection** ändrar en Collection i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="27005-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="27005-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27005-107">EXAMPLES</span></span>

## <span data-ttu-id="27005-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27005-108">PARAMETERS</span></span>

### <span data-ttu-id="27005-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27005-109">-DefaultProfile</span></span>
<span data-ttu-id="27005-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27005-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27005-111">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="27005-111">-Frequency</span></span>
<span data-ttu-id="27005-112">Anger den maximala frekvens som du kan ange för alla jobb i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="27005-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="27005-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="27005-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27005-114">Minut</span><span class="sxs-lookup"><span data-stu-id="27005-114">Minute</span></span> 
- <span data-ttu-id="27005-115">Timme</span><span class="sxs-lookup"><span data-stu-id="27005-115">Hour</span></span> 
- <span data-ttu-id="27005-116">Day</span><span class="sxs-lookup"><span data-stu-id="27005-116">Day</span></span> 
- <span data-ttu-id="27005-117">Fjorton</span><span class="sxs-lookup"><span data-stu-id="27005-117">Week</span></span> 
- <span data-ttu-id="27005-118">Månad</span><span class="sxs-lookup"><span data-stu-id="27005-118">Month</span></span>

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

### <span data-ttu-id="27005-119">-Intervall</span><span class="sxs-lookup"><span data-stu-id="27005-119">-Interval</span></span>
<span data-ttu-id="27005-120">Anger ett intervall för återkommande.</span><span class="sxs-lookup"><span data-stu-id="27005-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="27005-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="27005-121">-JobCollectionName</span></span>
<span data-ttu-id="27005-122">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="27005-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="27005-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="27005-123">-Location</span></span>
<span data-ttu-id="27005-124">Anger det Azure-område där jobb samlingen finns.</span><span class="sxs-lookup"><span data-stu-id="27005-124">Specifies the Azure region in which the job collection exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27005-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="27005-125">-MaxJobCount</span></span>
<span data-ttu-id="27005-126">Anger maximalt antal jobb som du kan skapa i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="27005-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="27005-127">Det maximala värdet beror på det abonnemang som anges i *plan* parametern.</span><span class="sxs-lookup"><span data-stu-id="27005-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="27005-128">-Planera</span><span class="sxs-lookup"><span data-stu-id="27005-128">-Plan</span></span>
<span data-ttu-id="27005-129">Anger projektplanen.</span><span class="sxs-lookup"><span data-stu-id="27005-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="27005-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="27005-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27005-131">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="27005-131">Free</span></span> 
- <span data-ttu-id="27005-132">Standar</span><span class="sxs-lookup"><span data-stu-id="27005-132">Standard</span></span> 
- <span data-ttu-id="27005-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="27005-133">P10Premium</span></span> 
- <span data-ttu-id="27005-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="27005-134">P20Premium</span></span>

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

### <span data-ttu-id="27005-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27005-135">-ResourceGroupName</span></span>
<span data-ttu-id="27005-136">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="27005-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="27005-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27005-137">-Confirm</span></span>
<span data-ttu-id="27005-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27005-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27005-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27005-139">-WhatIf</span></span>
<span data-ttu-id="27005-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27005-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27005-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27005-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27005-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27005-142">CommonParameters</span></span>
<span data-ttu-id="27005-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27005-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27005-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27005-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27005-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27005-145">INPUTS</span></span>

### <span data-ttu-id="27005-146">System. String</span><span class="sxs-lookup"><span data-stu-id="27005-146">System.String</span></span>

## <span data-ttu-id="27005-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27005-147">OUTPUTS</span></span>

### <span data-ttu-id="27005-148">Microsoft. Azure. commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="27005-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="27005-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27005-149">NOTES</span></span>

## <span data-ttu-id="27005-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27005-150">RELATED LINKS</span></span>

[<span data-ttu-id="27005-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="27005-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="27005-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="27005-154">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-154">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="27005-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="27005-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


