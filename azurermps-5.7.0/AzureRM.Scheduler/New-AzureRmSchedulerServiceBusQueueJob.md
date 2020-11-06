---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 7b6596d967d603a3dcecb3d20f9d2396fc00adf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579416"
---
# <span data-ttu-id="cb15a-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="cb15a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb15a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb15a-103">Skapar ett Service Bus-köjobb.</span><span class="sxs-lookup"><span data-stu-id="cb15a-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb15a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb15a-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb15a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb15a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb15a-106">Cmdleten **New-AzureRmSchedulerServiceBusQueueJob** skapar ett Service Bus Queue-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="cb15a-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="cb15a-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="cb15a-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="cb15a-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="cb15a-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="cb15a-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cb15a-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb15a-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb15a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb15a-111">EXAMPLES</span></span>

## <span data-ttu-id="cb15a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb15a-112">PARAMETERS</span></span>

### <span data-ttu-id="cb15a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb15a-113">-DefaultProfile</span></span>
<span data-ttu-id="cb15a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb15a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb15a-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="cb15a-115">-EndTime</span></span>
<span data-ttu-id="cb15a-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="cb15a-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="cb15a-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cb15a-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="cb15a-118">-ErrorActionType</span></span>
<span data-ttu-id="cb15a-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="cb15a-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cb15a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb15a-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="cb15a-121">Http</span></span> 
- <span data-ttu-id="cb15a-122">Https</span><span class="sxs-lookup"><span data-stu-id="cb15a-122">Https</span></span> 
- <span data-ttu-id="cb15a-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="cb15a-123">StorageQueue</span></span> 
- <span data-ttu-id="cb15a-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="cb15a-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="cb15a-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="cb15a-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="cb15a-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="cb15a-126">-ExecutionCount</span></span>
<span data-ttu-id="cb15a-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="cb15a-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="cb15a-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="cb15a-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="cb15a-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="cb15a-129">-Frequency</span></span>
<span data-ttu-id="cb15a-130">Anger en frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="cb15a-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cb15a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb15a-132">Minut</span><span class="sxs-lookup"><span data-stu-id="cb15a-132">Minute</span></span> 
- <span data-ttu-id="cb15a-133">Timme</span><span class="sxs-lookup"><span data-stu-id="cb15a-133">Hour</span></span> 
- <span data-ttu-id="cb15a-134">Day</span><span class="sxs-lookup"><span data-stu-id="cb15a-134">Day</span></span> 
- <span data-ttu-id="cb15a-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="cb15a-135">Week</span></span> 
- <span data-ttu-id="cb15a-136">Månad</span><span class="sxs-lookup"><span data-stu-id="cb15a-136">Month</span></span>

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

### <span data-ttu-id="cb15a-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="cb15a-137">-Interval</span></span>
<span data-ttu-id="cb15a-138">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="cb15a-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="cb15a-139">-JobCollectionName</span></span>
<span data-ttu-id="cb15a-140">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="cb15a-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="cb15a-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="cb15a-141">-JobName</span></span>
<span data-ttu-id="cb15a-142">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="cb15a-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="cb15a-143">-JobState</span></span>
<span data-ttu-id="cb15a-144">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-144">Specifies the state of the job.</span></span>
<span data-ttu-id="cb15a-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cb15a-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb15a-146">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="cb15a-146">Enabled</span></span> 
- <span data-ttu-id="cb15a-147">Aktiv</span><span class="sxs-lookup"><span data-stu-id="cb15a-147">Disabled</span></span>

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

### <span data-ttu-id="cb15a-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb15a-148">-ResourceGroupName</span></span>
<span data-ttu-id="cb15a-149">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="cb15a-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="cb15a-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="cb15a-150">-ServiceBusMessage</span></span>
<span data-ttu-id="cb15a-151">Anger ett Service Bus Queue-meddelande.</span><span class="sxs-lookup"><span data-stu-id="cb15a-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="cb15a-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="cb15a-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="cb15a-153">Anger ett Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="cb15a-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="cb15a-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="cb15a-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="cb15a-155">Anger namnet på en Service Bus-kö.</span><span class="sxs-lookup"><span data-stu-id="cb15a-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="cb15a-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="cb15a-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="cb15a-157">Anger ett namn på en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cb15a-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="cb15a-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="cb15a-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="cb15a-159">Anger ett värde för en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cb15a-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="cb15a-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="cb15a-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="cb15a-161">Anger typen Service Bus transport.</span><span class="sxs-lookup"><span data-stu-id="cb15a-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="cb15a-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cb15a-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb15a-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="cb15a-163">NetMessaging</span></span> 
- <span data-ttu-id="cb15a-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="cb15a-164">AMQP</span></span>

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

### <span data-ttu-id="cb15a-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cb15a-165">-StartTime</span></span>
<span data-ttu-id="cb15a-166">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cb15a-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="cb15a-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb15a-167">-Confirm</span></span>
<span data-ttu-id="cb15a-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb15a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb15a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb15a-169">-WhatIf</span></span>
<span data-ttu-id="cb15a-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb15a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb15a-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb15a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb15a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb15a-172">CommonParameters</span></span>
<span data-ttu-id="cb15a-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb15a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb15a-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb15a-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb15a-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb15a-175">INPUTS</span></span>

### <span data-ttu-id="cb15a-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="cb15a-176">None</span></span>
<span data-ttu-id="cb15a-177">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cb15a-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb15a-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb15a-178">OUTPUTS</span></span>

### <span data-ttu-id="cb15a-179">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cb15a-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="cb15a-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb15a-180">NOTES</span></span>

## <span data-ttu-id="cb15a-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb15a-181">RELATED LINKS</span></span>

[<span data-ttu-id="cb15a-182">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="cb15a-183">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb15a-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb15a-184">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="cb15a-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="cb15a-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="cb15a-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="cb15a-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="cb15a-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="cb15a-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="cb15a-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="cb15a-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


