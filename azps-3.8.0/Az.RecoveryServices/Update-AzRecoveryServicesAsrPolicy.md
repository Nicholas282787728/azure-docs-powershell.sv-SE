---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088534"
---
# <span data-ttu-id="30a29-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="30a29-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="30a29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30a29-102">SYNOPSIS</span></span>
<span data-ttu-id="30a29-103">Uppdaterar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="30a29-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="30a29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30a29-104">SYNTAX</span></span>

### <span data-ttu-id="30a29-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="30a29-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30a29-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a29-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30a29-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="30a29-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a29-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30a29-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="30a29-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a29-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30a29-111">DESCRIPTION</span></span>
<span data-ttu-id="30a29-112">Cmdleten **Update-AzRecoveryServicesAsrPolicy** uppdaterar den angivna auktoriseringsprincipen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30a29-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="30a29-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30a29-113">EXAMPLES</span></span>

### <span data-ttu-id="30a29-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30a29-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="30a29-115">Startar åtgärden Uppdatera replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="30a29-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="30a29-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30a29-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="30a29-117">Startar uppdateringen av Azure-replikeringstjänsten för Azure med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="30a29-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="30a29-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="30a29-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="30a29-119">Startar uppdatering av Azure till Azure-replikeringsprincipen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="30a29-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="30a29-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30a29-120">PARAMETERS</span></span>

### <span data-ttu-id="30a29-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="30a29-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="30a29-122">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="30a29-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="30a29-123">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="30a29-123">-Authentication</span></span>
<span data-ttu-id="30a29-124">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="30a29-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-125">-AzureToAzure</span></span>
<span data-ttu-id="30a29-126">Anger återställning av Azure till Azure-katastrofen.</span><span class="sxs-lookup"><span data-stu-id="30a29-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="30a29-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="30a29-127">-AzureToVMware</span></span>
<span data-ttu-id="30a29-128">Anger katastrof återställning för Azure till vMWare.</span><span class="sxs-lookup"><span data-stu-id="30a29-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="30a29-129">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="30a29-129">-Compression</span></span>
<span data-ttu-id="30a29-130">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="30a29-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a29-131">-DefaultProfile</span></span>
<span data-ttu-id="30a29-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30a29-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="30a29-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-133">-HyperVToAzure</span></span>
<span data-ttu-id="30a29-134">Byt parameter indikerar att den angivna principen används för att replikera Hyper-V-virtuella datorer till Azure.</span><span class="sxs-lookup"><span data-stu-id="30a29-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="30a29-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a29-135">-InputObject</span></span>
<span data-ttu-id="30a29-136">Indatavärdet för cmdleten: anger den auktoriseringsprincip för ASR som motsvarar den replikeringsprincip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="30a29-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="30a29-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="30a29-138">Anger multiVm synkroniseringsstatus för principen.</span><span class="sxs-lookup"><span data-stu-id="30a29-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="30a29-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="30a29-140">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="30a29-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30a29-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="30a29-142">Anger ID för Azure Storage-kontot för målobjektet.</span><span class="sxs-lookup"><span data-stu-id="30a29-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="30a29-143">Används som mål lagrings konto för replikering om ett alternativ inte tillhandahålls när du aktiverar replikering med New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a29-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="30a29-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="30a29-145">Tid i timmar för att behålla återställnings punkter när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="30a29-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="30a29-146">-ReplicaDeletion</span></span>
<span data-ttu-id="30a29-147">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="30a29-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="30a29-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="30a29-149">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="30a29-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="30a29-150">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="30a29-150">Valid values are:</span></span>

- <span data-ttu-id="30a29-151">halvtimme</span><span class="sxs-lookup"><span data-stu-id="30a29-151">30</span></span>
- <span data-ttu-id="30a29-152">300</span><span class="sxs-lookup"><span data-stu-id="30a29-152">300</span></span>
- <span data-ttu-id="30a29-153">900</span><span class="sxs-lookup"><span data-stu-id="30a29-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="30a29-154">-ReplicationMethod</span></span>
<span data-ttu-id="30a29-155">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="30a29-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="30a29-156">-ReplicationPort</span></span>
<span data-ttu-id="30a29-157">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="30a29-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="30a29-158">-ReplicationStartTime</span></span>
<span data-ttu-id="30a29-159">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="30a29-159">Specifies the replication start time.</span></span>
<span data-ttu-id="30a29-160">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="30a29-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="30a29-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="30a29-162">Tröskelvärdet för återställnings tid i minuter att varna för.</span><span class="sxs-lookup"><span data-stu-id="30a29-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30a29-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="30a29-163">-VmmToVmm</span></span>
<span data-ttu-id="30a29-164">Switch parameter anger att den angivna principen används för att replikera VMM-hanterade Hyper-V-datorer mellan två Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="30a29-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="30a29-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="30a29-165">-VMwareToAzure</span></span>
<span data-ttu-id="30a29-166">Byt parameter indikerar att den angivna principen används för att replikera VMware-virtuella datorer till Azure.</span><span class="sxs-lookup"><span data-stu-id="30a29-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="30a29-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30a29-167">-Confirm</span></span>
<span data-ttu-id="30a29-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30a29-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a29-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a29-169">-WhatIf</span></span>
<span data-ttu-id="30a29-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30a29-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30a29-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30a29-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a29-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a29-172">CommonParameters</span></span>
<span data-ttu-id="30a29-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a29-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a29-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a29-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a29-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30a29-175">INPUTS</span></span>

### <span data-ttu-id="30a29-176">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="30a29-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="30a29-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30a29-177">OUTPUTS</span></span>

### <span data-ttu-id="30a29-178">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="30a29-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30a29-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30a29-179">NOTES</span></span>

## <span data-ttu-id="30a29-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30a29-180">RELATED LINKS</span></span>