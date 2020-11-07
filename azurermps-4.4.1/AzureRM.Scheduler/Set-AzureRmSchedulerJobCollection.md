---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756849"
---
# <span data-ttu-id="d850d-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d850d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d850d-102">SYNOPSIS</span></span>
<span data-ttu-id="d850d-103">Ändrar en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="d850d-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d850d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d850d-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d850d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d850d-105">DESCRIPTION</span></span>
<span data-ttu-id="d850d-106">Cmdleten **set-AzureRmSchedulerJobCollection** ändrar en Collection i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d850d-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d850d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d850d-107">EXAMPLES</span></span>

## <span data-ttu-id="d850d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d850d-108">PARAMETERS</span></span>

### <span data-ttu-id="d850d-109">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="d850d-109">-Frequency</span></span>
<span data-ttu-id="d850d-110">Anger den maximala frekvens som du kan ange för alla jobb i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="d850d-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="d850d-111">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d850d-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d850d-112">Minut</span><span class="sxs-lookup"><span data-stu-id="d850d-112">Minute</span></span> 
- <span data-ttu-id="d850d-113">Timme</span><span class="sxs-lookup"><span data-stu-id="d850d-113">Hour</span></span> 
- <span data-ttu-id="d850d-114">Day</span><span class="sxs-lookup"><span data-stu-id="d850d-114">Day</span></span> 
- <span data-ttu-id="d850d-115">Fjorton</span><span class="sxs-lookup"><span data-stu-id="d850d-115">Week</span></span> 
- <span data-ttu-id="d850d-116">Månad</span><span class="sxs-lookup"><span data-stu-id="d850d-116">Month</span></span>

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

### <span data-ttu-id="d850d-117">-Intervall</span><span class="sxs-lookup"><span data-stu-id="d850d-117">-Interval</span></span>
<span data-ttu-id="d850d-118">Anger ett intervall för återkommande.</span><span class="sxs-lookup"><span data-stu-id="d850d-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="d850d-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d850d-119">-JobCollectionName</span></span>
<span data-ttu-id="d850d-120">Anger namnet på en jobb samling.</span><span class="sxs-lookup"><span data-stu-id="d850d-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="d850d-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="d850d-121">-Location</span></span>
<span data-ttu-id="d850d-122">Anger det Azure-område där jobb samlingen finns.</span><span class="sxs-lookup"><span data-stu-id="d850d-122">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="d850d-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d850d-123">-MaxJobCount</span></span>
<span data-ttu-id="d850d-124">Anger maximalt antal jobb som du kan skapa i jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="d850d-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="d850d-125">Det maximala värdet beror på det abonnemang som anges i *plan* parametern.</span><span class="sxs-lookup"><span data-stu-id="d850d-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="d850d-126">-Planera</span><span class="sxs-lookup"><span data-stu-id="d850d-126">-Plan</span></span>
<span data-ttu-id="d850d-127">Anger projektplanen.</span><span class="sxs-lookup"><span data-stu-id="d850d-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="d850d-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d850d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d850d-129">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="d850d-129">Free</span></span> 
- <span data-ttu-id="d850d-130">Standar</span><span class="sxs-lookup"><span data-stu-id="d850d-130">Standard</span></span> 
- <span data-ttu-id="d850d-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="d850d-131">P10Premium</span></span> 
- <span data-ttu-id="d850d-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="d850d-132">P20Premium</span></span>

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

### <span data-ttu-id="d850d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d850d-133">-ResourceGroupName</span></span>
<span data-ttu-id="d850d-134">Anger resurs gruppen för jobb samlingen.</span><span class="sxs-lookup"><span data-stu-id="d850d-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d850d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d850d-135">-Confirm</span></span>
<span data-ttu-id="d850d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d850d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d850d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d850d-137">-WhatIf</span></span>
<span data-ttu-id="d850d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d850d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d850d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d850d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d850d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d850d-140">-DefaultProfile</span></span>
<span data-ttu-id="d850d-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d850d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d850d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d850d-142">CommonParameters</span></span>
<span data-ttu-id="d850d-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d850d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d850d-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d850d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d850d-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d850d-145">INPUTS</span></span>

## <span data-ttu-id="d850d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d850d-146">OUTPUTS</span></span>

### <span data-ttu-id="d850d-147">Microsoft. Azure. commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="d850d-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="d850d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d850d-148">NOTES</span></span>

## <span data-ttu-id="d850d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d850d-149">RELATED LINKS</span></span>

[<span data-ttu-id="d850d-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d850d-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d850d-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d850d-153">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d850d-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d850d-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


