---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 48647fcc0382dd23f012d64aa70af364355c60e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755325"
---
# <span data-ttu-id="92a7b-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="92a7b-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="92a7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="92a7b-103">Uppdaterar replikeringsfrekvensen för det angivna replikerade skyddade objektet eller återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="92a7b-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="92a7b-104">Används för att återaktivera/omvända replikera ett misslyckat över replikerat objekt eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="92a7b-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92a7b-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92a7b-105">SYNTAX</span></span>

### <span data-ttu-id="92a7b-106">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="92a7b-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a7b-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="92a7b-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a7b-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a7b-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a7b-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="92a7b-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a7b-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a7b-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92a7b-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a7b-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="92a7b-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a7b-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="92a7b-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a7b-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92a7b-115">DESCRIPTION</span></span>
<span data-ttu-id="92a7b-116">Cmdleten **Update-AzureRmRecoveryServicesAsrProtectionDirection** uppdaterar replikeringsfrekvensen för det angivna Azure Site Recovery-objektet efter att commit-åtgärden slutförts.</span><span class="sxs-lookup"><span data-stu-id="92a7b-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="92a7b-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92a7b-117">EXAMPLES</span></span>

### <span data-ttu-id="92a7b-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92a7b-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="92a7b-119">Starta uppdaterings åtgärden för den angivna återställnings planen och returnerar det ASR-objekt som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="92a7b-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="92a7b-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="92a7b-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="92a7b-121">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och använda cachelagring (i samma region som VM).</span><span class="sxs-lookup"><span data-stu-id="92a7b-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="92a7b-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="92a7b-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="92a7b-123">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och den angivna konfigurationen för diskduplicering.</span><span class="sxs-lookup"><span data-stu-id="92a7b-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="92a7b-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92a7b-124">PARAMETERS</span></span>

### <span data-ttu-id="92a7b-125">-Konto</span><span class="sxs-lookup"><span data-stu-id="92a7b-125">-Account</span></span>
<span data-ttu-id="92a7b-126">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="92a7b-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="92a7b-127">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="92a7b-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="92a7b-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-128">-AzureToAzure</span></span>
<span data-ttu-id="92a7b-129">Switch parameter som anger att den replikeringsfrekvens som uppdateras för replikerade virtuella Azure-datorer mellan två Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="92a7b-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="92a7b-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="92a7b-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="92a7b-131">Anger listan över virtuella dator diskar som ska replikeras och det lagrings konto för cacheminne som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="92a7b-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="92a7b-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="92a7b-132">-AzureToVMware</span></span>
<span data-ttu-id="92a7b-133">Uppdatera replikeringsfrekvensen från Azure till VMware.</span><span class="sxs-lookup"><span data-stu-id="92a7b-133">Update replication direction from Azure to Vmware.</span></span>

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

### <span data-ttu-id="92a7b-134">-Data lager</span><span class="sxs-lookup"><span data-stu-id="92a7b-134">-DataStore</span></span>
<span data-ttu-id="92a7b-135">VMware-datalagret som ska användas för vmdisk.</span><span class="sxs-lookup"><span data-stu-id="92a7b-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="92a7b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a7b-136">-DefaultProfile</span></span>
<span data-ttu-id="92a7b-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92a7b-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="92a7b-138">-Riktning</span><span class="sxs-lookup"><span data-stu-id="92a7b-138">-Direction</span></span>
<span data-ttu-id="92a7b-139">Anger i vilken riktning som ska användas för uppdaterings åtgärden publicera en redundans.</span><span class="sxs-lookup"><span data-stu-id="92a7b-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="92a7b-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="92a7b-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92a7b-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="92a7b-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="92a7b-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="92a7b-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="92a7b-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-143">-HyperVToAzure</span></span>
<span data-ttu-id="92a7b-144">Skydda en virtuell dator med Hyper-V efter återställning.</span><span class="sxs-lookup"><span data-stu-id="92a7b-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="92a7b-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92a7b-145">-LogStorageAccountId</span></span>
<span data-ttu-id="92a7b-146">Anger ID för lagrings konto för att lagra replikeringsuppsättningen för datorer.</span><span class="sxs-lookup"><span data-stu-id="92a7b-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="92a7b-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="92a7b-147">-MasterTarget</span></span>
<span data-ttu-id="92a7b-148">Information om huvud mål servern.</span><span class="sxs-lookup"><span data-stu-id="92a7b-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="92a7b-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="92a7b-149">-ProcessServer</span></span>
<span data-ttu-id="92a7b-150">Process server som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="92a7b-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="92a7b-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="92a7b-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="92a7b-152">Skydds-containerMapping används för replikering.</span><span class="sxs-lookup"><span data-stu-id="92a7b-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="92a7b-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="92a7b-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="92a7b-154">Den tillgänglighets uppsättning som den virtuella datorn ska skapas på vid redundans</span><span class="sxs-lookup"><span data-stu-id="92a7b-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="92a7b-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92a7b-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="92a7b-156">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="92a7b-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="92a7b-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="92a7b-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="92a7b-158">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="92a7b-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="92a7b-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="92a7b-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="92a7b-160">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="92a7b-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="92a7b-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="92a7b-161">-RecoveryPlan</span></span>
<span data-ttu-id="92a7b-162">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="92a7b-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="92a7b-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="92a7b-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="92a7b-164">Återställning resourceGroup ID för skyddad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="92a7b-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="92a7b-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="92a7b-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="92a7b-166">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="92a7b-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="92a7b-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="92a7b-167">-RetentionVolume</span></span>
<span data-ttu-id="92a7b-168">Lagrings volym på huvud mål servern som ska användas.</span><span class="sxs-lookup"><span data-stu-id="92a7b-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="92a7b-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="92a7b-169">-VmmToVmm</span></span>
<span data-ttu-id="92a7b-170">Uppdatera replikeringsfrekvensen för en misslyckad dator med Hyper-V som skyddas mellan två VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="92a7b-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="92a7b-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="92a7b-171">-VMwareToAzure</span></span>
<span data-ttu-id="92a7b-172">Uppdatera replikeringsfrekvensen från VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="92a7b-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="92a7b-173">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92a7b-173">-Confirm</span></span>
<span data-ttu-id="92a7b-174">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92a7b-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a7b-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a7b-175">-WhatIf</span></span>
<span data-ttu-id="92a7b-176">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92a7b-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a7b-177">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92a7b-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a7b-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a7b-178">CommonParameters</span></span>
<span data-ttu-id="92a7b-179">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a7b-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a7b-180">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a7b-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a7b-181">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92a7b-181">INPUTS</span></span>

### <span data-ttu-id="92a7b-182">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="92a7b-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="92a7b-183">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="92a7b-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="92a7b-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92a7b-184">OUTPUTS</span></span>

### <span data-ttu-id="92a7b-185">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="92a7b-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92a7b-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92a7b-186">NOTES</span></span>

## <span data-ttu-id="92a7b-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92a7b-187">RELATED LINKS</span></span>
