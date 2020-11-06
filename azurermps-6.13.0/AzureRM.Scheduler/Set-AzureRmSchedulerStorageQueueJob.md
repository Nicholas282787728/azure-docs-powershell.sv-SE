---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: 68747f616971927ab719ec9ccc8eaf8bd9efc370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580707"
---
# <span data-ttu-id="2d531-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d531-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="2d531-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d531-102">SYNOPSIS</span></span>
<span data-ttu-id="2d531-103">Ändrar ett utskrifts jobb.</span><span class="sxs-lookup"><span data-stu-id="2d531-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d531-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d531-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d531-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d531-105">DESCRIPTION</span></span>
<span data-ttu-id="2d531-106">Cmdleten **set-AzureRmSchedulerStorageQueueJob** ändrar ett synkroniseringsjobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="2d531-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>
<span data-ttu-id="2d531-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="2d531-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="2d531-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="2d531-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="2d531-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="2d531-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2d531-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="2d531-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2d531-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d531-111">EXAMPLES</span></span>

## <span data-ttu-id="2d531-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d531-112">PARAMETERS</span></span>

### <span data-ttu-id="2d531-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d531-113">-DefaultProfile</span></span>
<span data-ttu-id="2d531-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d531-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d531-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="2d531-115">-EndTime</span></span>
<span data-ttu-id="2d531-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="2d531-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2d531-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d531-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="2d531-118">-ErrorActionType</span></span>
<span data-ttu-id="2d531-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="2d531-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2d531-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d531-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="2d531-121">Http</span></span> 
- <span data-ttu-id="2d531-122">Https</span><span class="sxs-lookup"><span data-stu-id="2d531-122">Https</span></span> 
- <span data-ttu-id="2d531-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d531-123">StorageQueue</span></span> 
- <span data-ttu-id="2d531-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2d531-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="2d531-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2d531-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d531-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="2d531-126">-ExecutionCount</span></span>
<span data-ttu-id="2d531-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="2d531-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="2d531-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="2d531-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="2d531-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="2d531-129">-Frequency</span></span>
<span data-ttu-id="2d531-130">Anger en frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="2d531-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2d531-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d531-132">Minut</span><span class="sxs-lookup"><span data-stu-id="2d531-132">Minute</span></span> 
- <span data-ttu-id="2d531-133">Timme</span><span class="sxs-lookup"><span data-stu-id="2d531-133">Hour</span></span> 
- <span data-ttu-id="2d531-134">Day</span><span class="sxs-lookup"><span data-stu-id="2d531-134">Day</span></span> 
- <span data-ttu-id="2d531-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="2d531-135">Week</span></span> 
- <span data-ttu-id="2d531-136">Månad</span><span class="sxs-lookup"><span data-stu-id="2d531-136">Month</span></span>

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

### <span data-ttu-id="2d531-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="2d531-137">-Interval</span></span>
<span data-ttu-id="2d531-138">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="2d531-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2d531-139">-JobCollectionName</span></span>
<span data-ttu-id="2d531-140">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="2d531-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="2d531-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="2d531-141">-JobName</span></span>
<span data-ttu-id="2d531-142">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="2d531-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2d531-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="2d531-143">-JobState</span></span>
<span data-ttu-id="2d531-144">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-144">Specifies the state of the job.</span></span>
<span data-ttu-id="2d531-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2d531-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d531-146">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="2d531-146">Enabled</span></span> 
- <span data-ttu-id="2d531-147">Aktiv</span><span class="sxs-lookup"><span data-stu-id="2d531-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d531-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d531-148">-ResourceGroupName</span></span>
<span data-ttu-id="2d531-149">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="2d531-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="2d531-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2d531-150">-StartTime</span></span>
<span data-ttu-id="2d531-151">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2d531-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d531-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="2d531-152">-StorageQueueAccount</span></span>
<span data-ttu-id="2d531-153">Anger ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="2d531-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="2d531-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="2d531-154">-StorageQueueMessage</span></span>
<span data-ttu-id="2d531-155">Anger ett Kömeddelanden för lagrings jobb.</span><span class="sxs-lookup"><span data-stu-id="2d531-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d531-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="2d531-156">-StorageQueueName</span></span>
<span data-ttu-id="2d531-157">Anger ett namn på en kölängd.</span><span class="sxs-lookup"><span data-stu-id="2d531-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="2d531-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="2d531-158">-StorageSASToken</span></span>
<span data-ttu-id="2d531-159">Anger ett delat åtkomsttoken för signaturer för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="2d531-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="2d531-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d531-160">-Confirm</span></span>
<span data-ttu-id="2d531-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d531-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d531-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d531-162">-WhatIf</span></span>
<span data-ttu-id="2d531-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d531-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d531-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d531-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d531-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d531-165">CommonParameters</span></span>
<span data-ttu-id="2d531-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d531-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d531-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d531-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d531-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d531-168">INPUTS</span></span>

### <span data-ttu-id="2d531-169">System. String</span><span class="sxs-lookup"><span data-stu-id="2d531-169">System.String</span></span>

## <span data-ttu-id="2d531-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d531-170">OUTPUTS</span></span>

### <span data-ttu-id="2d531-171">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2d531-171">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="2d531-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d531-172">NOTES</span></span>

## <span data-ttu-id="2d531-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d531-173">RELATED LINKS</span></span>

[<span data-ttu-id="2d531-174">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d531-174">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2d531-175">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2d531-175">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2d531-176">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d531-176">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2d531-177">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2d531-177">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="2d531-178">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d531-178">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="2d531-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="2d531-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="2d531-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2d531-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2d531-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d531-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="2d531-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="2d531-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


