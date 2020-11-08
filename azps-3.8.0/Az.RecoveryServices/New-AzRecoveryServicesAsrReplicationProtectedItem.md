---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3d9cd1bface4175e60b45d6865815f1a4ea964f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090414"
---
# <span data-ttu-id="6055a-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6055a-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6055a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6055a-102">SYNOPSIS</span></span>
<span data-ttu-id="6055a-103">Aktiverar replikering för ett skrivskyddat ASR-objekt genom att skapa ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="6055a-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="6055a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6055a-104">SYNTAX</span></span>

### <span data-ttu-id="6055a-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="6055a-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="6055a-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6055a-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="6055a-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6055a-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6055a-112">DESCRIPTION</span></span>
<span data-ttu-id="6055a-113">Cmdleten **New-AzRecoveryServicesAsrReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="6055a-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="6055a-114">Använd denna cmdlet för att aktivera replikering för ett skrivskyddat objekt i ASR.</span><span class="sxs-lookup"><span data-stu-id="6055a-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="6055a-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6055a-115">EXAMPLES</span></span>

### <span data-ttu-id="6055a-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6055a-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="6055a-117">Startar åtgärden för att skapa replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6055a-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6055a-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6055a-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="6055a-119">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (vmWare to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="6055a-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="6055a-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6055a-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="6055a-121">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="6055a-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="6055a-122">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="6055a-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="6055a-123">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="6055a-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="6055a-124">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="6055a-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="6055a-125">Startar åtgärden för att skapa replikerat objekt för det angivna systemfilerna för automatisk system återställning inklusive selektiva diskar och returnerar ASR-jobbet som används för att spåra åtgärden (vmWare to Azure scenario) med valda diskar.</span><span class="sxs-lookup"><span data-stu-id="6055a-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="6055a-126">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="6055a-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="6055a-127">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="6055a-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="6055a-128">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot). För den information om redundans som skickades till cmdlet för kryptering används den.</span><span class="sxs-lookup"><span data-stu-id="6055a-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

## <span data-ttu-id="6055a-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6055a-129">PARAMETERS</span></span>

### <span data-ttu-id="6055a-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="6055a-130">-Account</span></span>
<span data-ttu-id="6055a-131">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="6055a-131">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="6055a-132">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="6055a-132">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="6055a-133">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-133">-AzureToAzure</span></span>
<span data-ttu-id="6055a-134">Switch parameter anger att det replikerade objektet ska skapas i Azure-scenario.</span><span class="sxs-lookup"><span data-stu-id="6055a-134">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="6055a-135">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6055a-135">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="6055a-136">Anger den disk konfiguration som används för att använda den virtuella datorn för Azure till Azure katastrof återställnings scenario.</span><span class="sxs-lookup"><span data-stu-id="6055a-136">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="6055a-137">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="6055a-137">-AzureVmId</span></span>
<span data-ttu-id="6055a-138">Anger ID för Azure VM för katastrof återställnings skydd i återställnings området.</span><span class="sxs-lookup"><span data-stu-id="6055a-138">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="6055a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6055a-139">-DefaultProfile</span></span>
<span data-ttu-id="6055a-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6055a-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6055a-141">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="6055a-141">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="6055a-142">Anger den hemliga URL-adressen för disk kryptering med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-142">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6055a-143">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6055a-143">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6055a-144">Anger resurs-ID för disk krypterings uppsättningen som ska användas för kryptering av de hanterade diskarna.</span><span class="sxs-lookup"><span data-stu-id="6055a-144">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="6055a-145">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6055a-145">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="6055a-146">Anger det hemliga valv-ID för disk kryptering (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-146">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6055a-147">-DiskType</span><span class="sxs-lookup"><span data-stu-id="6055a-147">-DiskType</span></span>
<span data-ttu-id="6055a-148">Anger den hanterade disk typen för återställning av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6055a-148">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="6055a-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-149">-HyperVToAzure</span></span>
<span data-ttu-id="6055a-150">Byt parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="6055a-150">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="6055a-151">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="6055a-151">-IncludeDiskId</span></span>
<span data-ttu-id="6055a-152">Listan över diskar som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="6055a-152">The list of disks to include for replication.</span></span> <span data-ttu-id="6055a-153">Som standard ingår alla diskar.</span><span class="sxs-lookup"><span data-stu-id="6055a-153">By default all disks are included.</span></span>

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

### <span data-ttu-id="6055a-154">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="6055a-154">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="6055a-155">Anger disk konfigurations inmatning för vMWare-disk-ID för att skydda från ett specifikt skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="6055a-155">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="6055a-156">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6055a-156">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6055a-157">Anger URL-adressen till den disk krypterings plats med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-157">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6055a-158">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="6055a-158">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="6055a-159">Anger den disk krypterings nycklar-valv-ID (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-159">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="6055a-160">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6055a-160">-LogStorageAccountId</span></span>
<span data-ttu-id="6055a-161">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="6055a-161">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="6055a-162">-Namn</span><span class="sxs-lookup"><span data-stu-id="6055a-162">-Name</span></span>
<span data-ttu-id="6055a-163">Anger ett namn för det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="6055a-163">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="6055a-164">Namnet måste vara unikt inom valvet.</span><span class="sxs-lookup"><span data-stu-id="6055a-164">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="6055a-165">-OS</span><span class="sxs-lookup"><span data-stu-id="6055a-165">-OS</span></span>
<span data-ttu-id="6055a-166">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="6055a-166">Specifies the operating system family.</span></span>
<span data-ttu-id="6055a-167">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="6055a-167">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="6055a-168">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="6055a-168">-OSDiskName</span></span>
<span data-ttu-id="6055a-169">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="6055a-169">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="6055a-170">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="6055a-170">-ProcessServer</span></span>
<span data-ttu-id="6055a-171">Den process server som ska användas för att replikera den här datorn.</span><span class="sxs-lookup"><span data-stu-id="6055a-171">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="6055a-172">Använd listan med process servrar i ASR-Fabric som motsvarar konfigurations servern för att ange en.</span><span class="sxs-lookup"><span data-stu-id="6055a-172">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="6055a-173">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6055a-173">-ProtectableItem</span></span>
<span data-ttu-id="6055a-174">Anger objektet för skyddad ASR-objekt där replikering aktive ras.</span><span class="sxs-lookup"><span data-stu-id="6055a-174">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="6055a-175">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6055a-175">-ProtectionContainerMapping</span></span>
<span data-ttu-id="6055a-176">Anger det mappnings objekt för ASR-skyddsagenten som motsvarar den replikeringsprincip som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="6055a-176">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="6055a-177">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6055a-177">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="6055a-178">ID: t för AvailabilitySet som återställer datorn till i händelse av en redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-178">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="6055a-179">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="6055a-179">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="6055a-180">Anger tillgänglighets zonen för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-180">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="6055a-181">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6055a-181">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6055a-182">ID för det virtuella Azure-nätverket som återställer datorn till i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="6055a-182">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="6055a-183">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6055a-183">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6055a-184">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="6055a-184">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="6055a-185">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="6055a-185">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="6055a-186">Under nätet i återställnings bara Azure Virtual Network som den misslyckade över virtuell dator ska kopplas till i händelse av redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-186">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="6055a-187">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6055a-187">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="6055a-188">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="6055a-188">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="6055a-189">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="6055a-189">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6055a-190">Anger resurs-ID för återställnings moln tjänsten som ska redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="6055a-190">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="6055a-191">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6055a-191">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6055a-192">Anger ARM-identifieraren för den resurs grupp i vilken den virtuella datorn ska skapas i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="6055a-192">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="6055a-193">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="6055a-193">-RecoveryVmName</span></span>
<span data-ttu-id="6055a-194">Namn på den virtuella återställnings filen skapad efter redundans.</span><span class="sxs-lookup"><span data-stu-id="6055a-194">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="6055a-195">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="6055a-195">-ReplicationGroupName</span></span>
<span data-ttu-id="6055a-196">Anger namnet på den replikeringsgrupp som ska användas för att skapa enhetliga återställnings punkter med flera virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="6055a-196">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="6055a-197">Som standard skapas varje replikerat objekt i en grupp med egna och enhetliga återställnings punkter med flera virtuella datorer skapas inte.</span><span class="sxs-lookup"><span data-stu-id="6055a-197">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="6055a-198">Använd bara det här alternativet om du behöver skapa enhetliga återställnings punkter med flera virtuella enheter i en grupp datorer genom att skydda alla datorer mot samma replikeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="6055a-198">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="6055a-199">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="6055a-199">-VmmToVmm</span></span>
<span data-ttu-id="6055a-200">Växla parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras mellan VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="6055a-200">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="6055a-201">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6055a-201">-VMwareToAzure</span></span>
<span data-ttu-id="6055a-202">Byt parameter för att ange att det replikerade objektet är en virtuell dator eller fysisk server som kommer att replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="6055a-202">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="6055a-203">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6055a-203">-WaitForCompletion</span></span>
<span data-ttu-id="6055a-204">Anger att cmdleten ska vänta på att åtgärden slutförs innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="6055a-204">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="6055a-205">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6055a-205">-Confirm</span></span>
<span data-ttu-id="6055a-206">Uppmaningar om att bekräfta innan operationen startas.</span><span class="sxs-lookup"><span data-stu-id="6055a-206">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="6055a-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6055a-207">-WhatIf</span></span>
<span data-ttu-id="6055a-208">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6055a-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6055a-209">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6055a-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6055a-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6055a-210">CommonParameters</span></span>
<span data-ttu-id="6055a-211">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6055a-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6055a-212">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6055a-212">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6055a-213">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6055a-213">INPUTS</span></span>

### <span data-ttu-id="6055a-214">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6055a-214">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="6055a-215">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6055a-215">OUTPUTS</span></span>

### <span data-ttu-id="6055a-216">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6055a-216">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6055a-217">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6055a-217">NOTES</span></span>

## <span data-ttu-id="6055a-218">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6055a-218">RELATED LINKS</span></span>

[<span data-ttu-id="6055a-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6055a-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6055a-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6055a-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6055a-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6055a-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)