---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 6f1e92654c038cccf49e32b489ad5face70ae011
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758310"
---
# <span data-ttu-id="31ab9-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="31ab9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="31ab9-103">Ändrar ett ämne i Service Bus.</span><span class="sxs-lookup"><span data-stu-id="31ab9-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ab9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31ab9-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ab9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="31ab9-106">Cmdleten **set-AzureRmSchedulerServiceBusTopicJob** ändrar en tjänst Bus ämne i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="31ab9-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>
<span data-ttu-id="31ab9-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="31ab9-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="31ab9-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="31ab9-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="31ab9-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="31ab9-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="31ab9-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="31ab9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31ab9-111">EXAMPLES</span></span>

## <span data-ttu-id="31ab9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31ab9-112">PARAMETERS</span></span>

### <span data-ttu-id="31ab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ab9-113">-DefaultProfile</span></span>
<span data-ttu-id="31ab9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31ab9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ab9-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="31ab9-115">-EndTime</span></span>
<span data-ttu-id="31ab9-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="31ab9-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="31ab9-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="31ab9-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="31ab9-118">-ErrorActionType</span></span>
<span data-ttu-id="31ab9-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="31ab9-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31ab9-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31ab9-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="31ab9-121">Http</span></span> 
- <span data-ttu-id="31ab9-122">Https</span><span class="sxs-lookup"><span data-stu-id="31ab9-122">Https</span></span> 
- <span data-ttu-id="31ab9-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="31ab9-123">StorageQueue</span></span> 
- <span data-ttu-id="31ab9-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="31ab9-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="31ab9-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="31ab9-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="31ab9-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="31ab9-126">-ExecutionCount</span></span>
<span data-ttu-id="31ab9-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="31ab9-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="31ab9-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="31ab9-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="31ab9-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="31ab9-129">-Frequency</span></span>
<span data-ttu-id="31ab9-130">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="31ab9-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31ab9-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31ab9-132">Minut</span><span class="sxs-lookup"><span data-stu-id="31ab9-132">Minute</span></span> 
- <span data-ttu-id="31ab9-133">Timme</span><span class="sxs-lookup"><span data-stu-id="31ab9-133">Hour</span></span> 
- <span data-ttu-id="31ab9-134">Day</span><span class="sxs-lookup"><span data-stu-id="31ab9-134">Day</span></span> 
- <span data-ttu-id="31ab9-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="31ab9-135">Week</span></span> 
- <span data-ttu-id="31ab9-136">Månad</span><span class="sxs-lookup"><span data-stu-id="31ab9-136">Month</span></span>

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

### <span data-ttu-id="31ab9-137">-Intervall</span><span class="sxs-lookup"><span data-stu-id="31ab9-137">-Interval</span></span>
<span data-ttu-id="31ab9-138">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="31ab9-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="31ab9-139">-JobCollectionName</span></span>
<span data-ttu-id="31ab9-140">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="31ab9-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="31ab9-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="31ab9-141">-JobName</span></span>
<span data-ttu-id="31ab9-142">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="31ab9-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31ab9-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="31ab9-143">-JobState</span></span>
<span data-ttu-id="31ab9-144">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-144">Specifies the state of the job.</span></span>
<span data-ttu-id="31ab9-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31ab9-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31ab9-146">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="31ab9-146">Enabled</span></span> 
- <span data-ttu-id="31ab9-147">Aktiv</span><span class="sxs-lookup"><span data-stu-id="31ab9-147">Disabled</span></span>

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

### <span data-ttu-id="31ab9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ab9-148">-ResourceGroupName</span></span>
<span data-ttu-id="31ab9-149">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="31ab9-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="31ab9-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="31ab9-150">-ServiceBusMessage</span></span>
<span data-ttu-id="31ab9-151">Anger ett avsnitts meddelande för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="31ab9-151">Specifies a service bus topic message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="31ab9-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="31ab9-153">Anger ett Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="31ab9-153">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="31ab9-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="31ab9-155">Anger ett namn på en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="31ab9-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="31ab9-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="31ab9-157">Anger ett värde för en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="31ab9-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="31ab9-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="31ab9-159">Anger sökvägen till en tjänst buss.</span><span class="sxs-lookup"><span data-stu-id="31ab9-159">Specifies a service bus topic path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="31ab9-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="31ab9-161">Anger typen Service Bus transport.</span><span class="sxs-lookup"><span data-stu-id="31ab9-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="31ab9-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31ab9-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31ab9-163">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="31ab9-163">NetMessaging</span></span>
- <span data-ttu-id="31ab9-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="31ab9-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ab9-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="31ab9-165">-StartTime</span></span>
<span data-ttu-id="31ab9-166">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="31ab9-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="31ab9-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31ab9-167">-Confirm</span></span>
<span data-ttu-id="31ab9-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31ab9-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ab9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ab9-169">-WhatIf</span></span>
<span data-ttu-id="31ab9-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31ab9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ab9-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31ab9-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ab9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ab9-172">CommonParameters</span></span>
<span data-ttu-id="31ab9-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ab9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ab9-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ab9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ab9-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31ab9-175">INPUTS</span></span>

### <span data-ttu-id="31ab9-176">System. String</span><span class="sxs-lookup"><span data-stu-id="31ab9-176">System.String</span></span>

## <span data-ttu-id="31ab9-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31ab9-177">OUTPUTS</span></span>

### <span data-ttu-id="31ab9-178">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="31ab9-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="31ab9-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31ab9-179">NOTES</span></span>

## <span data-ttu-id="31ab9-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31ab9-180">RELATED LINKS</span></span>

[<span data-ttu-id="31ab9-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="31ab9-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31ab9-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="31ab9-183">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-183">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="31ab9-184">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="31ab9-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="31ab9-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="31ab9-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="31ab9-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="31ab9-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="31ab9-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="31ab9-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


