---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572659"
---
# <span data-ttu-id="0e6c4-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="0e6c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6c4-103">Aktiverar replikering för ett skrivskyddat ASR-objekt genom att skapa ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e6c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e6c4-104">SYNTAX</span></span>

### <span data-ttu-id="0e6c4-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="0e6c4-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6c4-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6c4-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6c4-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6c4-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6c4-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="0e6c4-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6c4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e6c4-111">DESCRIPTION</span></span>
<span data-ttu-id="0e6c4-112">Cmdleten **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="0e6c4-113">Använd denna cmdlet för att aktivera replikering för ett skrivskyddat objekt i ASR.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="0e6c4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e6c4-114">EXAMPLES</span></span>

### <span data-ttu-id="0e6c4-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e6c4-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="0e6c4-116">Startar åtgärden för att skapa replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="0e6c4-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0e6c4-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="0e6c4-118">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (vmWare to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="0e6c4-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="0e6c4-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0e6c4-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="0e6c4-120">Startar åtgärden för att skapa ett replikerat objekt för det angivna ASR-objektet och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="0e6c4-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="0e6c4-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="0e6c4-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="0e6c4-122">Startar åtgärden Skapa replikerat objekt för det angivna VmId och returnerar det ASR-jobb som används för att spåra åtgärden (Azure to Azure-scenariot).</span><span class="sxs-lookup"><span data-stu-id="0e6c4-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="0e6c4-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e6c4-123">PARAMETERS</span></span>

### <span data-ttu-id="0e6c4-124">-Konto</span><span class="sxs-lookup"><span data-stu-id="0e6c4-124">-Account</span></span>
<span data-ttu-id="0e6c4-125">Kör som-konto som ska användas för att pusha installera mobilitets tjänsten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="0e6c4-126">Måste finnas i listan med kör som-konton i ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="0e6c4-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-127">-AzureToAzure</span></span>
<span data-ttu-id="0e6c4-128">Växla parameter för att ange att det replikerade objektet är en virtuell Azure-dator som replikerar till ett återställnings-Azure-område.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="0e6c4-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e6c4-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="0e6c4-130">Anger listan över virtuella dator diskar som ska replikeras och det lagrings konto för cacheminne som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="0e6c4-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-131">-AzureVmId</span></span>
<span data-ttu-id="0e6c4-132">Anger det ID för Azure VM som ska replikeras.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="0e6c4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6c4-133">-DefaultProfile</span></span>
<span data-ttu-id="0e6c4-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0e6c4-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-135">-HyperVToAzure</span></span>
<span data-ttu-id="0e6c4-136">Byt parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="0e6c4-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-137">-IncludeDiskId</span></span>
<span data-ttu-id="0e6c4-138">Listan över diskar som ska ingå i replikeringen.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-138">The list of disks to include for replication.</span></span> <span data-ttu-id="0e6c4-139">Som standard ingår alla diskar.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-140">-LogStorageAccountId</span></span>
<span data-ttu-id="0e6c4-141">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="0e6c4-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e6c4-142">-Name</span></span>
<span data-ttu-id="0e6c4-143">Anger ett namn för det skyddade objektet för ASR-replikering.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="0e6c4-144">Namnet måste vara unikt inom valvet.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="0e6c4-145">-OS</span><span class="sxs-lookup"><span data-stu-id="0e6c4-145">-OS</span></span>
<span data-ttu-id="0e6c4-146">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-146">Specifies the operating system family.</span></span>
<span data-ttu-id="0e6c4-147">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="0e6c4-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="0e6c4-148">-OSDiskName</span></span>
<span data-ttu-id="0e6c4-149">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="0e6c4-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="0e6c4-150">-ProcessServer</span></span>
<span data-ttu-id="0e6c4-151">Den process server som ska användas för att replikera den här datorn.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="0e6c4-152">Använd listan med process servrar i ASR-Fabric som motsvarar konfigurations servern för att ange en.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-153">-ProtectableItem</span></span>
<span data-ttu-id="0e6c4-154">Anger objektet för skyddad ASR-objekt där replikering aktive ras.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0e6c4-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="0e6c4-156">Anger det mappnings objekt för ASR-skyddsagenten som motsvarar den replikeringsprincip som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="0e6c4-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="0e6c4-158">ID: t för AvailabilitySet som återställer datorn till i händelse av en redundans.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="0e6c4-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="0e6c4-160">ID för det virtuella Azure-nätverket som återställer datorn till i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="0e6c4-162">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="0e6c4-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="0e6c4-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="0e6c4-164">Under nätet i återställnings bara Azure Virtual Network som den misslyckade över virtuell dator ska kopplas till i händelse av redundans.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="0e6c4-166">Anger lagrings konto för startdiagnostik för återställning av Azure VM.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="0e6c4-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="0e6c4-168">Anger resurs-ID för återställnings moln tjänsten som ska redundansväxla den här virtuella datorn till.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="0e6c4-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="0e6c4-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="0e6c4-170">Anger ARM-identifieraren för den resurs grupp i vilken den virtuella datorn ska skapas i händelse av en failover.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="0e6c4-171">-RecoveryVmName</span></span>
<span data-ttu-id="0e6c4-172">Namn på den virtuella återställnings filen skapad efter redundans.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6c4-173">-ReplicationGroupName</span></span>
<span data-ttu-id="0e6c4-174">Anger namnet på den replikeringsgrupp som ska användas för att skapa enhetliga återställnings punkter med flera virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="0e6c4-175">Som standard skapas varje replikerat objekt i en grupp med egna och enhetliga återställnings punkter med flera virtuella datorer skapas inte.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="0e6c4-176">Använd bara det här alternativet om du behöver skapa enhetliga återställnings punkter med flera virtuella enheter i en grupp datorer genom att skydda alla datorer mot samma replikeringsgrupp.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6c4-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="0e6c4-177">-VmmToVmm</span></span>
<span data-ttu-id="0e6c4-178">Växla parameter för att ange att det replikerade objektet är en virtuell Hyper-V-dator som replikeras mellan VMM-hanterade Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="0e6c4-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="0e6c4-179">-VMwareToAzure</span></span>
<span data-ttu-id="0e6c4-180">Byt parameter för att ange att det replikerade objektet är en virtuell dator eller fysisk server som kommer att replikeras till Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="0e6c4-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0e6c4-181">-WaitForCompletion</span></span>
<span data-ttu-id="0e6c4-182">Anger att cmdleten ska vänta på att åtgärden slutförs innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="0e6c4-183">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e6c4-183">-Confirm</span></span>
<span data-ttu-id="0e6c4-184">Uppmaningar om att bekräfta innan operationen startas.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="0e6c4-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6c4-185">-WhatIf</span></span>
<span data-ttu-id="0e6c4-186">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6c4-187">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6c4-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6c4-188">CommonParameters</span></span>
<span data-ttu-id="0e6c4-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6c4-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6c4-190">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6c4-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6c4-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e6c4-191">INPUTS</span></span>

### <span data-ttu-id="0e6c4-192">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="0e6c4-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e6c4-193">OUTPUTS</span></span>

### <span data-ttu-id="0e6c4-194">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0e6c4-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e6c4-195">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e6c4-195">NOTES</span></span>

## <span data-ttu-id="0e6c4-196">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e6c4-196">RELATED LINKS</span></span>

[<span data-ttu-id="0e6c4-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="0e6c4-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="0e6c4-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0e6c4-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
