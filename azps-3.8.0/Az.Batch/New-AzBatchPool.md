---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: def1c315a99592ca584baa10194e7b9238984506
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100444"
---
# <span data-ttu-id="0dc6c-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0dc6c-101">New-AzBatchPool</span></span>

## <span data-ttu-id="0dc6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0dc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc6c-103">Skapar en pool i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="0dc6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0dc6c-104">SYNTAX</span></span>

### <span data-ttu-id="0dc6c-105">CloudServiceAndTargetDedicated (standard)</span><span class="sxs-lookup"><span data-stu-id="0dc6c-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dc6c-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="0dc6c-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc6c-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="0dc6c-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dc6c-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="0dc6c-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc6c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0dc6c-109">DESCRIPTION</span></span>
<span data-ttu-id="0dc6c-110">Cmdleten **New-AzBatchPool** skapar en pool i Azure Batch-tjänsten under kontot som anges av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="0dc6c-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="0dc6c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0dc6c-111">EXAMPLES</span></span>

### <span data-ttu-id="0dc6c-112">Exempel 1: skapa en ny pool med TargetDedicated parameter uppsättning med CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="0dc6c-113">Poolen är konfigurerad att använda STANDARD_D1_V2 virtuella datorer med operativ system versionen av familjen fyra.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="0dc6c-114">Exempel 2: skapa en ny pool med TargetDedicated parameter uppsättning med VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="0dc6c-115">Det här kommandot skapar en ny pool med ID-förpool med TargetDedicated parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="0dc6c-116">Tilldelningen är tre datornoder.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="0dc6c-117">Poolen är konfigurerad att använda STANDARD_D1_V2 virtuella datorer med avbildningen Windows-2016-datacenter.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="0dc6c-118">Exempel 3: skapa en ny pool med hjälp av den Autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="0dc6c-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="0dc6c-119">Det här kommandot skapar en ny pool med ID-AutoScalePool med hjälp av en parameter uppsättning för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="0dc6c-120">Poolen är konfigurerad att använda STANDARD_D1_V2 virtuella datorer med Windows-2016-datacenter-avbildningen och målvärdet för datornoder bestäms av den automatiska skalnings formeln.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="0dc6c-121">Exempel 4: skapa en pool med noder i ett undernät</span><span class="sxs-lookup"><span data-stu-id="0dc6c-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="0dc6c-122">Exempel 5: skapa en pool med anpassade användar konton</span><span class="sxs-lookup"><span data-stu-id="0dc6c-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="0dc6c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0dc6c-123">PARAMETERS</span></span>

### <span data-ttu-id="0dc6c-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="0dc6c-124">-ApplicationLicenses</span></span>
<span data-ttu-id="0dc6c-125">Listan med program licenser som är tillgängliga för varje datornod i poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="0dc6c-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="0dc6c-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="0dc6c-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="0dc6c-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="0dc6c-128">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="0dc6c-129">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="0dc6c-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="0dc6c-130">-AutoScaleFormula</span></span>
<span data-ttu-id="0dc6c-131">Anger formeln för automatisk skalning av poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="0dc6c-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0dc6c-132">-BatchContext</span></span>
<span data-ttu-id="0dc6c-133">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0dc6c-134">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0dc6c-135">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0dc6c-136">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0dc6c-137">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0dc6c-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="0dc6c-138">-CertificateReferences</span></span>
<span data-ttu-id="0dc6c-139">Anger certifikat som är associerade med poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="0dc6c-140">Batch-tjänsten installerar de refererade certifikaten på varje datornod för poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="0dc6c-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="0dc6c-142">Anger konfigurations inställningar för en pool baserad på Azure Cloud Service Platform.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="0dc6c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc6c-143">-DefaultProfile</span></span>
<span data-ttu-id="0dc6c-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dc6c-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0dc6c-145">-DisplayName</span></span>
<span data-ttu-id="0dc6c-146">Anger visnings namnet för poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="0dc6c-147">-ID</span><span class="sxs-lookup"><span data-stu-id="0dc6c-147">-Id</span></span>
<span data-ttu-id="0dc6c-148">Anger ID för den pool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="0dc6c-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="0dc6c-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="0dc6c-150">Anger att denna cmdlet konfigurerar poolen för direkt kommunikation mellan dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="0dc6c-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="0dc6c-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="0dc6c-152">Anger maximalt antal aktiviteter som kan köras på en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="0dc6c-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0dc6c-153">-Metadata</span></span>
<span data-ttu-id="0dc6c-154">Anger metadata, som nycklar/värde par, som ska läggas till i den nya poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="0dc6c-155">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-155">The key is the metadata name.</span></span>
<span data-ttu-id="0dc6c-156">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="0dc6c-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-157">-MountConfiguration</span></span>
<span data-ttu-id="0dc6c-158">En lista över fil system att montera på varje nod i poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="0dc6c-159">Detta stödjer Azure filer, NFS, CIFS/SMB och Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc6c-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-160">-NetworkConfiguration</span></span>
<span data-ttu-id="0dc6c-161">Nätverkets konfiguration för poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="0dc6c-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="0dc6c-162">-ResizeTimeout</span></span>
<span data-ttu-id="0dc6c-163">Anger timeout för tilldelning av datornoder till poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="0dc6c-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="0dc6c-164">-StartTask</span></span>
<span data-ttu-id="0dc6c-165">Anger den första uppgifts specifikationen för poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="0dc6c-166">Starta-aktiviteten körs när en datornod ansluter till poolen, eller när noden Compute startas om eller återskapas.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="0dc6c-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="0dc6c-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="0dc6c-168">Anger mål numret för dedikerade datornoder att tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="0dc6c-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="0dc6c-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="0dc6c-170">Anger målvärdet för de beräknade datornoder som du vill tilldela till poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="0dc6c-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="0dc6c-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="0dc6c-172">Anger schema för aktivitets planering, till exempel ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="0dc6c-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="0dc6c-173">-UserAccount</span></span>
<span data-ttu-id="0dc6c-174">Listan över användar konton som ska skapas på varje nod i poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="0dc6c-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc6c-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="0dc6c-176">Anger konfigurations inställningar för en pool på infrastrukturen för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="0dc6c-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="0dc6c-177">-VirtualMachineSize</span></span>
<span data-ttu-id="0dc6c-178">Anger storleken på de virtuella datorerna i poolen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="0dc6c-179">Mer information om storlekar för virtuell dator finns i storlekar för virtuella datorer https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) på Microsoft Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="0dc6c-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0dc6c-180">-Confirm</span></span>
<span data-ttu-id="0dc6c-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc6c-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc6c-182">-WhatIf</span></span>
<span data-ttu-id="0dc6c-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc6c-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc6c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc6c-185">CommonParameters</span></span>
<span data-ttu-id="0dc6c-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc6c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc6c-187">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dc6c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc6c-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0dc6c-188">INPUTS</span></span>

### <span data-ttu-id="0dc6c-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0dc6c-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0dc6c-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0dc6c-190">OUTPUTS</span></span>

### <span data-ttu-id="0dc6c-191">System. Void</span><span class="sxs-lookup"><span data-stu-id="0dc6c-191">System.Void</span></span>

## <span data-ttu-id="0dc6c-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0dc6c-192">NOTES</span></span>

## <span data-ttu-id="0dc6c-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0dc6c-193">RELATED LINKS</span></span>

[<span data-ttu-id="0dc6c-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0dc6c-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0dc6c-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0dc6c-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="0dc6c-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0dc6c-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="0dc6c-197">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0dc6c-197">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


