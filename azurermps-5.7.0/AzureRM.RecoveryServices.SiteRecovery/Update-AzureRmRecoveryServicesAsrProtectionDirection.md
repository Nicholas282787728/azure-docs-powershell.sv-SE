---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574195"
---
# <span data-ttu-id="47593-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="47593-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="47593-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47593-102">SYNOPSIS</span></span>
<span data-ttu-id="47593-103">Uppdaterar replikeringsfrekvensen för det angivna replikerade skyddade objektet eller återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="47593-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="47593-104">Används för att återaktivera/omvända replikera ett misslyckat över replikerat objekt eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="47593-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47593-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47593-105">SYNTAX</span></span>

### <span data-ttu-id="47593-106">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="47593-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="47593-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47593-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="47593-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47593-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="47593-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47593-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="47593-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47593-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47593-115">DESCRIPTION</span></span>
<span data-ttu-id="47593-116">Cmdleten **Update-AzureRmRecoveryServicesAsrProtectionDirection** uppdaterar replikeringsfrekvensen för det angivna Azure Site Recovery-objektet efter att commit-åtgärden slutförts.</span><span class="sxs-lookup"><span data-stu-id="47593-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="47593-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47593-117">EXAMPLES</span></span>

### <span data-ttu-id="47593-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47593-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="47593-119">Starta uppdaterings åtgärden för den angivna återställnings planen och returnerar det ASR-objekt som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="47593-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="47593-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="47593-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="47593-121">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och använda cachelagring (i samma region som VM).</span><span class="sxs-lookup"><span data-stu-id="47593-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="47593-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="47593-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="47593-123">Starta uppdaterings åtgärden för det replikerade skyddade objektet i mål Azure-regionen som definieras av mappning av skydds behållare och den angivna konfigurationen för diskduplicering.</span><span class="sxs-lookup"><span data-stu-id="47593-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="47593-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47593-124">PARAMETERS</span></span>

### <span data-ttu-id="47593-125">-Konto</span><span class="sxs-lookup"><span data-stu-id="47593-125">-Account</span></span>
<span data-ttu-id="47593-126">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="47593-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="47593-127">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="47593-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-128">-AzureToAzure</span></span>
<span data-ttu-id="47593-129">Switch parameter som anger att den replikeringsfrekvens som uppdateras för replikerade virtuella Azure-datorer mellan två Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="47593-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="47593-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="47593-131">Anger listan över virtuella dator diskar som ska replikeras och det lagrings konto för cacheminne som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="47593-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="47593-132">-AzureToVMware</span></span>
<span data-ttu-id="47593-133">Uppdatera replikeringsfrekvensen från Azure till VMware.</span><span class="sxs-lookup"><span data-stu-id="47593-133">Update replication direction from Azure to Vmware.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47593-134">-Confirm</span></span>
<span data-ttu-id="47593-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47593-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-136">-Data lager</span><span class="sxs-lookup"><span data-stu-id="47593-136">-DataStore</span></span>
<span data-ttu-id="47593-137">VMware-datalagret som ska användas för vmdisk.</span><span class="sxs-lookup"><span data-stu-id="47593-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47593-138">-DefaultProfile</span></span>
<span data-ttu-id="47593-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47593-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="47593-140">-Riktning</span><span class="sxs-lookup"><span data-stu-id="47593-140">-Direction</span></span>
<span data-ttu-id="47593-141">Anger i vilken riktning som ska användas för uppdaterings åtgärden publicera en redundans.</span><span class="sxs-lookup"><span data-stu-id="47593-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="47593-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="47593-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47593-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="47593-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="47593-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="47593-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-145">-HyperVToAzure</span></span>
<span data-ttu-id="47593-146">Skydda en virtuell dator med Hyper-V efter återställning.</span><span class="sxs-lookup"><span data-stu-id="47593-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-147">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47593-147">-LogStorageAccountId</span></span>
<span data-ttu-id="47593-148">Anger ID för lagrings konto för att lagra replikeringsuppsättningen för datorer.</span><span class="sxs-lookup"><span data-stu-id="47593-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="47593-149">-MasterTarget</span></span>
<span data-ttu-id="47593-150">Information om huvud mål servern.</span><span class="sxs-lookup"><span data-stu-id="47593-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="47593-151">-ProcessServer</span></span>
<span data-ttu-id="47593-152">Process server som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="47593-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="47593-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="47593-154">Skydds-containerMapping används för replikering.</span><span class="sxs-lookup"><span data-stu-id="47593-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="47593-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="47593-156">Den tillgänglighets uppsättning som den virtuella datorn ska skapas på vid redundans</span><span class="sxs-lookup"><span data-stu-id="47593-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-157">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47593-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="47593-158">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="47593-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="47593-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="47593-160">Resurs-ID för återställnings moln tjänsten för att redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="47593-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47593-161">-RecoveryPlan</span></span>
<span data-ttu-id="47593-162">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="47593-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47593-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="47593-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="47593-164">Återställning resourceGroup ID för skyddad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="47593-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47593-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="47593-166">Anger ett skyddat objekt i ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="47593-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47593-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="47593-167">-RetentionVolume</span></span>
<span data-ttu-id="47593-168">Lagrings volym på huvud mål servern som ska användas.</span><span class="sxs-lookup"><span data-stu-id="47593-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="47593-169">-VMwareToAzure</span></span>
<span data-ttu-id="47593-170">Uppdatera replikeringsfrekvensen från VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="47593-170">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="47593-171">-VmmToVmm</span></span>
<span data-ttu-id="47593-172">Uppdatera replikeringsfrekvensen för en misslyckad dator med Hyper-V som skyddas mellan två VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="47593-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47593-173">-WhatIf</span></span>
<span data-ttu-id="47593-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47593-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47593-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47593-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47593-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47593-176">CommonParameters</span></span>
<span data-ttu-id="47593-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47593-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47593-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47593-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47593-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47593-179">INPUTS</span></span>

### <span data-ttu-id="47593-180">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47593-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="47593-181">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47593-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="47593-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47593-182">OUTPUTS</span></span>

### <span data-ttu-id="47593-183">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="47593-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="47593-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47593-184">NOTES</span></span>

## <span data-ttu-id="47593-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47593-185">RELATED LINKS</span></span>
