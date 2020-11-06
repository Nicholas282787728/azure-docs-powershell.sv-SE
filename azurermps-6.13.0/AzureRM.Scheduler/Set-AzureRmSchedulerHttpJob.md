---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2810a73e54151d8227a115aa71f486d09811def8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575093"
---
# <span data-ttu-id="56f3f-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="56f3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="56f3f-103">Ändrar ett HTTP-jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="56f3f-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56f3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56f3f-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56f3f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56f3f-105">DESCRIPTION</span></span>
<span data-ttu-id="56f3f-106">Cmdleten **set-AzureRmSchedulerHttpJob** ändrar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="56f3f-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="56f3f-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="56f3f-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="56f3f-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="56f3f-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="56f3f-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="56f3f-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="56f3f-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="56f3f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56f3f-111">EXAMPLES</span></span>

## <span data-ttu-id="56f3f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56f3f-112">PARAMETERS</span></span>

### <span data-ttu-id="56f3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f3f-113">-DefaultProfile</span></span>
<span data-ttu-id="56f3f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56f3f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f3f-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="56f3f-115">-EndTime</span></span>
<span data-ttu-id="56f3f-116">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="56f3f-117">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="56f3f-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="56f3f-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="56f3f-118">-ErrorActionType</span></span>
<span data-ttu-id="56f3f-119">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="56f3f-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56f3f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f3f-121">Inkommande</span><span class="sxs-lookup"><span data-stu-id="56f3f-121">Http</span></span> 
- <span data-ttu-id="56f3f-122">Https</span><span class="sxs-lookup"><span data-stu-id="56f3f-122">Https</span></span> 
- <span data-ttu-id="56f3f-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="56f3f-123">StorageQueue</span></span> 
- <span data-ttu-id="56f3f-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="56f3f-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="56f3f-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="56f3f-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="56f3f-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="56f3f-126">-ExecutionCount</span></span>
<span data-ttu-id="56f3f-127">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="56f3f-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="56f3f-128">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="56f3f-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="56f3f-129">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="56f3f-129">-Frequency</span></span>
<span data-ttu-id="56f3f-130">Anger den maximala frekvensen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="56f3f-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56f3f-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f3f-132">Minut</span><span class="sxs-lookup"><span data-stu-id="56f3f-132">Minute</span></span> 
- <span data-ttu-id="56f3f-133">Timme</span><span class="sxs-lookup"><span data-stu-id="56f3f-133">Hour</span></span> 
- <span data-ttu-id="56f3f-134">Day</span><span class="sxs-lookup"><span data-stu-id="56f3f-134">Day</span></span> 
- <span data-ttu-id="56f3f-135">Fjorton</span><span class="sxs-lookup"><span data-stu-id="56f3f-135">Week</span></span> 
- <span data-ttu-id="56f3f-136">Månad</span><span class="sxs-lookup"><span data-stu-id="56f3f-136">Month</span></span>

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

### <span data-ttu-id="56f3f-137">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="56f3f-137">-Headers</span></span>
<span data-ttu-id="56f3f-138">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="56f3f-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="56f3f-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="56f3f-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="56f3f-140">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="56f3f-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="56f3f-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56f3f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f3f-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="56f3f-142">None</span></span> 
- <span data-ttu-id="56f3f-143">Mängden</span><span class="sxs-lookup"><span data-stu-id="56f3f-143">ClientCertificate</span></span> 
- <span data-ttu-id="56f3f-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="56f3f-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="56f3f-145">Basisk</span><span class="sxs-lookup"><span data-stu-id="56f3f-145">Basic</span></span>

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

### <span data-ttu-id="56f3f-146">-Intervall</span><span class="sxs-lookup"><span data-stu-id="56f3f-146">-Interval</span></span>
<span data-ttu-id="56f3f-147">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="56f3f-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="56f3f-148">-JobCollectionName</span></span>
<span data-ttu-id="56f3f-149">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="56f3f-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="56f3f-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="56f3f-150">-JobName</span></span>
<span data-ttu-id="56f3f-151">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="56f3f-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="56f3f-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="56f3f-152">-JobState</span></span>
<span data-ttu-id="56f3f-153">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-153">Specifies the state of the job.</span></span>
<span data-ttu-id="56f3f-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56f3f-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f3f-155">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="56f3f-155">Enabled</span></span> 
- <span data-ttu-id="56f3f-156">Aktiv</span><span class="sxs-lookup"><span data-stu-id="56f3f-156">Disabled</span></span>

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

### <span data-ttu-id="56f3f-157">-Metod</span><span class="sxs-lookup"><span data-stu-id="56f3f-157">-Method</span></span>
<span data-ttu-id="56f3f-158">Anger metod för åtgärds typer för det här jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="56f3f-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56f3f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f3f-160">LÄRA</span><span class="sxs-lookup"><span data-stu-id="56f3f-160">GET</span></span> 
- <span data-ttu-id="56f3f-161">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="56f3f-161">PUT</span></span> 
- <span data-ttu-id="56f3f-162">TEST</span><span class="sxs-lookup"><span data-stu-id="56f3f-162">POST</span></span> 
- <span data-ttu-id="56f3f-163">TA bort</span><span class="sxs-lookup"><span data-stu-id="56f3f-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f3f-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="56f3f-164">-RequestBody</span></span>
<span data-ttu-id="56f3f-165">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="56f3f-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="56f3f-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f3f-166">-ResourceGroupName</span></span>
<span data-ttu-id="56f3f-167">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="56f3f-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="56f3f-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="56f3f-168">-StartTime</span></span>
<span data-ttu-id="56f3f-169">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="56f3f-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="56f3f-170">-URI</span><span class="sxs-lookup"><span data-stu-id="56f3f-170">-Uri</span></span>
<span data-ttu-id="56f3f-171">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="56f3f-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f3f-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56f3f-172">-Confirm</span></span>
<span data-ttu-id="56f3f-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56f3f-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f3f-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f3f-174">-WhatIf</span></span>
<span data-ttu-id="56f3f-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56f3f-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f3f-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56f3f-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f3f-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f3f-177">CommonParameters</span></span>
<span data-ttu-id="56f3f-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f3f-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f3f-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f3f-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f3f-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56f3f-180">INPUTS</span></span>

### <span data-ttu-id="56f3f-181">System. String</span><span class="sxs-lookup"><span data-stu-id="56f3f-181">System.String</span></span>

### <span data-ttu-id="56f3f-182">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="56f3f-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="56f3f-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56f3f-183">OUTPUTS</span></span>

### <span data-ttu-id="56f3f-184">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="56f3f-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="56f3f-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56f3f-185">NOTES</span></span>

## <span data-ttu-id="56f3f-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56f3f-186">RELATED LINKS</span></span>

[<span data-ttu-id="56f3f-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="56f3f-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="56f3f-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="56f3f-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="56f3f-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="56f3f-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="56f3f-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="56f3f-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="56f3f-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="56f3f-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="56f3f-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="56f3f-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


