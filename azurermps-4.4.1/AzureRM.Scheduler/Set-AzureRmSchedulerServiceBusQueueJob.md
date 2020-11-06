---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 6928347ab5d78a25d53636f73413f772b9beea4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585312"
---
# <span data-ttu-id="f95f4-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="f95f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f95f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f95f4-103">Ändrar ett Service Bus-köjobb.</span><span class="sxs-lookup"><span data-stu-id="f95f4-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f95f4-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f95f4-105">DESCRIPTION</span></span>
<span data-ttu-id="f95f4-106">Cmdleten **set-AzureRmSchedulerServiceBusQueueJob** ändrar ett Service Bus-köjobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="f95f4-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="f95f4-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="f95f4-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="f95f4-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="f95f4-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="f95f4-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f95f4-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f95f4-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f95f4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f95f4-111">EXAMPLES</span></span>

## <span data-ttu-id="f95f4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f95f4-112">PARAMETERS</span></span>

### <span data-ttu-id="f95f4-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="f95f4-113">-EndTime</span></span>
<span data-ttu-id="f95f4-114">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="f95f4-115">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f95f4-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f95f4-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="f95f4-116">-ErrorActionType</span></span>
<span data-ttu-id="f95f4-117">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="f95f4-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f95f4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95f4-119">Inkommande</span><span class="sxs-lookup"><span data-stu-id="f95f4-119">Http</span></span> 
- <span data-ttu-id="f95f4-120">Https</span><span class="sxs-lookup"><span data-stu-id="f95f4-120">Https</span></span> 
- <span data-ttu-id="f95f4-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="f95f4-121">StorageQueue</span></span> 
- <span data-ttu-id="f95f4-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f95f4-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="f95f4-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f95f4-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="f95f4-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="f95f4-124">-ExecutionCount</span></span>
<span data-ttu-id="f95f4-125">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="f95f4-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="f95f4-126">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="f95f4-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="f95f4-127">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="f95f4-127">-Frequency</span></span>
<span data-ttu-id="f95f4-128">Anger en frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="f95f4-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f95f4-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95f4-130">Minut</span><span class="sxs-lookup"><span data-stu-id="f95f4-130">Minute</span></span> 
- <span data-ttu-id="f95f4-131">Timme</span><span class="sxs-lookup"><span data-stu-id="f95f4-131">Hour</span></span> 
- <span data-ttu-id="f95f4-132">Day</span><span class="sxs-lookup"><span data-stu-id="f95f4-132">Day</span></span> 
- <span data-ttu-id="f95f4-133">Fjorton</span><span class="sxs-lookup"><span data-stu-id="f95f4-133">Week</span></span> 
- <span data-ttu-id="f95f4-134">Månad</span><span class="sxs-lookup"><span data-stu-id="f95f4-134">Month</span></span>

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

### <span data-ttu-id="f95f4-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="f95f4-135">-Interval</span></span>
<span data-ttu-id="f95f4-136">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="f95f4-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f95f4-137">-JobCollectionName</span></span>
<span data-ttu-id="f95f4-138">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="f95f4-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="f95f4-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="f95f4-139">-JobName</span></span>
<span data-ttu-id="f95f4-140">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f95f4-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f95f4-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="f95f4-141">-JobState</span></span>
<span data-ttu-id="f95f4-142">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-142">Specifies the state of the job.</span></span>
<span data-ttu-id="f95f4-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f95f4-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95f4-144">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="f95f4-144">Enabled</span></span> 
- <span data-ttu-id="f95f4-145">Aktiv</span><span class="sxs-lookup"><span data-stu-id="f95f4-145">Disabled</span></span>

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

### <span data-ttu-id="f95f4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95f4-146">-ResourceGroupName</span></span>
<span data-ttu-id="f95f4-147">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="f95f4-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="f95f4-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="f95f4-148">-ServiceBusMessage</span></span>
<span data-ttu-id="f95f4-149">Anger ett Service Bus Queue-meddelande.</span><span class="sxs-lookup"><span data-stu-id="f95f4-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="f95f4-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f95f4-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="f95f4-151">Anger ett Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="f95f4-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="f95f4-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="f95f4-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="f95f4-153">Anger namnet på en Service Bus-kö.</span><span class="sxs-lookup"><span data-stu-id="f95f4-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="f95f4-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="f95f4-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="f95f4-155">Anger ett namn på en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="f95f4-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="f95f4-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="f95f4-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="f95f4-157">Anger ett värde för en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="f95f4-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="f95f4-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="f95f4-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="f95f4-159">Anger typen Service Bus transport.</span><span class="sxs-lookup"><span data-stu-id="f95f4-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="f95f4-160">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f95f4-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95f4-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="f95f4-161">NetMessaging</span></span> 
- <span data-ttu-id="f95f4-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="f95f4-162">AMQP</span></span>

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

### <span data-ttu-id="f95f4-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f95f4-163">-StartTime</span></span>
<span data-ttu-id="f95f4-164">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f95f4-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="f95f4-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f95f4-165">-Confirm</span></span>
<span data-ttu-id="f95f4-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f95f4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95f4-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95f4-167">-WhatIf</span></span>
<span data-ttu-id="f95f4-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f95f4-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95f4-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f95f4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95f4-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95f4-170">-DefaultProfile</span></span>
<span data-ttu-id="f95f4-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f95f4-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f95f4-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95f4-172">CommonParameters</span></span>
<span data-ttu-id="f95f4-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95f4-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95f4-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95f4-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95f4-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f95f4-175">INPUTS</span></span>

## <span data-ttu-id="f95f4-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f95f4-176">OUTPUTS</span></span>

### <span data-ttu-id="f95f4-177">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f95f4-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="f95f4-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f95f4-178">NOTES</span></span>

## <span data-ttu-id="f95f4-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f95f4-179">RELATED LINKS</span></span>

[<span data-ttu-id="f95f4-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f95f4-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f95f4-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f95f4-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f95f4-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f95f4-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="f95f4-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f95f4-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f95f4-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f95f4-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f95f4-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f95f4-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


