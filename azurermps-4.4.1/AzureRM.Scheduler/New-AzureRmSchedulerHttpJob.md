---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756855"
---
# <span data-ttu-id="0fb8d-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="0fb8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fb8d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb8d-103">Skapar ett HTTP-jobb.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fb8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fb8d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fb8d-105">DESCRIPTION</span></span>
<span data-ttu-id="0fb8d-106">Cmdleten **New-AzureRmSchedulerHttpJob** skapar ett http-jobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="0fb8d-107">Denna cmdlet stöder dynamiska parametrar baserat på parametrarna *ErrorActionType* och *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="0fb8d-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="0fb8d-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="0fb8d-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0fb8d-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0fb8d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fb8d-111">EXAMPLES</span></span>

## <span data-ttu-id="0fb8d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fb8d-112">PARAMETERS</span></span>

### <span data-ttu-id="0fb8d-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="0fb8d-113">-EndTime</span></span>
<span data-ttu-id="0fb8d-114">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="0fb8d-115">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0fb8d-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="0fb8d-116">-ErrorActionType</span></span>
<span data-ttu-id="0fb8d-117">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="0fb8d-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0fb8d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fb8d-119">Inkommande</span><span class="sxs-lookup"><span data-stu-id="0fb8d-119">Http</span></span> 
- <span data-ttu-id="0fb8d-120">Https</span><span class="sxs-lookup"><span data-stu-id="0fb8d-120">Https</span></span> 
- <span data-ttu-id="0fb8d-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="0fb8d-121">StorageQueue</span></span> 
- <span data-ttu-id="0fb8d-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0fb8d-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="0fb8d-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0fb8d-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="0fb8d-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="0fb8d-124">-ExecutionCount</span></span>
<span data-ttu-id="0fb8d-125">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="0fb8d-126">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="0fb8d-127">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="0fb8d-127">-Frequency</span></span>
<span data-ttu-id="0fb8d-128">Anger en maximal frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="0fb8d-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0fb8d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fb8d-130">Minut</span><span class="sxs-lookup"><span data-stu-id="0fb8d-130">Minute</span></span> 
- <span data-ttu-id="0fb8d-131">Timme</span><span class="sxs-lookup"><span data-stu-id="0fb8d-131">Hour</span></span> 
- <span data-ttu-id="0fb8d-132">Day</span><span class="sxs-lookup"><span data-stu-id="0fb8d-132">Day</span></span> 
- <span data-ttu-id="0fb8d-133">Fjorton</span><span class="sxs-lookup"><span data-stu-id="0fb8d-133">Week</span></span> 
- <span data-ttu-id="0fb8d-134">Månad</span><span class="sxs-lookup"><span data-stu-id="0fb8d-134">Month</span></span>

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

### <span data-ttu-id="0fb8d-135">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="0fb8d-135">-Headers</span></span>
<span data-ttu-id="0fb8d-136">Anger en hash-tabell som innehåller rubriker.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="0fb8d-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0fb8d-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="0fb8d-138">Anger typen HTTP-autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="0fb8d-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0fb8d-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fb8d-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="0fb8d-140">None</span></span> 
- <span data-ttu-id="0fb8d-141">Mängden</span><span class="sxs-lookup"><span data-stu-id="0fb8d-141">ClientCertificate</span></span> 
- <span data-ttu-id="0fb8d-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="0fb8d-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="0fb8d-143">Basisk</span><span class="sxs-lookup"><span data-stu-id="0fb8d-143">Basic</span></span>

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

### <span data-ttu-id="0fb8d-144">-Intervall</span><span class="sxs-lookup"><span data-stu-id="0fb8d-144">-Interval</span></span>
<span data-ttu-id="0fb8d-145">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="0fb8d-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0fb8d-146">-JobCollectionName</span></span>
<span data-ttu-id="0fb8d-147">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="0fb8d-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="0fb8d-148">-JobName</span></span>
<span data-ttu-id="0fb8d-149">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="0fb8d-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="0fb8d-150">-JobState</span></span>
<span data-ttu-id="0fb8d-151">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-151">Specifies the state of the job.</span></span>
<span data-ttu-id="0fb8d-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0fb8d-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fb8d-153">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="0fb8d-153">Enabled</span></span> 
- <span data-ttu-id="0fb8d-154">Aktiv</span><span class="sxs-lookup"><span data-stu-id="0fb8d-154">Disabled</span></span>

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

### <span data-ttu-id="0fb8d-155">-Metod</span><span class="sxs-lookup"><span data-stu-id="0fb8d-155">-Method</span></span>
<span data-ttu-id="0fb8d-156">Anger metod för jobbets åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="0fb8d-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0fb8d-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fb8d-158">LÄRA</span><span class="sxs-lookup"><span data-stu-id="0fb8d-158">GET</span></span> 
- <span data-ttu-id="0fb8d-159">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="0fb8d-159">PUT</span></span> 
- <span data-ttu-id="0fb8d-160">TEST</span><span class="sxs-lookup"><span data-stu-id="0fb8d-160">POST</span></span> 
- <span data-ttu-id="0fb8d-161">TA bort</span><span class="sxs-lookup"><span data-stu-id="0fb8d-161">DELETE</span></span>

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

### <span data-ttu-id="0fb8d-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="0fb8d-162">-RequestBody</span></span>
<span data-ttu-id="0fb8d-163">Anger värdet på bröd texten för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="0fb8d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb8d-164">-ResourceGroupName</span></span>
<span data-ttu-id="0fb8d-165">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="0fb8d-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0fb8d-166">-StartTime</span></span>
<span data-ttu-id="0fb8d-167">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="0fb8d-168">-URI</span><span class="sxs-lookup"><span data-stu-id="0fb8d-168">-Uri</span></span>
<span data-ttu-id="0fb8d-169">Anger en URI för jobb åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="0fb8d-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fb8d-170">-Confirm</span></span>
<span data-ttu-id="0fb8d-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb8d-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb8d-172">-WhatIf</span></span>
<span data-ttu-id="0fb8d-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fb8d-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb8d-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb8d-175">-DefaultProfile</span></span>
<span data-ttu-id="0fb8d-176">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fb8d-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb8d-177">CommonParameters</span></span>
<span data-ttu-id="0fb8d-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb8d-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb8d-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb8d-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb8d-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fb8d-180">INPUTS</span></span>

## <span data-ttu-id="0fb8d-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fb8d-181">OUTPUTS</span></span>

### <span data-ttu-id="0fb8d-182">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0fb8d-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="0fb8d-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fb8d-183">NOTES</span></span>

## <span data-ttu-id="0fb8d-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fb8d-184">RELATED LINKS</span></span>

[<span data-ttu-id="0fb8d-185">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0fb8d-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0fb8d-186">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0fb8d-187">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0fb8d-188">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="0fb8d-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0fb8d-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0fb8d-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0fb8d-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0fb8d-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0fb8d-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0fb8d-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


