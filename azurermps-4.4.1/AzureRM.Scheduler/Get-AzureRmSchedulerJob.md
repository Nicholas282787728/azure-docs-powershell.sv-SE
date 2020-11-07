---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756854"
---
# <span data-ttu-id="17c5e-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="17c5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="17c5e-103">Hämtar jobb för schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="17c5e-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17c5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17c5e-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="17c5e-106">Cmdleten **Get-AzureRmSchedulerJob** får Azure Scheduler-jobb.</span><span class="sxs-lookup"><span data-stu-id="17c5e-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="17c5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17c5e-107">EXAMPLES</span></span>

## <span data-ttu-id="17c5e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17c5e-108">PARAMETERS</span></span>

### <span data-ttu-id="17c5e-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="17c5e-109">-JobCollectionName</span></span>
<span data-ttu-id="17c5e-110">Anger namnet på en jobb samling som innehåller jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="17c5e-110">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="17c5e-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="17c5e-111">-JobName</span></span>
<span data-ttu-id="17c5e-112">Anger namnet på det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="17c5e-112">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c5e-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="17c5e-113">-JobState</span></span>
<span data-ttu-id="17c5e-114">Anger ett jobb tillstånd för att få jobb.</span><span class="sxs-lookup"><span data-stu-id="17c5e-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="17c5e-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="17c5e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17c5e-116">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="17c5e-116">Enabled</span></span> 
- <span data-ttu-id="17c5e-117">Aktiv</span><span class="sxs-lookup"><span data-stu-id="17c5e-117">Disabled</span></span> 
- <span data-ttu-id="17c5e-118">Fel</span><span class="sxs-lookup"><span data-stu-id="17c5e-118">Faulted</span></span> 
- <span data-ttu-id="17c5e-119">Rätta</span><span class="sxs-lookup"><span data-stu-id="17c5e-119">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="17c5e-121">Anger resurs gruppen för de jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="17c5e-121">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="17c5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c5e-122">-DefaultProfile</span></span>
<span data-ttu-id="17c5e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17c5e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17c5e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c5e-124">CommonParameters</span></span>
<span data-ttu-id="17c5e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c5e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c5e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c5e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c5e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17c5e-127">INPUTS</span></span>

## <span data-ttu-id="17c5e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17c5e-128">OUTPUTS</span></span>

### <span data-ttu-id="17c5e-129">Microsoft. Azure. commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="17c5e-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="17c5e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17c5e-130">NOTES</span></span>

## <span data-ttu-id="17c5e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17c5e-131">RELATED LINKS</span></span>

[<span data-ttu-id="17c5e-132">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="17c5e-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="17c5e-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="17c5e-134">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="17c5e-135">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="17c5e-136">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="17c5e-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="17c5e-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="17c5e-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="17c5e-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="17c5e-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="17c5e-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


