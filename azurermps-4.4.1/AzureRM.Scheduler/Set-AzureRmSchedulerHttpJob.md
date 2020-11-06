---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2debabbcd4ae9b5418436e7846e8490926f37b1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577480"
---
# <span data-ttu-id="3afc7-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="3afc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3afc7-102">SYNOPSIS</span></span>
<span data-ttu-id="3afc7-103">Ändrar ett HTTP-jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="3afc7-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3afc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3afc7-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3afc7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3afc7-105">DESCRIPTION</span></span>
<span data-ttu-id="3afc7-106">Cmdleten **set-AzureRmSchedulerHttpJob** ändrar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="3afc7-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="3afc7-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="3afc7-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="3afc7-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="3afc7-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="3afc7-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="3afc7-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3afc7-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3afc7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3afc7-111">EXAMPLES</span></span>

## <span data-ttu-id="3afc7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3afc7-112">PARAMETERS</span></span>

### <span data-ttu-id="3afc7-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="3afc7-113">-EndTime</span></span>
<span data-ttu-id="3afc7-114">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="3afc7-115">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3afc7-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="3afc7-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="3afc7-116">-ErrorActionType</span></span>
<span data-ttu-id="3afc7-117">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="3afc7-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3afc7-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3afc7-119">Inkommande</span><span class="sxs-lookup"><span data-stu-id="3afc7-119">Http</span></span> 
- <span data-ttu-id="3afc7-120">Https</span><span class="sxs-lookup"><span data-stu-id="3afc7-120">Https</span></span> 
- <span data-ttu-id="3afc7-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="3afc7-121">StorageQueue</span></span> 
- <span data-ttu-id="3afc7-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3afc7-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="3afc7-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="3afc7-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="3afc7-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="3afc7-124">-ExecutionCount</span></span>
<span data-ttu-id="3afc7-125">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="3afc7-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="3afc7-126">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="3afc7-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="3afc7-127">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="3afc7-127">-Frequency</span></span>
<span data-ttu-id="3afc7-128">Anger den maximala frekvensen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-128">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="3afc7-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3afc7-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3afc7-130">Minut</span><span class="sxs-lookup"><span data-stu-id="3afc7-130">Minute</span></span> 
- <span data-ttu-id="3afc7-131">Timme</span><span class="sxs-lookup"><span data-stu-id="3afc7-131">Hour</span></span> 
- <span data-ttu-id="3afc7-132">Day</span><span class="sxs-lookup"><span data-stu-id="3afc7-132">Day</span></span> 
- <span data-ttu-id="3afc7-133">Fjorton</span><span class="sxs-lookup"><span data-stu-id="3afc7-133">Week</span></span> 
- <span data-ttu-id="3afc7-134">Månad</span><span class="sxs-lookup"><span data-stu-id="3afc7-134">Month</span></span>

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

### <span data-ttu-id="3afc7-135">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="3afc7-135">-Headers</span></span>
<span data-ttu-id="3afc7-136">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="3afc7-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="3afc7-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3afc7-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="3afc7-138">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="3afc7-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="3afc7-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3afc7-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3afc7-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="3afc7-140">None</span></span> 
- <span data-ttu-id="3afc7-141">Mängden</span><span class="sxs-lookup"><span data-stu-id="3afc7-141">ClientCertificate</span></span> 
- <span data-ttu-id="3afc7-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="3afc7-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="3afc7-143">Basisk</span><span class="sxs-lookup"><span data-stu-id="3afc7-143">Basic</span></span>

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

### <span data-ttu-id="3afc7-144">-Intervall</span><span class="sxs-lookup"><span data-stu-id="3afc7-144">-Interval</span></span>
<span data-ttu-id="3afc7-145">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="3afc7-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3afc7-146">-JobCollectionName</span></span>
<span data-ttu-id="3afc7-147">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="3afc7-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="3afc7-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="3afc7-148">-JobName</span></span>
<span data-ttu-id="3afc7-149">Anger namnet på det jobb som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="3afc7-149">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3afc7-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="3afc7-150">-JobState</span></span>
<span data-ttu-id="3afc7-151">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-151">Specifies the state of the job.</span></span>
<span data-ttu-id="3afc7-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3afc7-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3afc7-153">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="3afc7-153">Enabled</span></span> 
- <span data-ttu-id="3afc7-154">Aktiv</span><span class="sxs-lookup"><span data-stu-id="3afc7-154">Disabled</span></span>

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

### <span data-ttu-id="3afc7-155">-Metod</span><span class="sxs-lookup"><span data-stu-id="3afc7-155">-Method</span></span>
<span data-ttu-id="3afc7-156">Anger metod för åtgärds typer för det här jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-156">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="3afc7-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3afc7-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3afc7-158">LÄRA</span><span class="sxs-lookup"><span data-stu-id="3afc7-158">GET</span></span> 
- <span data-ttu-id="3afc7-159">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="3afc7-159">PUT</span></span> 
- <span data-ttu-id="3afc7-160">TEST</span><span class="sxs-lookup"><span data-stu-id="3afc7-160">POST</span></span> 
- <span data-ttu-id="3afc7-161">TA bort</span><span class="sxs-lookup"><span data-stu-id="3afc7-161">DELETE</span></span>

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

### <span data-ttu-id="3afc7-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="3afc7-162">-RequestBody</span></span>
<span data-ttu-id="3afc7-163">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3afc7-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="3afc7-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afc7-164">-ResourceGroupName</span></span>
<span data-ttu-id="3afc7-165">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="3afc7-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="3afc7-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3afc7-166">-StartTime</span></span>
<span data-ttu-id="3afc7-167">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="3afc7-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="3afc7-168">-URI</span><span class="sxs-lookup"><span data-stu-id="3afc7-168">-Uri</span></span>
<span data-ttu-id="3afc7-169">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3afc7-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="3afc7-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3afc7-170">-Confirm</span></span>
<span data-ttu-id="3afc7-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3afc7-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3afc7-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3afc7-172">-WhatIf</span></span>
<span data-ttu-id="3afc7-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3afc7-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3afc7-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3afc7-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3afc7-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afc7-175">-DefaultProfile</span></span>
<span data-ttu-id="3afc7-176">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3afc7-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3afc7-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afc7-177">CommonParameters</span></span>
<span data-ttu-id="3afc7-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afc7-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afc7-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3afc7-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afc7-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3afc7-180">INPUTS</span></span>

## <span data-ttu-id="3afc7-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3afc7-181">OUTPUTS</span></span>

### <span data-ttu-id="3afc7-182">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3afc7-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="3afc7-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3afc7-183">NOTES</span></span>

## <span data-ttu-id="3afc7-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3afc7-184">RELATED LINKS</span></span>

[<span data-ttu-id="3afc7-185">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-185">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="3afc7-186">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3afc7-186">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3afc7-187">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-187">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3afc7-188">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-188">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3afc7-189">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-189">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="3afc7-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3afc7-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3afc7-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3afc7-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3afc7-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3afc7-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


