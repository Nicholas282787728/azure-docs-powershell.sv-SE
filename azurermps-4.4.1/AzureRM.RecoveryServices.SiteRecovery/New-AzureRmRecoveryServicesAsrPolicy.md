---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575904"
---
# <span data-ttu-id="51935-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="51935-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="51935-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51935-102">SYNOPSIS</span></span>
<span data-ttu-id="51935-103">Skapar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="51935-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51935-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51935-104">SYNTAX</span></span>

### <span data-ttu-id="51935-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="51935-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51935-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="51935-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51935-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51935-107">DESCRIPTION</span></span>
<span data-ttu-id="51935-108">Cmdleten **New-AzureRmRecoveryServicesAsrPolicy** skapar en Azure Site Recovery Replication-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="51935-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="51935-109">Replikeringsprincipen används för att ange replikeringsinställningar som replikeringsfrekvens och antal återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="51935-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="51935-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51935-110">EXAMPLES</span></span>

### <span data-ttu-id="51935-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51935-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="51935-112">Startar åtgärden för att skapa en replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="51935-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="51935-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51935-113">PARAMETERS</span></span>

### <span data-ttu-id="51935-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="51935-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="51935-115">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="51935-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="51935-116">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="51935-116">-Authentication</span></span>
<span data-ttu-id="51935-117">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="51935-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="51935-118">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="51935-118">Valid values are:</span></span>

- <span data-ttu-id="51935-119">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="51935-119">Certificate</span></span>
-  <span data-ttu-id="51935-120">Kerberos</span><span class="sxs-lookup"><span data-stu-id="51935-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-121">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="51935-121">-Compression</span></span>
<span data-ttu-id="51935-122">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="51935-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-123">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="51935-123">-Encryption</span></span>
<span data-ttu-id="51935-124">Anger om kryptering ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="51935-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="51935-125">-Name</span></span>
<span data-ttu-id="51935-126">Anger namnet på auktoriseringsprincipen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="51935-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="51935-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="51935-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="51935-128">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="51935-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="51935-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="51935-130">Anger ID för Azure Storage-kontot för målobjektet.</span><span class="sxs-lookup"><span data-stu-id="51935-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="51935-131">Används som mål lagrings konto för replikering om ett alternativ inte tillhandahålls när du aktiverar replikering med New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51935-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="51935-132">-ReplicaDeletion</span></span>
<span data-ttu-id="51935-133">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="51935-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="51935-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="51935-135">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="51935-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="51935-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="51935-136">Valid values are:</span></span>

- <span data-ttu-id="51935-137">halvtimme</span><span class="sxs-lookup"><span data-stu-id="51935-137">30</span></span>
- <span data-ttu-id="51935-138">300</span><span class="sxs-lookup"><span data-stu-id="51935-138">300</span></span>
- <span data-ttu-id="51935-139">900</span><span class="sxs-lookup"><span data-stu-id="51935-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="51935-140">-ReplicationMethod</span></span>
<span data-ttu-id="51935-141">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="51935-141">Specifies the replication method.</span></span>
<span data-ttu-id="51935-142">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="51935-142">Valid values are:</span></span>

- <span data-ttu-id="51935-143">Support</span><span class="sxs-lookup"><span data-stu-id="51935-143">Online</span></span>
- <span data-ttu-id="51935-144">Arbetade</span><span class="sxs-lookup"><span data-stu-id="51935-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="51935-145">-ReplicationPort</span></span>
<span data-ttu-id="51935-146">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="51935-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="51935-147">-ReplicationProvider</span></span>
<span data-ttu-id="51935-148">Anger replikeringsprovidern.</span><span class="sxs-lookup"><span data-stu-id="51935-148">Specifies the replication provider.</span></span>
<span data-ttu-id="51935-149">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="51935-149">Valid values are:</span></span>

- <span data-ttu-id="51935-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="51935-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="51935-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="51935-151">HyperVReplica2012</span></span>
- <span data-ttu-id="51935-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="51935-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="51935-153">-ReplicationStartTime</span></span>
<span data-ttu-id="51935-154">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="51935-154">Specifies the replication start time.</span></span>
<span data-ttu-id="51935-155">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="51935-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51935-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51935-156">-Confirm</span></span>
<span data-ttu-id="51935-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51935-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51935-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51935-158">-WhatIf</span></span>
<span data-ttu-id="51935-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51935-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51935-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51935-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51935-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51935-161">CommonParameters</span></span>
<span data-ttu-id="51935-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51935-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51935-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51935-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51935-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51935-164">INPUTS</span></span>

### <span data-ttu-id="51935-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="51935-165">None</span></span>

## <span data-ttu-id="51935-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51935-166">OUTPUTS</span></span>

### <span data-ttu-id="51935-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="51935-167">System.Object</span></span>

## <span data-ttu-id="51935-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51935-168">NOTES</span></span>

## <span data-ttu-id="51935-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51935-169">RELATED LINKS</span></span>

[<span data-ttu-id="51935-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="51935-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="51935-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="51935-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
