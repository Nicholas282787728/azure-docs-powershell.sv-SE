---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578476"
---
# <span data-ttu-id="46ccf-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="46ccf-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="46ccf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="46ccf-103">Skapar en pool i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="46ccf-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ccf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46ccf-104">SYNTAX</span></span>

### <span data-ttu-id="46ccf-105">CloudServiceAndTargetDedicated (standard)</span><span class="sxs-lookup"><span data-stu-id="46ccf-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46ccf-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="46ccf-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46ccf-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="46ccf-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46ccf-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="46ccf-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ccf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46ccf-109">DESCRIPTION</span></span>
<span data-ttu-id="46ccf-110">Cmdleten **New-AzureBatchPool** skapar en pool i Azure Batch-tjänsten under kontot som anges av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="46ccf-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="46ccf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46ccf-111">EXAMPLES</span></span>

### <span data-ttu-id="46ccf-112">Exempel 1: skapa en ny pool med TargetDedicated parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="46ccf-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="46ccf-113">Det här kommandot skapar en ny pool med ID-förpool med TargetDedicated parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="46ccf-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="46ccf-114">Tilldelningen är tre datornoder.</span><span class="sxs-lookup"><span data-stu-id="46ccf-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="46ccf-115">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra.</span><span class="sxs-lookup"><span data-stu-id="46ccf-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="46ccf-116">Exempel 2: skapa en ny pool med hjälp av den Autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="46ccf-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="46ccf-117">Det här kommandot skapar en ny pool med ID-AutoScalePool med hjälp av en parameter uppsättning för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="46ccf-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="46ccf-118">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra och målvärdet för datornoder bestäms av den automatiska skalnings formeln.</span><span class="sxs-lookup"><span data-stu-id="46ccf-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="46ccf-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46ccf-119">PARAMETERS</span></span>

### <span data-ttu-id="46ccf-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="46ccf-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="46ccf-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="46ccf-122">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="46ccf-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="46ccf-123">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="46ccf-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="46ccf-124">-AutoScaleFormula</span></span>
<span data-ttu-id="46ccf-125">Anger formeln för automatisk skalning av poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="46ccf-126">-BatchContext</span></span>
<span data-ttu-id="46ccf-127">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="46ccf-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="46ccf-128">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="46ccf-129">-CertificateReferences</span></span>
<span data-ttu-id="46ccf-130">Anger certifikat som är associerade med poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="46ccf-131">Batch-tjänsten installerar de refererade certifikaten på varje datornod för poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ccf-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="46ccf-133">Anger konfigurations inställningar för en pool baserad på Azure Cloud Service Platform.</span><span class="sxs-lookup"><span data-stu-id="46ccf-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="46ccf-134">-DisplayName</span></span>
<span data-ttu-id="46ccf-135">Anger visnings namnet för poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="46ccf-136">-ID</span><span class="sxs-lookup"><span data-stu-id="46ccf-136">-Id</span></span>
<span data-ttu-id="46ccf-137">Anger ID för den pool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="46ccf-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="46ccf-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="46ccf-139">Anger att denna cmdlet konfigurerar poolen för direkt kommunikation mellan dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="46ccf-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="46ccf-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="46ccf-141">Anger maximalt antal aktiviteter som kan köras på en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="46ccf-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="46ccf-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="46ccf-142">-Metadata</span></span>
<span data-ttu-id="46ccf-143">Anger metadata, som nycklar/värde par, som ska läggas till i den nya poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="46ccf-144">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="46ccf-144">The key is the metadata name.</span></span>
<span data-ttu-id="46ccf-145">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="46ccf-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ccf-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="46ccf-147">-ResizeTimeout</span></span>
<span data-ttu-id="46ccf-148">Anger timeout för tilldelning av datornoder till poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="46ccf-149">-StartTask</span></span>
<span data-ttu-id="46ccf-150">Anger den första uppgifts specifikationen för poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="46ccf-151">Starta-aktiviteten körs när en datornod ansluter till poolen, eller när noden Compute startas om eller återskapas.</span><span class="sxs-lookup"><span data-stu-id="46ccf-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="46ccf-152">-TargetDedicated</span></span>
<span data-ttu-id="46ccf-153">Anger målvärdet för datornoder att tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="46ccf-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="46ccf-155">Anger schema för aktivitets planering, till exempel ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="46ccf-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ccf-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="46ccf-157">Anger konfigurations inställningar för en pool på infrastrukturen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="46ccf-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ccf-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="46ccf-158">-VirtualMachineSize</span></span>
<span data-ttu-id="46ccf-159">Anger storleken på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="46ccf-160">Mer information om storlekar för virtuell dator finns i storlekar för virtuella datorer https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) på Microsoft Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="46ccf-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="46ccf-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46ccf-161">-Confirm</span></span>
<span data-ttu-id="46ccf-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46ccf-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ccf-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ccf-163">-WhatIf</span></span>
<span data-ttu-id="46ccf-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46ccf-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ccf-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46ccf-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ccf-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ccf-166">-DefaultProfile</span></span>
<span data-ttu-id="46ccf-167">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46ccf-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ccf-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ccf-168">CommonParameters</span></span>
<span data-ttu-id="46ccf-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ccf-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ccf-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ccf-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ccf-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46ccf-171">INPUTS</span></span>

### <span data-ttu-id="46ccf-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="46ccf-172">BatchAccountContext</span></span>
<span data-ttu-id="46ccf-173">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="46ccf-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="46ccf-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46ccf-174">OUTPUTS</span></span>

## <span data-ttu-id="46ccf-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46ccf-175">NOTES</span></span>

## <span data-ttu-id="46ccf-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46ccf-176">RELATED LINKS</span></span>

[<span data-ttu-id="46ccf-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="46ccf-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="46ccf-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="46ccf-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="46ccf-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="46ccf-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="46ccf-180">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="46ccf-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


