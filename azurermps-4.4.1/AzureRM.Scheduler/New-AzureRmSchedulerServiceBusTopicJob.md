---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582200"
---
# <span data-ttu-id="75322-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="75322-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="75322-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75322-102">SYNOPSIS</span></span>
<span data-ttu-id="75322-103">Skapar ett ämnes jobb för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="75322-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75322-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75322-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75322-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75322-105">DESCRIPTION</span></span>
<span data-ttu-id="75322-106">Cmdleten **New-AzureRmSchedulerServiceBusTopicJob** skapar ett artikel jobb för Service Bus i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="75322-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="75322-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="75322-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="75322-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="75322-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="75322-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="75322-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="75322-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="75322-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="75322-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75322-111">EXAMPLES</span></span>

## <span data-ttu-id="75322-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75322-112">PARAMETERS</span></span>

### <span data-ttu-id="75322-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="75322-113">-EndTime</span></span>
<span data-ttu-id="75322-114">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="75322-115">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="75322-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="75322-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="75322-116">-ErrorActionType</span></span>
<span data-ttu-id="75322-117">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="75322-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="75322-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75322-119">Inkommande</span><span class="sxs-lookup"><span data-stu-id="75322-119">Http</span></span> 
- <span data-ttu-id="75322-120">Https</span><span class="sxs-lookup"><span data-stu-id="75322-120">Https</span></span> 
- <span data-ttu-id="75322-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="75322-121">StorageQueue</span></span> 
- <span data-ttu-id="75322-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="75322-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="75322-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="75322-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="75322-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="75322-124">-ExecutionCount</span></span>
<span data-ttu-id="75322-125">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="75322-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="75322-126">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="75322-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="75322-127">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="75322-127">-Frequency</span></span>
<span data-ttu-id="75322-128">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="75322-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="75322-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75322-130">Minut</span><span class="sxs-lookup"><span data-stu-id="75322-130">Minute</span></span> 
- <span data-ttu-id="75322-131">Timme</span><span class="sxs-lookup"><span data-stu-id="75322-131">Hour</span></span> 
- <span data-ttu-id="75322-132">Day</span><span class="sxs-lookup"><span data-stu-id="75322-132">Day</span></span> 
- <span data-ttu-id="75322-133">Fjorton</span><span class="sxs-lookup"><span data-stu-id="75322-133">Week</span></span> 
- <span data-ttu-id="75322-134">Månad</span><span class="sxs-lookup"><span data-stu-id="75322-134">Month</span></span>

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

### <span data-ttu-id="75322-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="75322-135">-Interval</span></span>
<span data-ttu-id="75322-136">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="75322-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="75322-137">-JobCollectionName</span></span>
<span data-ttu-id="75322-138">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="75322-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="75322-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="75322-139">-JobName</span></span>
<span data-ttu-id="75322-140">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="75322-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="75322-141">-JobState</span></span>
<span data-ttu-id="75322-142">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-142">Specifies the state of the job.</span></span>
<span data-ttu-id="75322-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="75322-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75322-144">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="75322-144">Enabled</span></span> 
- <span data-ttu-id="75322-145">Aktiv</span><span class="sxs-lookup"><span data-stu-id="75322-145">Disabled</span></span>

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

### <span data-ttu-id="75322-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75322-146">-ResourceGroupName</span></span>
<span data-ttu-id="75322-147">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="75322-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="75322-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="75322-148">-ServiceBusMessage</span></span>
<span data-ttu-id="75322-149">Anger ett avsnitts meddelande för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="75322-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="75322-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="75322-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="75322-151">Anger ett Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="75322-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="75322-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="75322-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="75322-153">Anger ett namn på en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="75322-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="75322-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="75322-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="75322-155">Anger ett värde för en signaturnyckel för en delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="75322-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="75322-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="75322-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="75322-157">Anger sökvägen till en tjänst buss.</span><span class="sxs-lookup"><span data-stu-id="75322-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="75322-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="75322-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="75322-159">Anger typen Service Bus transport.</span><span class="sxs-lookup"><span data-stu-id="75322-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="75322-160">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="75322-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75322-161">Netmessaging</span><span class="sxs-lookup"><span data-stu-id="75322-161">NetMessaging</span></span>
- <span data-ttu-id="75322-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="75322-162">AMQP</span></span>

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

### <span data-ttu-id="75322-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="75322-163">-StartTime</span></span>
<span data-ttu-id="75322-164">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="75322-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="75322-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75322-165">-Confirm</span></span>
<span data-ttu-id="75322-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75322-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75322-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75322-167">-WhatIf</span></span>
<span data-ttu-id="75322-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75322-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75322-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75322-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75322-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75322-170">-DefaultProfile</span></span>
<span data-ttu-id="75322-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75322-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75322-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75322-172">CommonParameters</span></span>
<span data-ttu-id="75322-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75322-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75322-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75322-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75322-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75322-175">INPUTS</span></span>

## <span data-ttu-id="75322-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75322-176">OUTPUTS</span></span>

### <span data-ttu-id="75322-177">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="75322-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="75322-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75322-178">NOTES</span></span>

## <span data-ttu-id="75322-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75322-179">RELATED LINKS</span></span>

[<span data-ttu-id="75322-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="75322-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="75322-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="75322-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="75322-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="75322-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="75322-183">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="75322-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="75322-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="75322-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="75322-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="75322-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="75322-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="75322-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="75322-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="75322-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="75322-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="75322-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)

