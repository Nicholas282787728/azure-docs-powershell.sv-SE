---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ba8d917c33f2ab7ac6c82db303df08c01c648bf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582196"
---
# <span data-ttu-id="207a3-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="207a3-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="207a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="207a3-102">SYNOPSIS</span></span>
<span data-ttu-id="207a3-103">Skapar ett utskrifts jobb.</span><span class="sxs-lookup"><span data-stu-id="207a3-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="207a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="207a3-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="207a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="207a3-105">DESCRIPTION</span></span>
<span data-ttu-id="207a3-106">Cmdleten **New-AzureRmSchedulerStorageQueueJob** skapar ett synkroniseringsjobb i Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="207a3-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="207a3-107">Denna cmdlet stöder dynamiska parametrar baserat på parametern *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="207a3-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="207a3-108">Dynamiska parametrar blir tillgängliga baserat på andra parameter värden.</span><span class="sxs-lookup"><span data-stu-id="207a3-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="207a3-109">Om du vill söka efter namn på dynamiska parametrar efter att du har angett de andra parametrarna skriver du ett bindestreck (-) och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="207a3-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="207a3-110">Om du utelämnar en obligatorisk parameter uppmanas du att ange värdet.</span><span class="sxs-lookup"><span data-stu-id="207a3-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="207a3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="207a3-111">EXAMPLES</span></span>

## <span data-ttu-id="207a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="207a3-112">PARAMETERS</span></span>

### <span data-ttu-id="207a3-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="207a3-113">-EndTime</span></span>
<span data-ttu-id="207a3-114">Anger en slut tid, som ett **datetime** -objekt, för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="207a3-115">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="207a3-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="207a3-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="207a3-116">-ErrorActionType</span></span>
<span data-ttu-id="207a3-117">Anger ett fel åtgärds värde för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="207a3-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="207a3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="207a3-119">Inkommande</span><span class="sxs-lookup"><span data-stu-id="207a3-119">Http</span></span> 
- <span data-ttu-id="207a3-120">Https</span><span class="sxs-lookup"><span data-stu-id="207a3-120">Https</span></span> 
- <span data-ttu-id="207a3-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="207a3-121">StorageQueue</span></span> 
- <span data-ttu-id="207a3-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="207a3-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="207a3-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="207a3-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="207a3-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="207a3-124">-ExecutionCount</span></span>
<span data-ttu-id="207a3-125">Anger hur många gånger jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="207a3-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="207a3-126">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="207a3-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="207a3-127">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="207a3-127">-Frequency</span></span>
<span data-ttu-id="207a3-128">Anger en frekvens för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="207a3-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="207a3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="207a3-130">Minut</span><span class="sxs-lookup"><span data-stu-id="207a3-130">Minute</span></span> 
- <span data-ttu-id="207a3-131">Timme</span><span class="sxs-lookup"><span data-stu-id="207a3-131">Hour</span></span> 
- <span data-ttu-id="207a3-132">Day</span><span class="sxs-lookup"><span data-stu-id="207a3-132">Day</span></span> 
- <span data-ttu-id="207a3-133">Fjorton</span><span class="sxs-lookup"><span data-stu-id="207a3-133">Week</span></span> 
- <span data-ttu-id="207a3-134">Månad</span><span class="sxs-lookup"><span data-stu-id="207a3-134">Month</span></span>

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

### <span data-ttu-id="207a3-135">-Intervall</span><span class="sxs-lookup"><span data-stu-id="207a3-135">-Interval</span></span>
<span data-ttu-id="207a3-136">Anger ett intervall för upprepning för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="207a3-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="207a3-137">-JobCollectionName</span></span>
<span data-ttu-id="207a3-138">Anger namnet på den jobb samling som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="207a3-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="207a3-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="207a3-139">-JobName</span></span>
<span data-ttu-id="207a3-140">Anger ett namn för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="207a3-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="207a3-141">-JobState</span></span>
<span data-ttu-id="207a3-142">Anger statusen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-142">Specifies the state of the job.</span></span>
<span data-ttu-id="207a3-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="207a3-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="207a3-144">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="207a3-144">Enabled</span></span> 
- <span data-ttu-id="207a3-145">Aktiv</span><span class="sxs-lookup"><span data-stu-id="207a3-145">Disabled</span></span>

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

### <span data-ttu-id="207a3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="207a3-146">-ResourceGroupName</span></span>
<span data-ttu-id="207a3-147">Anger resurs gruppen som jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="207a3-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="207a3-148">-StartTime</span><span class="sxs-lookup"><span data-stu-id="207a3-148">-StartTime</span></span>
<span data-ttu-id="207a3-149">Anger start tiden som ett **datetime** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="207a3-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="207a3-150">-StorageQueueAccount</span></span>
<span data-ttu-id="207a3-151">Anger ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="207a3-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="207a3-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="207a3-152">-StorageQueueMessage</span></span>
<span data-ttu-id="207a3-153">Anger ett Kömeddelanden för lagrings jobbet.</span><span class="sxs-lookup"><span data-stu-id="207a3-153">Specifies a queue message for the storage job.</span></span>

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

### <span data-ttu-id="207a3-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="207a3-154">-StorageQueueName</span></span>
<span data-ttu-id="207a3-155">Anger ett namn på en kölängd.</span><span class="sxs-lookup"><span data-stu-id="207a3-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="207a3-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="207a3-156">-StorageSASToken</span></span>
<span data-ttu-id="207a3-157">Anger ett delat åtkomsttoken för signaturer för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="207a3-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="207a3-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="207a3-158">-Confirm</span></span>
<span data-ttu-id="207a3-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="207a3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="207a3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207a3-160">-WhatIf</span></span>
<span data-ttu-id="207a3-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="207a3-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="207a3-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="207a3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="207a3-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207a3-163">-DefaultProfile</span></span>
<span data-ttu-id="207a3-164">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="207a3-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="207a3-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207a3-165">CommonParameters</span></span>
<span data-ttu-id="207a3-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="207a3-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207a3-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="207a3-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207a3-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="207a3-168">INPUTS</span></span>

## <span data-ttu-id="207a3-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="207a3-169">OUTPUTS</span></span>

### <span data-ttu-id="207a3-170">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="207a3-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="207a3-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="207a3-171">NOTES</span></span>

## <span data-ttu-id="207a3-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="207a3-172">RELATED LINKS</span></span>

[<span data-ttu-id="207a3-173">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="207a3-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="207a3-174">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="207a3-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="207a3-175">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="207a3-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="207a3-176">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="207a3-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="207a3-177">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="207a3-177">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="207a3-178">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="207a3-178">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="207a3-179">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="207a3-179">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="207a3-180">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="207a3-180">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="207a3-181">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="207a3-181">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


