---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525229"
---
# <span data-ttu-id="f8d6e-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="f8d6e-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="f8d6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d6e-103">Uppdaterar replikeringsfrekvensen för det angivna replikerade skyddade objektet eller återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="f8d6e-104">Används för att återaktivera/omvända replikera ett misslyckat över replikerat objekt eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="f8d6e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8d6e-105">SYNTAX</span></span>

### <span data-ttu-id="f8d6e-106">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f8d6e-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f8d6e-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f8d6e-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8d6e-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f8d6e-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d6e-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f8d6e-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d6e-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8d6e-115">DESCRIPTION</span></span>
<span data-ttu-id="f8d6e-116">Cmdleten **Update-AzRecoveryServicesAsrProtectionDirection** uppdaterar replikeringsfrekvensen för det angivna Azure Site Recovery-objektet efter att commit-åtgärden slutförts.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="f8d6e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8d6e-117">EXAMPLES</span></span>

### <span data-ttu-id="f8d6e-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8d6e-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f8d6e-119">Starta uppdaterings åtgärden för den angivna återställnings planen och returnerar det ASR-objekt som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="f8d6e-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f8d6e-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="f8d6e-121">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och använda cachelagring (i samma region som VM).</span><span class="sxs-lookup"><span data-stu-id="f8d6e-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="f8d6e-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f8d6e-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="f8d6e-123">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och den angivna konfigurationen för diskduplicering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="f8d6e-124">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="f8d6e-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="f8d6e-125">Starta uppdaterings åtgärden för det angivna krypterade objektet för skyddad replikering i mål Azure-regionen som definieras av mappning av skydds behållare och den angivna konfigurationen för diskduplicering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="f8d6e-126">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="f8d6e-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="f8d6e-127">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och Använd lagrings utrymme för cacheminnet (i samma område som VM) och närhets placering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="f8d6e-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8d6e-128">PARAMETERS</span></span>

### <span data-ttu-id="f8d6e-129">-Konto</span><span class="sxs-lookup"><span data-stu-id="f8d6e-129">-Account</span></span>
<span data-ttu-id="f8d6e-130">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="f8d6e-131">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-132">-AzureToAzure</span></span>
<span data-ttu-id="f8d6e-133">Anger återställning av Azure till Azure-katastrofen.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d6e-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="f8d6e-135">Anger disk konfigurationen för katastrof återställning.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f8d6e-136">-AzureToVMware</span></span>
<span data-ttu-id="f8d6e-137">Anger scenariot för att växla Azure till vMWare.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-137">Specifies the switch azure to vMWare scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-138">-Data lager</span><span class="sxs-lookup"><span data-stu-id="f8d6e-138">-DataStore</span></span>
<span data-ttu-id="f8d6e-139">VMware data-Store som ska användas för vmdisk.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d6e-140">-DefaultProfile</span></span>
<span data-ttu-id="f8d6e-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f8d6e-142">-Riktning</span><span class="sxs-lookup"><span data-stu-id="f8d6e-142">-Direction</span></span>
<span data-ttu-id="f8d6e-143">Anger i vilken riktning som ska användas för uppdaterings åtgärden publicera en redundans.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="f8d6e-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f8d6e-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8d6e-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f8d6e-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="f8d6e-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f8d6e-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="f8d6e-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="f8d6e-148">Anger den hemliga URL-adressen för disk kryptering med version (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="f8d6e-150">Anger det hemliga valv-ID för disk kryptering (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-151">-HyperVToAzure</span></span>
<span data-ttu-id="f8d6e-152">Skydda en virtuell dator med Hyper-V efter återställning.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f8d6e-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f8d6e-154">Anger den URL för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="f8d6e-156">Anger det ID för disk krypterings nycklar (Azure Disk Encryption) som ska användas för återställning av virtuell dator efter redundans.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-157">-LogStorageAccountId</span></span>
<span data-ttu-id="f8d6e-158">Anger ID för lagrings konto för att lagra replikeringsuppsättningen för datorer.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="f8d6e-159">-MasterTarget</span></span>
<span data-ttu-id="f8d6e-160">Information om huvud mål servern.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="f8d6e-161">-ProcessServer</span></span>
<span data-ttu-id="f8d6e-162">Process server som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f8d6e-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="f8d6e-164">Skydds-containerMapping används för replikering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="f8d6e-166">Den tillgänglighets uppsättning som den virtuella datorn ska skapas på vid redundans</span><span class="sxs-lookup"><span data-stu-id="f8d6e-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f8d6e-168">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="f8d6e-170">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="f8d6e-172">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8d6e-173">-RecoveryPlan</span></span>
<span data-ttu-id="f8d6e-174">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="f8d6e-176">Resurs-ID för gruppen återställning efter omställning till redundans den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f8d6e-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f8d6e-178">Återställning resourceGroup ID för skyddad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f8d6e-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f8d6e-180">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="f8d6e-181">-RetentionVolume</span></span>
<span data-ttu-id="f8d6e-182">Lagrings volym på huvud mål servern som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f8d6e-183">-VmmToVmm</span></span>
<span data-ttu-id="f8d6e-184">Uppdatera replikeringsfrekvensen för en misslyckad dator med Hyper-V som skyddas mellan två VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f8d6e-185">-VMwareToAzure</span></span>
<span data-ttu-id="f8d6e-186">Uppdatera replikeringsfrekvensen från VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-186">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d6e-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8d6e-187">-Confirm</span></span>
<span data-ttu-id="f8d6e-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d6e-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d6e-189">-WhatIf</span></span>
<span data-ttu-id="f8d6e-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8d6e-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d6e-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d6e-192">CommonParameters</span></span>
<span data-ttu-id="f8d6e-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d6e-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d6e-194">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8d6e-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d6e-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8d6e-195">INPUTS</span></span>

### <span data-ttu-id="f8d6e-196">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8d6e-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f8d6e-197">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f8d6e-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f8d6e-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8d6e-198">OUTPUTS</span></span>

### <span data-ttu-id="f8d6e-199">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8d6e-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8d6e-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8d6e-200">NOTES</span></span>

## <span data-ttu-id="f8d6e-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8d6e-201">RELATED LINKS</span></span>
