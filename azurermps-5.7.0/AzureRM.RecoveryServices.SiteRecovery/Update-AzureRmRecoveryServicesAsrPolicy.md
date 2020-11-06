---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573336"
---
# <span data-ttu-id="c0359-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c0359-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="c0359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0359-102">SYNOPSIS</span></span>
<span data-ttu-id="c0359-103">Uppdaterar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c0359-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0359-104">SYNTAX</span></span>

### <span data-ttu-id="c0359-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c0359-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0359-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0359-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0359-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c0359-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0359-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0359-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c0359-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0359-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0359-111">DESCRIPTION</span></span>
<span data-ttu-id="c0359-112">Cmdleten **Update-AzureRmRecoveryServicesAsrPolicy** uppdaterar den angivna auktoriseringsprincipen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c0359-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="c0359-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0359-113">EXAMPLES</span></span>

### <span data-ttu-id="c0359-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0359-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="c0359-115">Startar åtgärden Uppdatera replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c0359-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="c0359-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0359-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="c0359-117">Startar uppdateringen av Azure-replikeringstjänsten för Azure med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c0359-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="c0359-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c0359-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="c0359-119">Startar uppdatering av Azure till Azure-replikeringsprincipen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c0359-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c0359-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0359-120">PARAMETERS</span></span>

### <span data-ttu-id="c0359-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="c0359-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="c0359-122">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="c0359-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-123">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="c0359-123">-Authentication</span></span>
<span data-ttu-id="c0359-124">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="c0359-124">Specifies the type of authentication used.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-125">-AzureToAzure</span></span>
<span data-ttu-id="c0359-126">Växla parameter som anger att den replikeringsprincip som används för att replikera Azure Virtual-datorer mellan två Azure-regioner kommer att uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c0359-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c0359-127">-AzureToVMware</span></span>
<span data-ttu-id="c0359-128">Switch parameter anger att specfied-principen används för att replikera misslyckade över virtuella datorer som körs i Azure tillbaka till en lokal VMware-webbplats.</span><span class="sxs-lookup"><span data-stu-id="c0359-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="c0359-129">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="c0359-129">-Compression</span></span>
<span data-ttu-id="c0359-130">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="c0359-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0359-131">-Confirm</span></span>
<span data-ttu-id="c0359-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0359-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0359-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0359-133">-DefaultProfile</span></span>
<span data-ttu-id="c0359-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0359-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c0359-135">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="c0359-135">-Encryption</span></span>
<span data-ttu-id="c0359-136">Anger om kryptering ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="c0359-136">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-137">-HyperVToAzure</span></span>
<span data-ttu-id="c0359-138">Switch parameter anger att specfied-principen används för att replikera Hyper-V-virtuella datorer till Azure.</span><span class="sxs-lookup"><span data-stu-id="c0359-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="c0359-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0359-139">-InputObject</span></span>
<span data-ttu-id="c0359-140">Indatavärdet för cmdleten: anger den auktoriseringsprincip för ASR som motsvarar den replikeringsprincip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c0359-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="c0359-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="c0359-142">Anger multiVm synkroniseringsstatus för principen.</span><span class="sxs-lookup"><span data-stu-id="c0359-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="c0359-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="c0359-144">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="c0359-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="c0359-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="c0359-146">Tröskelvärdet för återställnings tid i minuter att varna för.</span><span class="sxs-lookup"><span data-stu-id="c0359-146">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c0359-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c0359-148">Anger ID för Azure Storage-kontot för målobjektet.</span><span class="sxs-lookup"><span data-stu-id="c0359-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="c0359-149">Används som mål lagrings konto för replikering om ett alternativ inte tillhandahålls när du aktiverar replikering med New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0359-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-150">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="c0359-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="c0359-151">Tid i timmar för att behålla återställnings punkter när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="c0359-151">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-152">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="c0359-152">-ReplicaDeletion</span></span>
<span data-ttu-id="c0359-153">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="c0359-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="c0359-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="c0359-155">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="c0359-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="c0359-156">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="c0359-156">Valid values are:</span></span>

- <span data-ttu-id="c0359-157">halvtimme</span><span class="sxs-lookup"><span data-stu-id="c0359-157">30</span></span>
- <span data-ttu-id="c0359-158">300</span><span class="sxs-lookup"><span data-stu-id="c0359-158">300</span></span>
- <span data-ttu-id="c0359-159">900</span><span class="sxs-lookup"><span data-stu-id="c0359-159">900</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="c0359-160">-ReplicationMethod</span></span>
<span data-ttu-id="c0359-161">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="c0359-161">Specifies the replication method.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="c0359-162">-ReplicationPort</span></span>
<span data-ttu-id="c0359-163">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="c0359-163">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="c0359-164">-ReplicationStartTime</span></span>
<span data-ttu-id="c0359-165">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="c0359-165">Specifies the replication start time.</span></span>
<span data-ttu-id="c0359-166">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="c0359-166">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0359-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c0359-167">-VMwareToAzure</span></span>
<span data-ttu-id="c0359-168">Switch parameter anger att specfied-principen används för att replikera VMware Virtual Machines till Azure.</span><span class="sxs-lookup"><span data-stu-id="c0359-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="c0359-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="c0359-169">-VmmToVmm</span></span>
<span data-ttu-id="c0359-170">Switch parameter anger att specfied-principen används för att replikera VMM-hanterade Hyper-V-datorer mellan två Hyper-V-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="c0359-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="c0359-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0359-171">-WhatIf</span></span>
<span data-ttu-id="c0359-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0359-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0359-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0359-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0359-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0359-174">CommonParameters</span></span>
<span data-ttu-id="c0359-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0359-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0359-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0359-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0359-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0359-177">INPUTS</span></span>

### <span data-ttu-id="c0359-178">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="c0359-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="c0359-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0359-179">OUTPUTS</span></span>

### <span data-ttu-id="c0359-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="c0359-180">System.Object</span></span>

## <span data-ttu-id="c0359-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0359-181">NOTES</span></span>

## <span data-ttu-id="c0359-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0359-182">RELATED LINKS</span></span>
