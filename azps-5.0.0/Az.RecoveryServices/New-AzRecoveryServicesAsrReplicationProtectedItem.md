---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269148"
---
# <span data-ttu-id="a0d20-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="a0d20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0d20-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d20-103">Aktiverar replikering för ett skrivskyddat ASR-objekt genom att skapa ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="a0d20-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="a0d20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0d20-104">SYNTAX</span></span>

### <span data-ttu-id="a0d20-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="a0d20-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="a0d20-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d20-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="a0d20-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d20-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0d20-112">DESCRIPTION</span></span>
<span data-ttu-id="a0d20-113">Cmdleten **New-AzRecoveryServicesAsrReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="a0d20-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="a0d20-114">Använd denna cmdlet för att aktivera replikering för ett skrivskyddat objekt i ASR.</span><span class="sxs-lookup"><span data-stu-id="a0d20-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="a0d20-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0d20-115">EXAMPLES</span></span>

### <span data-ttu-id="a0d20-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0d20-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="a0d20-117">Startar åtgärden för att skapa replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a0d20-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a0d20-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a0d20-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="a0d20-119">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (vmWare to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="a0d20-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="a0d20-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a0d20-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="a0d20-121">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="a0d20-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="a0d20-122">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a0d20-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="a0d20-123">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="a0d20-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="a0d20-124">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="a0d20-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="a0d20-125">Startar åtgärden för att skapa replikerat objekt för det angivna systemfilerna för automatisk system återställning inklusive selektiva diskar och returnerar ASR-jobbet som används för att spåra åtgärden (vmWare to Azure scenario) med valda diskar.</span><span class="sxs-lookup"><span data-stu-id="a0d20-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="a0d20-126">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="a0d20-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="a0d20-127">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="a0d20-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="a0d20-128">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot). För den information om redundans som skickades till cmdlet för kryptering används den.</span><span class="sxs-lookup"><span data-stu-id="a0d20-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="a0d20-129">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="a0d20-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="a0d20-130">Startar åtgärden Skapa replikerat objekt för en virtuell dator inom närhet och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="a0d20-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="a0d20-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0d20-131">PARAMETERS</span></span>

### <span data-ttu-id="a0d20-132">-Konto</span><span class="sxs-lookup"><span data-stu-id="a0d20-132">-Account</span></span>
<span data-ttu-id="a0d20-133">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="a0d20-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="a0d20-134">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="a0d20-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-135">-AzureToAzure</span></span>
<span data-ttu-id="a0d20-136">Switch parameter anger att det replikerade objektet ska skapas i Azure-scenario.</span><span class="sxs-lookup"><span data-stu-id="a0d20-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0d20-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="a0d20-138">Anger den disk konfiguration som används för att använda den virtuella datorn för Azure till Azure katastrof återställnings scenario.</span><span class="sxs-lookup"><span data-stu-id="a0d20-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="a0d20-139">-AzureVmId</span></span>
<span data-ttu-id="a0d20-140">Anger ID för Azure VM för katastrof återställnings skydd i återställnings området.</span><span class="sxs-lookup"><span data-stu-id="a0d20-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d20-141">-DefaultProfile</span></span>
<span data-ttu-id="a0d20-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d20-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a0d20-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="a0d20-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="a0d20-144">Anger den hemliga URL-adressen för disk kryptering med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a0d20-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a0d20-146">Anger resurs-ID för disk krypterings uppsättningen som ska användas för kryptering av de hanterade diskarna.</span><span class="sxs-lookup"><span data-stu-id="a0d20-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a0d20-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="a0d20-148">Anger det hemliga valv-ID för disk kryptering (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="a0d20-149">-DiskType</span></span>
<span data-ttu-id="a0d20-150">Anger den hanterade disk typen för återställning av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a0d20-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-151">-HyperVToAzure</span></span>
<span data-ttu-id="a0d20-152">Byt parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d20-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="a0d20-153">-IncludeDiskId</span></span>
<span data-ttu-id="a0d20-154">Listan över diskar som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="a0d20-154">The list of disks to include for replication.</span></span> <span data-ttu-id="a0d20-155">Som standard ingår alla diskar.</span><span class="sxs-lookup"><span data-stu-id="a0d20-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a0d20-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="a0d20-157">Anger disk konfigurations inmatning för vMWare-disk-ID för att skydda från ett specifikt skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="a0d20-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a0d20-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a0d20-159">Anger URL-adressen till den disk krypterings plats med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a0d20-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="a0d20-161">Anger den disk krypterings nycklar-valv-ID (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a0d20-162">-LogStorageAccountId</span></span>
<span data-ttu-id="a0d20-163">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="a0d20-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-164">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0d20-164">-Name</span></span>
<span data-ttu-id="a0d20-165">Anger ett namn för det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="a0d20-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="a0d20-166">Namnet måste vara unikt inom valvet.</span><span class="sxs-lookup"><span data-stu-id="a0d20-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="a0d20-167">-OS</span><span class="sxs-lookup"><span data-stu-id="a0d20-167">-OS</span></span>
<span data-ttu-id="a0d20-168">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="a0d20-168">Specifies the operating system family.</span></span>
<span data-ttu-id="a0d20-169">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="a0d20-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="a0d20-170">-OSDiskName</span></span>
<span data-ttu-id="a0d20-171">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="a0d20-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="a0d20-172">-ProcessServer</span></span>
<span data-ttu-id="a0d20-173">Den process server som ska användas för att replikera den här datorn.</span><span class="sxs-lookup"><span data-stu-id="a0d20-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="a0d20-174">Använd listan med process servrar i ASR-Fabric som motsvarar konfigurations servern för att ange en.</span><span class="sxs-lookup"><span data-stu-id="a0d20-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-175">-ProtectableItem</span></span>
<span data-ttu-id="a0d20-176">Anger objektet för skyddad ASR-objekt där replikering aktive ras.</span><span class="sxs-lookup"><span data-stu-id="a0d20-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a0d20-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="a0d20-178">Anger det mappnings objekt för ASR-skyddsagenten som motsvarar den replikeringsprincip som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="a0d20-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="a0d20-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="a0d20-180">ID: t för AvailabilitySet som återställer datorn till i händelse av en redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="a0d20-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="a0d20-182">Anger tillgänglighets zonen för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a0d20-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a0d20-184">ID för det virtuella Azure-nätverket som återställer datorn till i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="a0d20-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a0d20-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a0d20-186">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="a0d20-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="a0d20-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="a0d20-188">Under nätet i återställnings bara Azure Virtual Network som den misslyckade över virtuell dator ska kopplas till i händelse av redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a0d20-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="a0d20-190">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="a0d20-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="a0d20-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="a0d20-192">Anger resurs-ID för återställnings moln tjänsten som ska redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="a0d20-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a0d20-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="a0d20-194">Ange grupp-ID för närhet som används av den virtuella dator för mål återställning.</span><span class="sxs-lookup"><span data-stu-id="a0d20-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a0d20-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a0d20-196">Anger ARM-identifieraren för den resurs grupp i vilken den virtuella datorn ska skapas i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="a0d20-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="a0d20-197">-RecoveryVmName</span></span>
<span data-ttu-id="a0d20-198">Namn på den virtuella återställnings filen skapad efter redundans.</span><span class="sxs-lookup"><span data-stu-id="a0d20-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d20-199">-ReplicationGroupName</span></span>
<span data-ttu-id="a0d20-200">Anger namnet på den replikeringsgrupp som ska användas för att skapa enhetliga återställnings punkter med flera virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="a0d20-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="a0d20-201">Som standard skapas varje replikerat objekt i en grupp med egna och enhetliga återställnings punkter med flera virtuella datorer skapas inte.</span><span class="sxs-lookup"><span data-stu-id="a0d20-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="a0d20-202">Använd bara det här alternativet om du behöver skapa enhetliga återställnings punkter med flera virtuella enheter i en grupp datorer genom att skydda alla datorer mot samma replikeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="a0d20-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a0d20-203">-VmmToVmm</span></span>
<span data-ttu-id="a0d20-204">Växla parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras mellan VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="a0d20-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a0d20-205">-VMwareToAzure</span></span>
<span data-ttu-id="a0d20-206">Byt parameter för att ange att det replikerade objektet är en virtuell dator eller fysisk server som kommer att replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d20-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a0d20-207">-WaitForCompletion</span></span>
<span data-ttu-id="a0d20-208">Anger att cmdleten ska vänta på att åtgärden slutförs innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="a0d20-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="a0d20-209">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0d20-209">-Confirm</span></span>
<span data-ttu-id="a0d20-210">Uppmaningar om att bekräfta innan operationen startas.</span><span class="sxs-lookup"><span data-stu-id="a0d20-210">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d20-211">-WhatIf</span></span>
<span data-ttu-id="a0d20-212">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0d20-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d20-213">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0d20-213">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d20-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d20-214">CommonParameters</span></span>
<span data-ttu-id="a0d20-215">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d20-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d20-216">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0d20-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d20-217">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0d20-217">INPUTS</span></span>

### <span data-ttu-id="a0d20-218">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="a0d20-219">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0d20-219">OUTPUTS</span></span>

### <span data-ttu-id="a0d20-220">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a0d20-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a0d20-221">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0d20-221">NOTES</span></span>

## <span data-ttu-id="a0d20-222">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0d20-222">RELATED LINKS</span></span>

[<span data-ttu-id="a0d20-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a0d20-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a0d20-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0d20-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
