---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 255db3680707af4e3658ce8a526cfa7b4a4d6f1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755082"
---
# <span data-ttu-id="da9f2-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da9f2-101">New-AzBatchPool</span></span>

## <span data-ttu-id="da9f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="da9f2-103">Skapar en pool i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="da9f2-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="da9f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da9f2-104">SYNTAX</span></span>

### <span data-ttu-id="da9f2-105">CloudServiceAndTargetDedicated (standard)</span><span class="sxs-lookup"><span data-stu-id="da9f2-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da9f2-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="da9f2-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
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

### <span data-ttu-id="da9f2-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="da9f2-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

### <span data-ttu-id="da9f2-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="da9f2-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

## <span data-ttu-id="da9f2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da9f2-109">DESCRIPTION</span></span>
<span data-ttu-id="da9f2-110">Cmdleten **New-AzBatchPool** skapar en pool i Azure Batch-tjänsten under kontot som anges av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="da9f2-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="da9f2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da9f2-111">EXAMPLES</span></span>

### <span data-ttu-id="da9f2-112">Exempel 1: skapa en ny pool med TargetDedicated parameter uppsättning med CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="da9f2-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="da9f2-113">Exempel 2: skapa en ny pool med TargetDedicated parameter uppsättning med VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="da9f2-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="da9f2-114">Det här kommandot skapar en ny pool med ID-förpool med TargetDedicated parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="da9f2-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="da9f2-115">Tilldelningen är tre datornoder.</span><span class="sxs-lookup"><span data-stu-id="da9f2-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="da9f2-116">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra.</span><span class="sxs-lookup"><span data-stu-id="da9f2-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="da9f2-117">Exempel 3: skapa en ny pool med hjälp av den Autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="da9f2-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="da9f2-118">Det här kommandot skapar en ny pool med ID-AutoScalePool med hjälp av en parameter uppsättning för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="da9f2-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="da9f2-119">Poolen är konfigurerad att använda små virtuella datorer med den senaste operativ system versionen av familjen fyra och målvärdet för datornoder bestäms av den automatiska skalnings formeln.</span><span class="sxs-lookup"><span data-stu-id="da9f2-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="da9f2-120">Exempel 4: skapa en pool med noder i ett undernät</span><span class="sxs-lookup"><span data-stu-id="da9f2-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="da9f2-121">Exempel 5: skapa en pool med anpassade användar konton</span><span class="sxs-lookup"><span data-stu-id="da9f2-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="da9f2-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da9f2-122">PARAMETERS</span></span>

### <span data-ttu-id="da9f2-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="da9f2-123">-ApplicationLicenses</span></span>
<span data-ttu-id="da9f2-124">Listan med program licenser som är tillgängliga för varje datornod i poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="da9f2-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="da9f2-125">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9f2-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="da9f2-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="da9f2-127">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="da9f2-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="da9f2-128">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="da9f2-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="da9f2-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="da9f2-129">-AutoScaleFormula</span></span>
<span data-ttu-id="da9f2-130">Anger formeln för automatisk skalning av poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-130">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="da9f2-131">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da9f2-131">-BatchContext</span></span>
<span data-ttu-id="da9f2-132">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="da9f2-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da9f2-133">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="da9f2-133">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da9f2-134">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="da9f2-134">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da9f2-135">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="da9f2-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da9f2-136">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="da9f2-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="da9f2-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="da9f2-137">-CertificateReferences</span></span>
<span data-ttu-id="da9f2-138">Anger certifikat som är associerade med poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="da9f2-139">Batch-tjänsten installerar de refererade certifikaten på varje datornod för poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9f2-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="da9f2-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="da9f2-141">Anger konfigurations inställningar för en pool baserad på Azure Cloud Service Platform.</span><span class="sxs-lookup"><span data-stu-id="da9f2-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="da9f2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9f2-142">-DefaultProfile</span></span>
<span data-ttu-id="da9f2-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da9f2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9f2-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="da9f2-144">-DisplayName</span></span>
<span data-ttu-id="da9f2-145">Anger visnings namnet för poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="da9f2-146">-ID</span><span class="sxs-lookup"><span data-stu-id="da9f2-146">-Id</span></span>
<span data-ttu-id="da9f2-147">Anger ID för den pool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="da9f2-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="da9f2-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="da9f2-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="da9f2-149">Anger att denna cmdlet konfigurerar poolen för direkt kommunikation mellan dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="da9f2-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="da9f2-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="da9f2-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="da9f2-151">Anger maximalt antal aktiviteter som kan köras på en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="da9f2-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="da9f2-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="da9f2-152">-Metadata</span></span>
<span data-ttu-id="da9f2-153">Anger metadata, som nycklar/värde par, som ska läggas till i den nya poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="da9f2-154">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="da9f2-154">The key is the metadata name.</span></span>
<span data-ttu-id="da9f2-155">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="da9f2-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="da9f2-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da9f2-156">-NetworkConfiguration</span></span>
<span data-ttu-id="da9f2-157">Nätverkets konfiguration för poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-157">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="da9f2-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="da9f2-158">-ResizeTimeout</span></span>
<span data-ttu-id="da9f2-159">Anger timeout för tilldelning av datornoder till poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="da9f2-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="da9f2-160">-StartTask</span></span>
<span data-ttu-id="da9f2-161">Anger den första uppgifts specifikationen för poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="da9f2-162">Starta-aktiviteten körs när en datornod ansluter till poolen, eller när noden Compute startas om eller återskapas.</span><span class="sxs-lookup"><span data-stu-id="da9f2-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="da9f2-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="da9f2-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="da9f2-164">Anger mål numret för dedikerade datornoder att tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9f2-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="da9f2-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="da9f2-166">Anger målvärdet för de beräknade datornoder som du vill tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="da9f2-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="da9f2-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="da9f2-168">Anger schema för aktivitets planering, till exempel ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="da9f2-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="da9f2-169">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="da9f2-169">-UserAccount</span></span>
<span data-ttu-id="da9f2-170">Listan över användar konton som ska skapas på varje nod i poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-170">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9f2-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="da9f2-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="da9f2-172">Anger konfigurations inställningar för en pool på infrastrukturen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="da9f2-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="da9f2-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="da9f2-173">-VirtualMachineSize</span></span>
<span data-ttu-id="da9f2-174">Anger storleken på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="da9f2-175">Mer information om storlekar för virtuell dator finns i storlekar för virtuella datorer https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) på Microsoft Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="da9f2-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="da9f2-176">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da9f2-176">-Confirm</span></span>
<span data-ttu-id="da9f2-177">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da9f2-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da9f2-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da9f2-178">-WhatIf</span></span>
<span data-ttu-id="da9f2-179">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da9f2-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da9f2-180">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da9f2-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da9f2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9f2-181">CommonParameters</span></span>
<span data-ttu-id="da9f2-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9f2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9f2-183">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9f2-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9f2-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da9f2-184">INPUTS</span></span>

### <span data-ttu-id="da9f2-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da9f2-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="da9f2-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da9f2-186">OUTPUTS</span></span>

### <span data-ttu-id="da9f2-187">System. Void</span><span class="sxs-lookup"><span data-stu-id="da9f2-187">System.Void</span></span>

## <span data-ttu-id="da9f2-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da9f2-188">NOTES</span></span>

## <span data-ttu-id="da9f2-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da9f2-189">RELATED LINKS</span></span>

[<span data-ttu-id="da9f2-190">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="da9f2-190">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="da9f2-191">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da9f2-191">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="da9f2-192">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da9f2-192">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="da9f2-193">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="da9f2-193">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

