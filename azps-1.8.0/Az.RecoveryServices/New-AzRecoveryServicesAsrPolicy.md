---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 98031226919b143431206fd9e3b512e6c653b8a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747391"
---
# <span data-ttu-id="a9ac5-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a9ac5-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="a9ac5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ac5-103">Skapar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="a9ac5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9ac5-104">SYNTAX</span></span>

### <span data-ttu-id="a9ac5-105">HyperVToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="a9ac5-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ac5-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9ac5-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a9ac5-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9ac5-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ac5-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a9ac5-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9ac5-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9ac5-110">DESCRIPTION</span></span>
<span data-ttu-id="a9ac5-111">Cmdleten **New-AzRecoveryServicesAsrPolicy** skapar en Azure Site Recovery Replication-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="a9ac5-112">Replikeringsprincipen används för att ange replikeringsinställningar som replikeringsfrekvens och antal återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="a9ac5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9ac5-113">EXAMPLES</span></span>

### <span data-ttu-id="a9ac5-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9ac5-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="a9ac5-115">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a9ac5-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a9ac5-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="a9ac5-117">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a9ac5-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a9ac5-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="a9ac5-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a9ac5-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="a9ac5-120">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a9ac5-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9ac5-121">PARAMETERS</span></span>

### <span data-ttu-id="a9ac5-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a9ac5-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a9ac5-123">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="a9ac5-124">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="a9ac5-124">-Authentication</span></span>
<span data-ttu-id="a9ac5-125">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="a9ac5-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a9ac5-126">Valid values are:</span></span>

- <span data-ttu-id="a9ac5-127">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="a9ac5-127">Certificate</span></span>
-  <span data-ttu-id="a9ac5-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="a9ac5-128">Kerberos</span></span>

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

### <span data-ttu-id="a9ac5-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-129">-AzureToAzure</span></span>
<span data-ttu-id="a9ac5-130">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="a9ac5-130">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="a9ac5-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a9ac5-131">-AzureToVMware</span></span>
<span data-ttu-id="a9ac5-132">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="a9ac5-132">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="a9ac5-133">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="a9ac5-133">-Compression</span></span>
<span data-ttu-id="a9ac5-134">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="a9ac5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ac5-135">-DefaultProfile</span></span>
<span data-ttu-id="a9ac5-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a9ac5-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-137">-HyperVToAzure</span></span>
<span data-ttu-id="a9ac5-138">Växla parameter för att ange princip som ska användas för att replikera virtuella datorer med Hyper-V till Azure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="a9ac5-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="a9ac5-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="a9ac5-140">Anger multiVm synkroniseringsstatus för principen.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="a9ac5-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9ac5-141">-Name</span></span>
<span data-ttu-id="a9ac5-142">Anger namnet på auktoriseringsprincipen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="a9ac5-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="a9ac5-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="a9ac5-144">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="a9ac5-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a9ac5-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a9ac5-146">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="a9ac5-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="a9ac5-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="a9ac5-148">Behåll återställnings punkterna för angiven tid i timmar.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="a9ac5-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="a9ac5-149">-ReplicaDeletion</span></span>
<span data-ttu-id="a9ac5-150">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="a9ac5-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a9ac5-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a9ac5-152">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="a9ac5-153">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a9ac5-153">Valid values are:</span></span>

- <span data-ttu-id="a9ac5-154">halvtimme</span><span class="sxs-lookup"><span data-stu-id="a9ac5-154">30</span></span>
- <span data-ttu-id="a9ac5-155">300</span><span class="sxs-lookup"><span data-stu-id="a9ac5-155">300</span></span>
- <span data-ttu-id="a9ac5-156">900</span><span class="sxs-lookup"><span data-stu-id="a9ac5-156">900</span></span>

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

### <span data-ttu-id="a9ac5-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a9ac5-157">-ReplicationMethod</span></span>
<span data-ttu-id="a9ac5-158">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-158">Specifies the replication method.</span></span>
<span data-ttu-id="a9ac5-159">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a9ac5-159">Valid values are:</span></span>

- <span data-ttu-id="a9ac5-160">Support</span><span class="sxs-lookup"><span data-stu-id="a9ac5-160">Online</span></span>
- <span data-ttu-id="a9ac5-161">Arbetade</span><span class="sxs-lookup"><span data-stu-id="a9ac5-161">Offline</span></span>

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

### <span data-ttu-id="a9ac5-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a9ac5-162">-ReplicationPort</span></span>
<span data-ttu-id="a9ac5-163">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="a9ac5-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="a9ac5-164">-ReplicationProvider</span></span>
<span data-ttu-id="a9ac5-165">Anger replikeringsprovidern för principen.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="a9ac5-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a9ac5-166">-ReplicationStartTime</span></span>
<span data-ttu-id="a9ac5-167">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-167">Specifies the replication start time.</span></span>
<span data-ttu-id="a9ac5-168">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="a9ac5-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="a9ac5-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="a9ac5-170">Tröskelvärdet för återställnings tid i minuter att varna för.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="a9ac5-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a9ac5-171">-VmmToVmm</span></span>
<span data-ttu-id="a9ac5-172">Växla parameter för att ange princip som ska användas för att replikera mellan Hyper-V-webbplatser som hanteras av en VMM-Server.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="a9ac5-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a9ac5-173">-VMwareToAzure</span></span>
<span data-ttu-id="a9ac5-174">Switch parameter som anger att den replikeringsprincip som skapas ska användas för att replikera VMware-virtuella datorer och/eller fysiska servrar till Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="a9ac5-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9ac5-175">-Confirm</span></span>
<span data-ttu-id="a9ac5-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ac5-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ac5-177">-WhatIf</span></span>
<span data-ttu-id="a9ac5-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9ac5-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ac5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ac5-180">CommonParameters</span></span>
<span data-ttu-id="a9ac5-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ac5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ac5-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ac5-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ac5-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9ac5-183">INPUTS</span></span>

### <span data-ttu-id="a9ac5-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9ac5-184">None</span></span>

## <span data-ttu-id="a9ac5-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9ac5-185">OUTPUTS</span></span>

### <span data-ttu-id="a9ac5-186">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a9ac5-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a9ac5-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9ac5-187">NOTES</span></span>

## <span data-ttu-id="a9ac5-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9ac5-188">RELATED LINKS</span></span>

[<span data-ttu-id="a9ac5-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a9ac5-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="a9ac5-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a9ac5-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
