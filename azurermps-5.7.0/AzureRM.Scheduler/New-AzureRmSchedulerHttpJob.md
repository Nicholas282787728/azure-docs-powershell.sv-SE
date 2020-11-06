---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574180"
---
# <span data-ttu-id="a09af-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a09af-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="a09af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a09af-102">SYNOPSIS</span></span>
<span data-ttu-id="a09af-103">Skapar ett HTTP-jobb.</span><span class="sxs-lookup"><span data-stu-id="a09af-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a09af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a09af-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a09af-105">DESCRIPTION</span></span>
<span data-ttu-id="a09af-106">Cmdleten **New-AzureRmSchedulerHttpJob** skapar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="a09af-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="a09af-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="a09af-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="a09af-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="a09af-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="a09af-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a09af-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a09af-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="a09af-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a09af-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a09af-111">EXAMPLES</span></span>

## <span data-ttu-id="a09af-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a09af-112">PARAMETERS</span></span>

### <span data-ttu-id="a09af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09af-113">-DefaultProfile</span></span>
<span data-ttu-id="a09af-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a09af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a09af-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="a09af-115">-EndTime</span></span>
<span data-ttu-id="a09af-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a09af-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a09af-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a09af-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a09af-118">-ErrorActionType</span></span>
<span data-ttu-id="a09af-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a09af-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09af-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09af-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="a09af-121">Http</span></span> 
- <span data-ttu-id="a09af-122">Https</span><span class="sxs-lookup"><span data-stu-id="a09af-122">Https</span></span> 
- <span data-ttu-id="a09af-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a09af-123">StorageQueue</span></span> 
- <span data-ttu-id="a09af-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a09af-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="a09af-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a09af-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a09af-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a09af-126">-ExecutionCount</span></span>
<span data-ttu-id="a09af-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="a09af-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a09af-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="a09af-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a09af-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="a09af-129">-Frequency</span></span>
<span data-ttu-id="a09af-130">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="a09af-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09af-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09af-132">Minut</span><span class="sxs-lookup"><span data-stu-id="a09af-132">Minute</span></span> 
- <span data-ttu-id="a09af-133">Timme</span><span class="sxs-lookup"><span data-stu-id="a09af-133">Hour</span></span> 
- <span data-ttu-id="a09af-134">Day</span><span class="sxs-lookup"><span data-stu-id="a09af-134">Day</span></span> 
- <span data-ttu-id="a09af-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="a09af-135">Week</span></span> 
- <span data-ttu-id="a09af-136">Månad</span><span class="sxs-lookup"><span data-stu-id="a09af-136">Month</span></span>

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

### <span data-ttu-id="a09af-137">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="a09af-137">-Headers</span></span>
<span data-ttu-id="a09af-138">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="a09af-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="a09af-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a09af-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="a09af-140">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="a09af-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="a09af-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09af-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09af-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="a09af-142">None</span></span> 
- <span data-ttu-id="a09af-143">Mängden</span><span class="sxs-lookup"><span data-stu-id="a09af-143">ClientCertificate</span></span> 
- <span data-ttu-id="a09af-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="a09af-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="a09af-145">Basisk</span><span class="sxs-lookup"><span data-stu-id="a09af-145">Basic</span></span>

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

### <span data-ttu-id="a09af-146">-Intervall</span><span class="sxs-lookup"><span data-stu-id="a09af-146">-Interval</span></span>
<span data-ttu-id="a09af-147">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a09af-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a09af-148">-JobCollectionName</span></span>
<span data-ttu-id="a09af-149">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="a09af-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a09af-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="a09af-150">-JobName</span></span>
<span data-ttu-id="a09af-151">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="a09af-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="a09af-152">-JobState</span></span>
<span data-ttu-id="a09af-153">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-153">Specifies the state of the job.</span></span>
<span data-ttu-id="a09af-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09af-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09af-155">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="a09af-155">Enabled</span></span> 
- <span data-ttu-id="a09af-156">Aktiv</span><span class="sxs-lookup"><span data-stu-id="a09af-156">Disabled</span></span>

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

### <span data-ttu-id="a09af-157">-Metod</span><span class="sxs-lookup"><span data-stu-id="a09af-157">-Method</span></span>
<span data-ttu-id="a09af-158">Anger metod för jobbets åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="a09af-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="a09af-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a09af-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09af-160">LÄRA</span><span class="sxs-lookup"><span data-stu-id="a09af-160">GET</span></span> 
- <span data-ttu-id="a09af-161">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="a09af-161">PUT</span></span> 
- <span data-ttu-id="a09af-162">TEST</span><span class="sxs-lookup"><span data-stu-id="a09af-162">POST</span></span> 
- <span data-ttu-id="a09af-163">TA bort</span><span class="sxs-lookup"><span data-stu-id="a09af-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09af-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="a09af-164">-RequestBody</span></span>
<span data-ttu-id="a09af-165">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a09af-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="a09af-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09af-166">-ResourceGroupName</span></span>
<span data-ttu-id="a09af-167">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="a09af-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a09af-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a09af-168">-StartTime</span></span>
<span data-ttu-id="a09af-169">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a09af-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a09af-170">-URI</span><span class="sxs-lookup"><span data-stu-id="a09af-170">-Uri</span></span>
<span data-ttu-id="a09af-171">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a09af-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09af-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a09af-172">-Confirm</span></span>
<span data-ttu-id="a09af-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a09af-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09af-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09af-174">-WhatIf</span></span>
<span data-ttu-id="a09af-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a09af-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09af-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a09af-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09af-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09af-177">CommonParameters</span></span>
<span data-ttu-id="a09af-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09af-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09af-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09af-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09af-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a09af-180">INPUTS</span></span>

### <span data-ttu-id="a09af-181">Ingen</span><span class="sxs-lookup"><span data-stu-id="a09af-181">None</span></span>
<span data-ttu-id="a09af-182">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a09af-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a09af-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a09af-183">OUTPUTS</span></span>

### <span data-ttu-id="a09af-184">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a09af-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a09af-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a09af-185">NOTES</span></span>

## <span data-ttu-id="a09af-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a09af-186">RELATED LINKS</span></span>

[<span data-ttu-id="a09af-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a09af-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a09af-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a09af-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a09af-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a09af-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a09af-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a09af-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a09af-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a09af-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a09af-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a09af-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a09af-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a09af-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a09af-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a09af-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a09af-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a09af-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


