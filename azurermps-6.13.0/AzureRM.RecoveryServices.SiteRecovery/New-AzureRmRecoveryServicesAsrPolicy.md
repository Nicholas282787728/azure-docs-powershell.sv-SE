---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572667"
---
# <span data-ttu-id="267e9-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="267e9-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="267e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="267e9-102">SYNOPSIS</span></span>
<span data-ttu-id="267e9-103">Skapar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="267e9-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="267e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="267e9-104">SYNTAX</span></span>

### <span data-ttu-id="267e9-105">HyperVToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="267e9-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="267e9-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="267e9-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="267e9-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="267e9-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="267e9-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="267e9-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="267e9-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="267e9-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="267e9-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="267e9-110">DESCRIPTION</span></span>
<span data-ttu-id="267e9-111">Cmdleten **New-AzureRmRecoveryServicesAsrPolicy** skapar en Azure Site Recovery Replication-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="267e9-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="267e9-112">Replikeringsprincipen används för att ange replikeringsinställningar som replikeringsfrekvens och antal återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="267e9-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="267e9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="267e9-113">EXAMPLES</span></span>

### <span data-ttu-id="267e9-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="267e9-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="267e9-115">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="267e9-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="267e9-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="267e9-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="267e9-117">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="267e9-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="267e9-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="267e9-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="267e9-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="267e9-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="267e9-120">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="267e9-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="267e9-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="267e9-121">PARAMETERS</span></span>

### <span data-ttu-id="267e9-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="267e9-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="267e9-123">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="267e9-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-124">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="267e9-124">-Authentication</span></span>
<span data-ttu-id="267e9-125">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="267e9-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="267e9-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="267e9-126">Valid values are:</span></span>

- <span data-ttu-id="267e9-127">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="267e9-127">Certificate</span></span>
-  <span data-ttu-id="267e9-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="267e9-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="267e9-129">-AzureToAzure</span></span>
<span data-ttu-id="267e9-130">Switch parameter som anger att den replikeringsprincip som skapas ska användas för replikerade Azure Virtual-datorer mellan två Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="267e9-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="267e9-131">-AzureToVMware</span></span>
<span data-ttu-id="267e9-132">Switch parameter som anger att den replikeringsprincip som skapas ska användas för att återföra replikeringen misslyckades via VMware Virtual Machines och fysiska servrar som körs i Azure tillbaka till en lokal VMware-webbplats.</span><span class="sxs-lookup"><span data-stu-id="267e9-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="267e9-133">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="267e9-133">-Compression</span></span>
<span data-ttu-id="267e9-134">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="267e9-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267e9-135">-DefaultProfile</span></span>
<span data-ttu-id="267e9-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="267e9-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="267e9-137">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="267e9-137">-Encryption</span></span>
<span data-ttu-id="267e9-138">{{Fill Encryption Description}}</span><span class="sxs-lookup"><span data-stu-id="267e9-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="267e9-139">-HyperVToAzure</span></span>
<span data-ttu-id="267e9-140">Växla parameter för att ange princip som ska användas för att replikera virtuella datorer med Hyper-V till Azure</span><span class="sxs-lookup"><span data-stu-id="267e9-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="267e9-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="267e9-142">Anger multiVm synkroniseringsstatus för principen.</span><span class="sxs-lookup"><span data-stu-id="267e9-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="267e9-143">-Name</span></span>
<span data-ttu-id="267e9-144">Anger namnet på auktoriseringsprincipen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="267e9-144">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="267e9-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="267e9-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="267e9-146">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="267e9-146">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="267e9-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="267e9-148">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="267e9-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="267e9-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="267e9-150">Behåll återställnings punkterna för angiven tid i timmar.</span><span class="sxs-lookup"><span data-stu-id="267e9-150">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="267e9-151">-ReplicaDeletion</span></span>
<span data-ttu-id="267e9-152">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="267e9-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="267e9-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="267e9-154">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="267e9-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="267e9-155">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="267e9-155">Valid values are:</span></span>

- <span data-ttu-id="267e9-156">halvtimme</span><span class="sxs-lookup"><span data-stu-id="267e9-156">30</span></span>
- <span data-ttu-id="267e9-157">300</span><span class="sxs-lookup"><span data-stu-id="267e9-157">300</span></span>
- <span data-ttu-id="267e9-158">900</span><span class="sxs-lookup"><span data-stu-id="267e9-158">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="267e9-159">-ReplicationMethod</span></span>
<span data-ttu-id="267e9-160">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="267e9-160">Specifies the replication method.</span></span>
<span data-ttu-id="267e9-161">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="267e9-161">Valid values are:</span></span>

- <span data-ttu-id="267e9-162">Support</span><span class="sxs-lookup"><span data-stu-id="267e9-162">Online</span></span>
- <span data-ttu-id="267e9-163">Arbetade</span><span class="sxs-lookup"><span data-stu-id="267e9-163">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="267e9-164">-ReplicationPort</span></span>
<span data-ttu-id="267e9-165">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="267e9-165">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-166">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="267e9-166">-ReplicationProvider</span></span>
<span data-ttu-id="267e9-167">Anger replikeringsprovidern för principen.</span><span class="sxs-lookup"><span data-stu-id="267e9-167">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="267e9-168">-ReplicationStartTime</span></span>
<span data-ttu-id="267e9-169">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="267e9-169">Specifies the replication start time.</span></span>
<span data-ttu-id="267e9-170">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="267e9-170">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="267e9-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="267e9-172">Tröskelvärdet för återställnings tid i minuter att varna för.</span><span class="sxs-lookup"><span data-stu-id="267e9-172">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e9-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="267e9-173">-VmmToVmm</span></span>
<span data-ttu-id="267e9-174">Växla parameter för att ange princip som ska användas för att replikera mellan Hyper-V-webbplatser som hanteras av en VMM-Server.</span><span class="sxs-lookup"><span data-stu-id="267e9-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="267e9-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="267e9-175">-VMwareToAzure</span></span>
<span data-ttu-id="267e9-176">Switch parameter som anger att den replikeringsprincip som skapas ska användas för att replikera VMware-virtuella datorer och/eller fysiska servrar till Azure.</span><span class="sxs-lookup"><span data-stu-id="267e9-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="267e9-177">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="267e9-177">-Confirm</span></span>
<span data-ttu-id="267e9-178">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="267e9-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="267e9-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="267e9-179">-WhatIf</span></span>
<span data-ttu-id="267e9-180">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="267e9-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="267e9-181">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="267e9-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="267e9-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267e9-182">CommonParameters</span></span>
<span data-ttu-id="267e9-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267e9-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267e9-184">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="267e9-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267e9-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="267e9-185">INPUTS</span></span>

### <span data-ttu-id="267e9-186">Ingen</span><span class="sxs-lookup"><span data-stu-id="267e9-186">None</span></span>

## <span data-ttu-id="267e9-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="267e9-187">OUTPUTS</span></span>

### <span data-ttu-id="267e9-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="267e9-188">System.Object</span></span>

## <span data-ttu-id="267e9-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="267e9-189">NOTES</span></span>

## <span data-ttu-id="267e9-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="267e9-190">RELATED LINKS</span></span>

[<span data-ttu-id="267e9-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="267e9-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="267e9-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="267e9-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
