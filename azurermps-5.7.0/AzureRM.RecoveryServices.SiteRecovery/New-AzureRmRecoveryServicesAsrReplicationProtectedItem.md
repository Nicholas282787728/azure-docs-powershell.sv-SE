---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756791"
---
# <span data-ttu-id="7ba8c-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7ba8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ba8c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba8c-103">Aktiverar replikering för ett skrivskyddat ASR-objekt genom att skapa ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ba8c-104">SYNTAX</span></span>

### <span data-ttu-id="7ba8c-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="7ba8c-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba8c-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba8c-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba8c-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba8c-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba8c-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ba8c-110">DESCRIPTION</span></span>
<span data-ttu-id="7ba8c-111">Cmdleten **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="7ba8c-112">Använd denna cmdlet för att aktivera replikering för ett skrivskyddat objekt i ASR.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="7ba8c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ba8c-113">EXAMPLES</span></span>

### <span data-ttu-id="7ba8c-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ba8c-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7ba8c-115">Startar åtgärden för att skapa replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7ba8c-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7ba8c-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="7ba8c-117">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (vmWare to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="7ba8c-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="7ba8c-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7ba8c-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="7ba8c-119">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="7ba8c-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="7ba8c-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="7ba8c-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="7ba8c-121">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="7ba8c-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="7ba8c-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ba8c-122">PARAMETERS</span></span>

### <span data-ttu-id="7ba8c-123">-Konto</span><span class="sxs-lookup"><span data-stu-id="7ba8c-123">-Account</span></span>
<span data-ttu-id="7ba8c-124">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="7ba8c-125">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="7ba8c-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-126">-AzureToAzure</span></span>
<span data-ttu-id="7ba8c-127">Växla parameter för att ange att det replikerade objektet är en virtuell Azure-dator som replikerar till ett återställnings-Azure-område.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ba8c-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="7ba8c-129">Anger listan över virtuella dator diskar som ska replikeras och det lagrings konto för cacheminne som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-130">-AzureVmId</span></span>
<span data-ttu-id="7ba8c-131">Anger det ID för Azure VM som ska replikeras.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-131">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="7ba8c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ba8c-132">-Confirm</span></span>
<span data-ttu-id="7ba8c-133">Uppmaningar om att bekräfta innan operationen startas.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-133">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="7ba8c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba8c-134">-DefaultProfile</span></span>
<span data-ttu-id="7ba8c-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="7ba8c-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-136">-HyperVToAzure</span></span>
<span data-ttu-id="7ba8c-137">Byt parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-138">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-138">-IncludeDiskId</span></span>
<span data-ttu-id="7ba8c-139">Listan över diskar som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-139">The list of disks to include for replication.</span></span> <span data-ttu-id="7ba8c-140">Som standard ingår alla diskar.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-141">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-141">-LogStorageAccountId</span></span>
<span data-ttu-id="7ba8c-142">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ba8c-143">-Name</span></span>
<span data-ttu-id="7ba8c-144">Anger ett namn för det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="7ba8c-145">Namnet måste vara unikt inom valvet.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-145">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="7ba8c-146">-OS</span><span class="sxs-lookup"><span data-stu-id="7ba8c-146">-OS</span></span>
<span data-ttu-id="7ba8c-147">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-147">Specifies the operating system family.</span></span>
<span data-ttu-id="7ba8c-148">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="7ba8c-149">-OSDiskName</span></span>
<span data-ttu-id="7ba8c-150">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="7ba8c-151">-ProcessServer</span></span>
<span data-ttu-id="7ba8c-152">Den process server som ska användas för att replikera den här datorn.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="7ba8c-153">Använd listan med process servrar i ASR-Fabric som motsvarar konfigurations servern för att ange en.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-154">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-154">-ProtectableItem</span></span>
<span data-ttu-id="7ba8c-155">Anger objektet för skyddad ASR-objekt där replikering aktive ras.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7ba8c-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="7ba8c-157">Anger det mappnings objekt för ASR-skyddsagenten som motsvarar den replikeringsprincip som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="7ba8c-159">ID: t för AvailabilitySet som återställer datorn till i händelse av en redundans.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-160">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7ba8c-161">ID för det virtuella Azure-nätverket som återställer datorn till i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-162">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7ba8c-163">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-164">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="7ba8c-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="7ba8c-165">Under nätet i återställnings bara Azure Virtual Network som den misslyckade över virtuell dator ska kopplas till i händelse av redundans.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-166">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="7ba8c-167">Anger resurs-ID för återställnings moln tjänsten som ska redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-168">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7ba8c-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7ba8c-169">Anger ARM-identifieraren för den resurs grupp i vilken den virtuella datorn ska skapas i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="7ba8c-170">-RecoveryVmName</span></span>
<span data-ttu-id="7ba8c-171">Namn på den virtuella återställnings filen skapad efter redundans.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba8c-172">-ReplicationGroupName</span></span>
<span data-ttu-id="7ba8c-173">Anger namnet på den replikeringsgrupp som ska användas för att skapa enhetliga återställnings punkter med flera virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="7ba8c-174">Som standard skapas varje replikerat objekt i en grupp med egna och enhetliga återställnings punkter med flera virtuella datorer skapas inte.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="7ba8c-175">Använd bara det här alternativet om du behöver skapa enhetliga återställnings punkter med flera virtuella enheter i en grupp datorer genom att skydda alla datorer mot samma replikeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7ba8c-176">-VMwareToAzure</span></span>
<span data-ttu-id="7ba8c-177">Byt parameter för att ange att det replikerade objektet är en virtuell dator eller fysisk server som kommer att replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="7ba8c-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="7ba8c-178">-VmmToVmm</span></span>
<span data-ttu-id="7ba8c-179">Växla parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras mellan VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba8c-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7ba8c-180">-WaitForCompletion</span></span>
<span data-ttu-id="7ba8c-181">Anger att cmdleten ska vänta på att åtgärden slutförs innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="7ba8c-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba8c-182">-WhatIf</span></span>
<span data-ttu-id="7ba8c-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba8c-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba8c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba8c-185">CommonParameters</span></span>
<span data-ttu-id="7ba8c-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba8c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba8c-187">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba8c-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba8c-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ba8c-188">INPUTS</span></span>

### <span data-ttu-id="7ba8c-189">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7ba8c-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ba8c-190">OUTPUTS</span></span>

### <span data-ttu-id="7ba8c-191">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ba8c-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ba8c-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ba8c-192">NOTES</span></span>

## <span data-ttu-id="7ba8c-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ba8c-193">RELATED LINKS</span></span>

[<span data-ttu-id="7ba8c-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ba8c-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ba8c-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ba8c-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
