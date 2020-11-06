---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 9f43780cc7684c897b7b6d42e381e47f6ff8e106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581979"
---
# <span data-ttu-id="ad24b-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="ad24b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad24b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad24b-103">Ändrar ett HTTP-jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="ad24b-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad24b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad24b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad24b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad24b-105">DESCRIPTION</span></span>
<span data-ttu-id="ad24b-106">Cmdleten **set-AzureRmSchedulerHttpJob** ändrar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="ad24b-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="ad24b-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="ad24b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="ad24b-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="ad24b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ad24b-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ad24b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad24b-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad24b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad24b-111">EXAMPLES</span></span>

## <span data-ttu-id="ad24b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad24b-112">PARAMETERS</span></span>

### <span data-ttu-id="ad24b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad24b-113">-DefaultProfile</span></span>
<span data-ttu-id="ad24b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad24b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad24b-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="ad24b-115">-EndTime</span></span>
<span data-ttu-id="ad24b-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ad24b-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad24b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ad24b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ad24b-118">-ErrorActionType</span></span>
<span data-ttu-id="ad24b-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ad24b-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ad24b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad24b-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="ad24b-121">Http</span></span> 
- <span data-ttu-id="ad24b-122">Https</span><span class="sxs-lookup"><span data-stu-id="ad24b-122">Https</span></span> 
- <span data-ttu-id="ad24b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ad24b-123">StorageQueue</span></span> 
- <span data-ttu-id="ad24b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ad24b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="ad24b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ad24b-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="ad24b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ad24b-126">-ExecutionCount</span></span>
<span data-ttu-id="ad24b-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="ad24b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ad24b-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="ad24b-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ad24b-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="ad24b-129">-Frequency</span></span>
<span data-ttu-id="ad24b-130">Anger den maximala frekvensen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="ad24b-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ad24b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad24b-132">Minut</span><span class="sxs-lookup"><span data-stu-id="ad24b-132">Minute</span></span> 
- <span data-ttu-id="ad24b-133">Timme</span><span class="sxs-lookup"><span data-stu-id="ad24b-133">Hour</span></span> 
- <span data-ttu-id="ad24b-134">Day</span><span class="sxs-lookup"><span data-stu-id="ad24b-134">Day</span></span> 
- <span data-ttu-id="ad24b-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="ad24b-135">Week</span></span> 
- <span data-ttu-id="ad24b-136">Månad</span><span class="sxs-lookup"><span data-stu-id="ad24b-136">Month</span></span>

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

### <span data-ttu-id="ad24b-137">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="ad24b-137">-Headers</span></span>
<span data-ttu-id="ad24b-138">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="ad24b-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad24b-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="ad24b-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="ad24b-140">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="ad24b-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="ad24b-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ad24b-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad24b-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="ad24b-142">None</span></span> 
- <span data-ttu-id="ad24b-143">Mängden</span><span class="sxs-lookup"><span data-stu-id="ad24b-143">ClientCertificate</span></span> 
- <span data-ttu-id="ad24b-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="ad24b-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="ad24b-145">Basisk</span><span class="sxs-lookup"><span data-stu-id="ad24b-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24b-146">-Intervall</span><span class="sxs-lookup"><span data-stu-id="ad24b-146">-Interval</span></span>
<span data-ttu-id="ad24b-147">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ad24b-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ad24b-148">-JobCollectionName</span></span>
<span data-ttu-id="ad24b-149">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="ad24b-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="ad24b-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="ad24b-150">-JobName</span></span>
<span data-ttu-id="ad24b-151">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ad24b-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ad24b-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="ad24b-152">-JobState</span></span>
<span data-ttu-id="ad24b-153">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-153">Specifies the state of the job.</span></span>
<span data-ttu-id="ad24b-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ad24b-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad24b-155">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="ad24b-155">Enabled</span></span> 
- <span data-ttu-id="ad24b-156">Aktiv</span><span class="sxs-lookup"><span data-stu-id="ad24b-156">Disabled</span></span>

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

### <span data-ttu-id="ad24b-157">-Metod</span><span class="sxs-lookup"><span data-stu-id="ad24b-157">-Method</span></span>
<span data-ttu-id="ad24b-158">Anger metod för åtgärds typer för det här jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="ad24b-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ad24b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad24b-160">LÄRA</span><span class="sxs-lookup"><span data-stu-id="ad24b-160">GET</span></span> 
- <span data-ttu-id="ad24b-161">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="ad24b-161">PUT</span></span> 
- <span data-ttu-id="ad24b-162">TEST</span><span class="sxs-lookup"><span data-stu-id="ad24b-162">POST</span></span> 
- <span data-ttu-id="ad24b-163">TA bort</span><span class="sxs-lookup"><span data-stu-id="ad24b-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24b-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="ad24b-164">-RequestBody</span></span>
<span data-ttu-id="ad24b-165">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ad24b-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="ad24b-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad24b-166">-ResourceGroupName</span></span>
<span data-ttu-id="ad24b-167">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="ad24b-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ad24b-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ad24b-168">-StartTime</span></span>
<span data-ttu-id="ad24b-169">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="ad24b-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ad24b-170">-URI</span><span class="sxs-lookup"><span data-stu-id="ad24b-170">-Uri</span></span>
<span data-ttu-id="ad24b-171">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ad24b-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24b-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad24b-172">-Confirm</span></span>
<span data-ttu-id="ad24b-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad24b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad24b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad24b-174">-WhatIf</span></span>
<span data-ttu-id="ad24b-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad24b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad24b-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad24b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad24b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad24b-177">CommonParameters</span></span>
<span data-ttu-id="ad24b-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad24b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad24b-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad24b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad24b-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad24b-180">INPUTS</span></span>

### <span data-ttu-id="ad24b-181">Ingen</span><span class="sxs-lookup"><span data-stu-id="ad24b-181">None</span></span>
<span data-ttu-id="ad24b-182">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ad24b-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad24b-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad24b-183">OUTPUTS</span></span>

### <span data-ttu-id="ad24b-184">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ad24b-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ad24b-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad24b-185">NOTES</span></span>

## <span data-ttu-id="ad24b-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad24b-186">RELATED LINKS</span></span>

[<span data-ttu-id="ad24b-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ad24b-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ad24b-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ad24b-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ad24b-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ad24b-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ad24b-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ad24b-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ad24b-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ad24b-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ad24b-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ad24b-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


