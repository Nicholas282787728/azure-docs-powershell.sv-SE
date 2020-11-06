---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: ecd801cff6a6cc67a4187e7f89b26e8b5edb3784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579415"
---
# <span data-ttu-id="aebce-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="aebce-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="aebce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aebce-102">SYNOPSIS</span></span>
<span data-ttu-id="aebce-103">Skapar ett ämnes jobb för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="aebce-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aebce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aebce-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aebce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aebce-105">DESCRIPTION</span></span>
<span data-ttu-id="aebce-106">Cmdleten **New-AzureRmSchedulerServiceBusTopicJob** skapar ett artikel jobb för Service Bus i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="aebce-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="aebce-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="aebce-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="aebce-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="aebce-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="aebce-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="aebce-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aebce-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="aebce-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aebce-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aebce-111">EXAMPLES</span></span>

## <span data-ttu-id="aebce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aebce-112">PARAMETERS</span></span>

### <span data-ttu-id="aebce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebce-113">-DefaultProfile</span></span>
<span data-ttu-id="aebce-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aebce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aebce-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="aebce-115">-EndTime</span></span>
<span data-ttu-id="aebce-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="aebce-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="aebce-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="aebce-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="aebce-118">-ErrorActionType</span></span>
<span data-ttu-id="aebce-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="aebce-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aebce-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aebce-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="aebce-121">Http</span></span> 
- <span data-ttu-id="aebce-122">Https</span><span class="sxs-lookup"><span data-stu-id="aebce-122">Https</span></span> 
- <span data-ttu-id="aebce-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="aebce-123">StorageQueue</span></span> 
- <span data-ttu-id="aebce-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="aebce-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="aebce-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="aebce-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="aebce-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="aebce-126">-ExecutionCount</span></span>
<span data-ttu-id="aebce-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="aebce-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="aebce-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="aebce-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="aebce-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="aebce-129">-Frequency</span></span>
<span data-ttu-id="aebce-130">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="aebce-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aebce-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aebce-132">Minut</span><span class="sxs-lookup"><span data-stu-id="aebce-132">Minute</span></span> 
- <span data-ttu-id="aebce-133">Timme</span><span class="sxs-lookup"><span data-stu-id="aebce-133">Hour</span></span> 
- <span data-ttu-id="aebce-134">Day</span><span class="sxs-lookup"><span data-stu-id="aebce-134">Day</span></span> 
- <span data-ttu-id="aebce-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="aebce-135">Week</span></span> 
- <span data-ttu-id="aebce-136">Månad</span><span class="sxs-lookup"><span data-stu-id="aebce-136">Month</span></span>

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

### <span data-ttu-id="aebce-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="aebce-137">-Interval</span></span>
<span data-ttu-id="aebce-138">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="aebce-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="aebce-139">-JobCollectionName</span></span>
<span data-ttu-id="aebce-140">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="aebce-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="aebce-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="aebce-141">-JobName</span></span>
<span data-ttu-id="aebce-142">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="aebce-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="aebce-143">-JobState</span></span>
<span data-ttu-id="aebce-144">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-144">Specifies the state of the job.</span></span>
<span data-ttu-id="aebce-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aebce-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aebce-146">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="aebce-146">Enabled</span></span> 
- <span data-ttu-id="aebce-147">Aktiv</span><span class="sxs-lookup"><span data-stu-id="aebce-147">Disabled</span></span>

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

### <span data-ttu-id="aebce-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aebce-148">-ResourceGroupName</span></span>
<span data-ttu-id="aebce-149">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="aebce-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="aebce-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="aebce-150">-ServiceBusMessage</span></span>
<span data-ttu-id="aebce-151">Anger ett avsnitts meddelande för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="aebce-151">Specifies a service bus topic message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="aebce-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="aebce-153">Anger ett Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="aebce-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="aebce-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="aebce-155">Anger ett namn på en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="aebce-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="aebce-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="aebce-157">Anger ett värde för en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="aebce-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="aebce-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="aebce-159">Anger sökvägen till en tjänst buss.</span><span class="sxs-lookup"><span data-stu-id="aebce-159">Specifies a service bus topic path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="aebce-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="aebce-161">Anger typen Service Bus transport.</span><span class="sxs-lookup"><span data-stu-id="aebce-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="aebce-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aebce-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aebce-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="aebce-163">NetMessaging</span></span>
- <span data-ttu-id="aebce-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="aebce-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebce-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="aebce-165">-StartTime</span></span>
<span data-ttu-id="aebce-166">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="aebce-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="aebce-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aebce-167">-Confirm</span></span>
<span data-ttu-id="aebce-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aebce-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aebce-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aebce-169">-WhatIf</span></span>
<span data-ttu-id="aebce-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aebce-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aebce-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aebce-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aebce-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebce-172">CommonParameters</span></span>
<span data-ttu-id="aebce-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aebce-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebce-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aebce-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebce-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aebce-175">INPUTS</span></span>

### <span data-ttu-id="aebce-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="aebce-176">None</span></span>
<span data-ttu-id="aebce-177">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="aebce-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aebce-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aebce-178">OUTPUTS</span></span>

### <span data-ttu-id="aebce-179">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="aebce-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="aebce-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aebce-180">NOTES</span></span>

## <span data-ttu-id="aebce-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aebce-181">RELATED LINKS</span></span>

[<span data-ttu-id="aebce-182">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="aebce-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="aebce-183">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="aebce-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="aebce-184">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="aebce-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="aebce-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="aebce-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="aebce-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="aebce-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="aebce-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="aebce-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="aebce-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="aebce-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="aebce-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="aebce-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="aebce-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="aebce-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


