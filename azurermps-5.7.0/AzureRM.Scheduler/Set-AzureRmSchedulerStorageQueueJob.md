---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755371"
---
# <span data-ttu-id="97ec1-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="97ec1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="97ec1-103">Ändrar ett utskrifts jobb.</span><span class="sxs-lookup"><span data-stu-id="97ec1-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ec1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97ec1-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97ec1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="97ec1-106">Cmdleten **set-AzureRmSchedulerStorageQueueJob** ändrar ett synkroniseringsjobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="97ec1-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="97ec1-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="97ec1-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="97ec1-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="97ec1-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="97ec1-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="97ec1-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="97ec1-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="97ec1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97ec1-111">EXAMPLES</span></span>

## <span data-ttu-id="97ec1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97ec1-112">PARAMETERS</span></span>

### <span data-ttu-id="97ec1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ec1-113">-DefaultProfile</span></span>
<span data-ttu-id="97ec1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97ec1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97ec1-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="97ec1-115">-EndTime</span></span>
<span data-ttu-id="97ec1-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="97ec1-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="97ec1-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="97ec1-118">-ErrorActionType</span></span>
<span data-ttu-id="97ec1-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="97ec1-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="97ec1-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97ec1-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="97ec1-121">Http</span></span> 
- <span data-ttu-id="97ec1-122">Https</span><span class="sxs-lookup"><span data-stu-id="97ec1-122">Https</span></span> 
- <span data-ttu-id="97ec1-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="97ec1-123">StorageQueue</span></span> 
- <span data-ttu-id="97ec1-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="97ec1-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="97ec1-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="97ec1-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="97ec1-126">-ExecutionCount</span></span>
<span data-ttu-id="97ec1-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="97ec1-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="97ec1-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="97ec1-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="97ec1-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="97ec1-129">-Frequency</span></span>
<span data-ttu-id="97ec1-130">Anger en frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="97ec1-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="97ec1-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97ec1-132">Minut</span><span class="sxs-lookup"><span data-stu-id="97ec1-132">Minute</span></span> 
- <span data-ttu-id="97ec1-133">Timme</span><span class="sxs-lookup"><span data-stu-id="97ec1-133">Hour</span></span> 
- <span data-ttu-id="97ec1-134">Day</span><span class="sxs-lookup"><span data-stu-id="97ec1-134">Day</span></span> 
- <span data-ttu-id="97ec1-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="97ec1-135">Week</span></span> 
- <span data-ttu-id="97ec1-136">Månad</span><span class="sxs-lookup"><span data-stu-id="97ec1-136">Month</span></span>

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

### <span data-ttu-id="97ec1-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="97ec1-137">-Interval</span></span>
<span data-ttu-id="97ec1-138">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="97ec1-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="97ec1-139">-JobCollectionName</span></span>
<span data-ttu-id="97ec1-140">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="97ec1-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="97ec1-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="97ec1-141">-JobName</span></span>
<span data-ttu-id="97ec1-142">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="97ec1-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97ec1-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="97ec1-143">-JobState</span></span>
<span data-ttu-id="97ec1-144">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-144">Specifies the state of the job.</span></span>
<span data-ttu-id="97ec1-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="97ec1-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97ec1-146">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="97ec1-146">Enabled</span></span> 
- <span data-ttu-id="97ec1-147">Aktiv</span><span class="sxs-lookup"><span data-stu-id="97ec1-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ec1-148">-ResourceGroupName</span></span>
<span data-ttu-id="97ec1-149">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="97ec1-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="97ec1-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="97ec1-150">-StartTime</span></span>
<span data-ttu-id="97ec1-151">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="97ec1-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="97ec1-152">-StorageQueueAccount</span></span>
<span data-ttu-id="97ec1-153">Anger ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="97ec1-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="97ec1-154">-StorageQueueMessage</span></span>
<span data-ttu-id="97ec1-155">Anger ett Kömeddelanden för lagrings jobb.</span><span class="sxs-lookup"><span data-stu-id="97ec1-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="97ec1-156">-StorageQueueName</span></span>
<span data-ttu-id="97ec1-157">Anger ett namn på en kölängd.</span><span class="sxs-lookup"><span data-stu-id="97ec1-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="97ec1-158">-StorageSASToken</span></span>
<span data-ttu-id="97ec1-159">Anger ett delat åtkomsttoken för signaturer för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="97ec1-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ec1-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97ec1-160">-Confirm</span></span>
<span data-ttu-id="97ec1-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97ec1-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ec1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ec1-162">-WhatIf</span></span>
<span data-ttu-id="97ec1-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97ec1-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ec1-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97ec1-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ec1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ec1-165">CommonParameters</span></span>
<span data-ttu-id="97ec1-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ec1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ec1-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ec1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ec1-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97ec1-168">INPUTS</span></span>

### <span data-ttu-id="97ec1-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="97ec1-169">None</span></span>
<span data-ttu-id="97ec1-170">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="97ec1-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97ec1-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97ec1-171">OUTPUTS</span></span>

### <span data-ttu-id="97ec1-172">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="97ec1-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="97ec1-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97ec1-173">NOTES</span></span>

## <span data-ttu-id="97ec1-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97ec1-174">RELATED LINKS</span></span>

[<span data-ttu-id="97ec1-175">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="97ec1-176">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="97ec1-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="97ec1-177">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="97ec1-178">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="97ec1-179">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="97ec1-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="97ec1-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="97ec1-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="97ec1-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="97ec1-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="97ec1-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


