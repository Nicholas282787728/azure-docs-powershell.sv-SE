---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583943"
---
# <span data-ttu-id="a83f4-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="a83f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a83f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a83f4-103">Skapar ett HTTP-jobb.</span><span class="sxs-lookup"><span data-stu-id="a83f4-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a83f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a83f4-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a83f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a83f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a83f4-106">Cmdleten **New-AzureRmSchedulerHttpJob** skapar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="a83f4-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="a83f4-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="a83f4-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="a83f4-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="a83f4-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="a83f4-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a83f4-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a83f4-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a83f4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a83f4-111">EXAMPLES</span></span>

## <span data-ttu-id="a83f4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a83f4-112">PARAMETERS</span></span>

### <span data-ttu-id="a83f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83f4-113">-DefaultProfile</span></span>
<span data-ttu-id="a83f4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a83f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83f4-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="a83f4-115">-EndTime</span></span>
<span data-ttu-id="a83f4-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a83f4-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a83f4-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a83f4-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a83f4-118">-ErrorActionType</span></span>
<span data-ttu-id="a83f4-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a83f4-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a83f4-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a83f4-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="a83f4-121">Http</span></span> 
- <span data-ttu-id="a83f4-122">Https</span><span class="sxs-lookup"><span data-stu-id="a83f4-122">Https</span></span> 
- <span data-ttu-id="a83f4-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a83f4-123">StorageQueue</span></span> 
- <span data-ttu-id="a83f4-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a83f4-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="a83f4-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a83f4-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a83f4-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a83f4-126">-ExecutionCount</span></span>
<span data-ttu-id="a83f4-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="a83f4-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a83f4-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="a83f4-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a83f4-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="a83f4-129">-Frequency</span></span>
<span data-ttu-id="a83f4-130">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="a83f4-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a83f4-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a83f4-132">Minut</span><span class="sxs-lookup"><span data-stu-id="a83f4-132">Minute</span></span> 
- <span data-ttu-id="a83f4-133">Timme</span><span class="sxs-lookup"><span data-stu-id="a83f4-133">Hour</span></span> 
- <span data-ttu-id="a83f4-134">Day</span><span class="sxs-lookup"><span data-stu-id="a83f4-134">Day</span></span> 
- <span data-ttu-id="a83f4-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="a83f4-135">Week</span></span> 
- <span data-ttu-id="a83f4-136">Månad</span><span class="sxs-lookup"><span data-stu-id="a83f4-136">Month</span></span>

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

### <span data-ttu-id="a83f4-137">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="a83f4-137">-Headers</span></span>
<span data-ttu-id="a83f4-138">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="a83f4-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83f4-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a83f4-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="a83f4-140">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="a83f4-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="a83f4-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a83f4-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a83f4-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="a83f4-142">None</span></span> 
- <span data-ttu-id="a83f4-143">Mängden</span><span class="sxs-lookup"><span data-stu-id="a83f4-143">ClientCertificate</span></span> 
- <span data-ttu-id="a83f4-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="a83f4-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="a83f4-145">Basisk</span><span class="sxs-lookup"><span data-stu-id="a83f4-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83f4-146">-Intervall</span><span class="sxs-lookup"><span data-stu-id="a83f4-146">-Interval</span></span>
<span data-ttu-id="a83f4-147">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a83f4-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a83f4-148">-JobCollectionName</span></span>
<span data-ttu-id="a83f4-149">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="a83f4-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a83f4-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="a83f4-150">-JobName</span></span>
<span data-ttu-id="a83f4-151">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="a83f4-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="a83f4-152">-JobState</span></span>
<span data-ttu-id="a83f4-153">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-153">Specifies the state of the job.</span></span>
<span data-ttu-id="a83f4-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a83f4-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a83f4-155">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="a83f4-155">Enabled</span></span> 
- <span data-ttu-id="a83f4-156">Aktiv</span><span class="sxs-lookup"><span data-stu-id="a83f4-156">Disabled</span></span>

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

### <span data-ttu-id="a83f4-157">-Metod</span><span class="sxs-lookup"><span data-stu-id="a83f4-157">-Method</span></span>
<span data-ttu-id="a83f4-158">Anger metod för jobbets åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="a83f4-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="a83f4-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a83f4-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a83f4-160">LÄRA</span><span class="sxs-lookup"><span data-stu-id="a83f4-160">GET</span></span> 
- <span data-ttu-id="a83f4-161">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="a83f4-161">PUT</span></span> 
- <span data-ttu-id="a83f4-162">TEST</span><span class="sxs-lookup"><span data-stu-id="a83f4-162">POST</span></span> 
- <span data-ttu-id="a83f4-163">TA bort</span><span class="sxs-lookup"><span data-stu-id="a83f4-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83f4-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="a83f4-164">-RequestBody</span></span>
<span data-ttu-id="a83f4-165">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a83f4-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="a83f4-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a83f4-166">-ResourceGroupName</span></span>
<span data-ttu-id="a83f4-167">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="a83f4-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a83f4-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a83f4-168">-StartTime</span></span>
<span data-ttu-id="a83f4-169">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a83f4-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a83f4-170">-URI</span><span class="sxs-lookup"><span data-stu-id="a83f4-170">-Uri</span></span>
<span data-ttu-id="a83f4-171">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a83f4-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83f4-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a83f4-172">-Confirm</span></span>
<span data-ttu-id="a83f4-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a83f4-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a83f4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a83f4-174">-WhatIf</span></span>
<span data-ttu-id="a83f4-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a83f4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a83f4-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a83f4-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a83f4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83f4-177">CommonParameters</span></span>
<span data-ttu-id="a83f4-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83f4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83f4-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83f4-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83f4-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a83f4-180">INPUTS</span></span>

### <span data-ttu-id="a83f4-181">System. String</span><span class="sxs-lookup"><span data-stu-id="a83f4-181">System.String</span></span>

### <span data-ttu-id="a83f4-182">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a83f4-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a83f4-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a83f4-183">OUTPUTS</span></span>

### <span data-ttu-id="a83f4-184">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a83f4-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a83f4-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a83f4-185">NOTES</span></span>

## <span data-ttu-id="a83f4-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a83f4-186">RELATED LINKS</span></span>

[<span data-ttu-id="a83f4-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a83f4-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a83f4-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a83f4-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a83f4-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a83f4-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a83f4-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a83f4-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a83f4-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a83f4-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a83f4-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a83f4-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


