---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757226"
---
# <span data-ttu-id="f1bd4-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="f1bd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bd4-103">Hämtar jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1bd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1bd4-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1bd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="f1bd4-106">Cmdleten **Get-AzureRmSchedulerJob** får Azure Scheduler-jobb.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="f1bd4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1bd4-107">EXAMPLES</span></span>

## <span data-ttu-id="f1bd4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1bd4-108">PARAMETERS</span></span>

### <span data-ttu-id="f1bd4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1bd4-109">-DefaultProfile</span></span>
<span data-ttu-id="f1bd4-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1bd4-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f1bd4-111">-JobCollectionName</span></span>
<span data-ttu-id="f1bd4-112">Anger namnet på en jobb samling som innehåller jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-112">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="f1bd4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1bd4-113">-JobName</span></span>
<span data-ttu-id="f1bd4-114">Anger namnet på det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bd4-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="f1bd4-115">-JobState</span></span>
<span data-ttu-id="f1bd4-116">Anger ett jobb tillstånd för att få jobb.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="f1bd4-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f1bd4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1bd4-118">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="f1bd4-118">Enabled</span></span> 
- <span data-ttu-id="f1bd4-119">Aktiv</span><span class="sxs-lookup"><span data-stu-id="f1bd4-119">Disabled</span></span> 
- <span data-ttu-id="f1bd4-120">Fel</span><span class="sxs-lookup"><span data-stu-id="f1bd4-120">Faulted</span></span> 
- <span data-ttu-id="f1bd4-121">Rätta</span><span class="sxs-lookup"><span data-stu-id="f1bd4-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bd4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bd4-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1bd4-123">Anger resurs gruppen för de jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-123">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="f1bd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bd4-124">CommonParameters</span></span>
<span data-ttu-id="f1bd4-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bd4-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1bd4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bd4-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1bd4-127">INPUTS</span></span>

### <span data-ttu-id="f1bd4-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="f1bd4-128">None</span></span>
<span data-ttu-id="f1bd4-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f1bd4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1bd4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1bd4-130">OUTPUTS</span></span>

### <span data-ttu-id="f1bd4-131">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f1bd4-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="f1bd4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1bd4-132">NOTES</span></span>

## <span data-ttu-id="f1bd4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1bd4-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1bd4-134">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f1bd4-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1bd4-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1bd4-136">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f1bd4-137">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f1bd4-138">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="f1bd4-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="f1bd4-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f1bd4-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f1bd4-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f1bd4-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1bd4-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


