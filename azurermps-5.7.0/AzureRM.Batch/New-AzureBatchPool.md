---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586108"
---
# <span data-ttu-id="a178b-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a178b-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="a178b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a178b-102">SYNOPSIS</span></span>
<span data-ttu-id="a178b-103">Skapar en pool i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a178b-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a178b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a178b-104">SYNTAX</span></span>

### <span data-ttu-id="a178b-105">CloudServiceAndTargetDedicated (standard)</span><span class="sxs-lookup"><span data-stu-id="a178b-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a178b-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="a178b-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a178b-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="a178b-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a178b-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="a178b-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a178b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a178b-109">DESCRIPTION</span></span>
<span data-ttu-id="a178b-110">Cmdleten **New-AzureBatchPool** skapar en pool i Azure Batch-tjänsten under kontot som anges av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a178b-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="a178b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a178b-111">EXAMPLES</span></span>

### <span data-ttu-id="a178b-112">Exempel 1: skapa en ny pool med TargetDedicated parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="a178b-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="a178b-113">Det här kommandot skapar en ny pool med ID-förpool med TargetDedicated parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="a178b-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="a178b-114">Tilldelningen är tre datornoder.</span><span class="sxs-lookup"><span data-stu-id="a178b-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="a178b-115">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra.</span><span class="sxs-lookup"><span data-stu-id="a178b-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="a178b-116">Exempel 2: skapa en ny pool med hjälp av den Autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="a178b-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="a178b-117">Det här kommandot skapar en ny pool med ID-AutoScalePool med hjälp av en parameter uppsättning för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="a178b-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="a178b-118">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra och målvärdet för datornoder bestäms av den automatiska skalnings formeln.</span><span class="sxs-lookup"><span data-stu-id="a178b-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="a178b-119">Exempel 3: skapa en pool med noder i ett undernät</span><span class="sxs-lookup"><span data-stu-id="a178b-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="a178b-120">Exempel 4: skapa en pool med anpassade användar konton</span><span class="sxs-lookup"><span data-stu-id="a178b-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="a178b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a178b-121">PARAMETERS</span></span>

### <span data-ttu-id="a178b-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="a178b-122">-ApplicationLicenses</span></span>
<span data-ttu-id="a178b-123">Listan med program licenser som är tillgängliga för varje datornod i poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="a178b-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="a178b-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="a178b-126">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="a178b-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="a178b-127">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="a178b-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="a178b-128">-AutoScaleFormula</span></span>
<span data-ttu-id="a178b-129">Anger formeln för automatisk skalning av poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a178b-130">-BatchContext</span></span>
<span data-ttu-id="a178b-131">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a178b-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a178b-132">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a178b-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a178b-133">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="a178b-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a178b-134">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="a178b-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a178b-135">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a178b-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="a178b-136">-CertificateReferences</span></span>
<span data-ttu-id="a178b-137">Anger certifikat som är associerade med poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="a178b-138">Batch-tjänsten installerar de refererade certifikaten på varje datornod för poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a178b-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="a178b-140">Anger konfigurations inställningar för en pool baserad på Azure Cloud Service Platform.</span><span class="sxs-lookup"><span data-stu-id="a178b-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a178b-141">-DefaultProfile</span></span>
<span data-ttu-id="a178b-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a178b-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a178b-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a178b-143">-DisplayName</span></span>
<span data-ttu-id="a178b-144">Anger visnings namnet för poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-144">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="a178b-145">-ID</span><span class="sxs-lookup"><span data-stu-id="a178b-145">-Id</span></span>
<span data-ttu-id="a178b-146">Anger ID för den pool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a178b-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="a178b-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="a178b-148">Anger att denna cmdlet konfigurerar poolen för direkt kommunikation mellan dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="a178b-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="a178b-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="a178b-150">Anger maximalt antal aktiviteter som kan köras på en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="a178b-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="a178b-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a178b-151">-Metadata</span></span>
<span data-ttu-id="a178b-152">Anger metadata, som nycklar/värde par, som ska läggas till i den nya poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="a178b-153">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="a178b-153">The key is the metadata name.</span></span>
<span data-ttu-id="a178b-154">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="a178b-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a178b-155">-NetworkConfiguration</span></span>
<span data-ttu-id="a178b-156">Nätverkets konfiguration för poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="a178b-157">-ResizeTimeout</span></span>
<span data-ttu-id="a178b-158">Anger timeout för tilldelning av datornoder till poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="a178b-159">-StartTask</span></span>
<span data-ttu-id="a178b-160">Anger den första uppgifts specifikationen för poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="a178b-161">Starta-aktiviteten körs när en datornod ansluter till poolen, eller när noden Compute startas om eller återskapas.</span><span class="sxs-lookup"><span data-stu-id="a178b-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="a178b-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="a178b-163">Anger mål numret för dedikerade datornoder att tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="a178b-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="a178b-165">Anger målvärdet för de beräknade datornoder som du vill tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="a178b-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="a178b-167">Anger schema för aktivitets planering, till exempel ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="a178b-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-168">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="a178b-168">-UserAccount</span></span>
<span data-ttu-id="a178b-169">Listan över användar konton som ska skapas på varje nod i poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="a178b-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="a178b-171">Anger konfigurations inställningar för en pool på infrastrukturen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a178b-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="a178b-172">-VirtualMachineSize</span></span>
<span data-ttu-id="a178b-173">Anger storleken på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="a178b-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="a178b-174">Mer information om storlekar för virtuell dator finns i storlekar för virtuella datorer https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) på Microsoft Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="a178b-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a178b-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a178b-175">-Confirm</span></span>
<span data-ttu-id="a178b-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a178b-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a178b-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a178b-177">-WhatIf</span></span>
<span data-ttu-id="a178b-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a178b-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a178b-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a178b-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a178b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a178b-180">CommonParameters</span></span>
<span data-ttu-id="a178b-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a178b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a178b-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a178b-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a178b-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a178b-183">INPUTS</span></span>

### <span data-ttu-id="a178b-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a178b-184">BatchAccountContext</span></span>
<span data-ttu-id="a178b-185">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a178b-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a178b-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a178b-186">OUTPUTS</span></span>

## <span data-ttu-id="a178b-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a178b-187">NOTES</span></span>

## <span data-ttu-id="a178b-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a178b-188">RELATED LINKS</span></span>

[<span data-ttu-id="a178b-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a178b-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a178b-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a178b-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="a178b-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a178b-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="a178b-192">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a178b-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


