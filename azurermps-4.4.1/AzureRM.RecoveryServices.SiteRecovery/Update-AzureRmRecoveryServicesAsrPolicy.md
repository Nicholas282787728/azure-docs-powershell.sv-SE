---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582247"
---
# <span data-ttu-id="0e78d-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0e78d-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0e78d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e78d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e78d-103">Uppdaterar en Azure Site Recovery-replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="0e78d-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e78d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e78d-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e78d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e78d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e78d-106">Cmdleten **Update-AzureRmRecoveryServicesAsrPolicy** uppdaterar den angivna auktoriseringsprincipen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0e78d-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="0e78d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e78d-107">EXAMPLES</span></span>

### <span data-ttu-id="0e78d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e78d-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="0e78d-109">Startar åtgärden Uppdatera replikeringsprincip med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0e78d-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0e78d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e78d-110">PARAMETERS</span></span>

### <span data-ttu-id="0e78d-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="0e78d-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="0e78d-112">Anger frekvensen (i timmar) som du kan skapa program konsekventa återställnings punkter för.</span><span class="sxs-lookup"><span data-stu-id="0e78d-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="0e78d-113">-Inloggningsautentisering</span><span class="sxs-lookup"><span data-stu-id="0e78d-113">-Authentication</span></span>
<span data-ttu-id="0e78d-114">Anger vilken typ av verifikation som används.</span><span class="sxs-lookup"><span data-stu-id="0e78d-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="0e78d-115">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0e78d-115">Valid values are:</span></span>

- <span data-ttu-id="0e78d-116">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="0e78d-116">Certificate</span></span>
-  <span data-ttu-id="0e78d-117">Kerberos</span><span class="sxs-lookup"><span data-stu-id="0e78d-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-118">-Komprimering</span><span class="sxs-lookup"><span data-stu-id="0e78d-118">-Compression</span></span>
<span data-ttu-id="0e78d-119">Anger om komprimering ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="0e78d-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-120">-Kryptering</span><span class="sxs-lookup"><span data-stu-id="0e78d-120">-Encryption</span></span>
<span data-ttu-id="0e78d-121">Anger om kryptering ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="0e78d-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e78d-122">-InputObject</span></span>
<span data-ttu-id="0e78d-123">Indatavärdet för cmdleten: anger den auktoriseringsprincip för ASR som motsvarar den replikeringsprincip som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="0e78d-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="0e78d-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="0e78d-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="0e78d-125">Anger hur många återställnings punkter som ska behållas.</span><span class="sxs-lookup"><span data-stu-id="0e78d-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="0e78d-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e78d-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="0e78d-127">Anger ID för Azure Storage-kontot för målobjektet.</span><span class="sxs-lookup"><span data-stu-id="0e78d-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="0e78d-128">Används som mål lagrings konto för replikering om ett alternativ inte tillhandahålls när du aktiverar replikering med New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e78d-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="0e78d-129">-ReplicaDeletion</span></span>
<span data-ttu-id="0e78d-130">Anger om den virtuella replik datorn ska tas bort när du inaktiverar replikering från en hanterad VMM-plats till en annan.</span><span class="sxs-lookup"><span data-stu-id="0e78d-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="0e78d-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="0e78d-132">Anger frekvens intervallet för replikering i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0e78d-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="0e78d-133">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0e78d-133">Valid values are:</span></span>

- <span data-ttu-id="0e78d-134">halvtimme</span><span class="sxs-lookup"><span data-stu-id="0e78d-134">30</span></span>
- <span data-ttu-id="0e78d-135">300</span><span class="sxs-lookup"><span data-stu-id="0e78d-135">300</span></span>
- <span data-ttu-id="0e78d-136">900</span><span class="sxs-lookup"><span data-stu-id="0e78d-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="0e78d-137">-ReplicationMethod</span></span>
<span data-ttu-id="0e78d-138">Anger replikeringsfrekvensen.</span><span class="sxs-lookup"><span data-stu-id="0e78d-138">Specifies the replication method.</span></span>
<span data-ttu-id="0e78d-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0e78d-139">Valid values are:</span></span>

- <span data-ttu-id="0e78d-140">Support</span><span class="sxs-lookup"><span data-stu-id="0e78d-140">Online</span></span>
- <span data-ttu-id="0e78d-141">Arbetade</span><span class="sxs-lookup"><span data-stu-id="0e78d-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="0e78d-142">-ReplicationPort</span></span>
<span data-ttu-id="0e78d-143">Anger vilken port som används för replikering.</span><span class="sxs-lookup"><span data-stu-id="0e78d-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e78d-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="0e78d-144">-ReplicationStartTime</span></span>
<span data-ttu-id="0e78d-145">Anger start tiden för replikering.</span><span class="sxs-lookup"><span data-stu-id="0e78d-145">Specifies the replication start time.</span></span>
<span data-ttu-id="0e78d-146">Det får inte vara senare än 24 timmar från början av jobbet.</span><span class="sxs-lookup"><span data-stu-id="0e78d-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="0e78d-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e78d-147">-Confirm</span></span>
<span data-ttu-id="0e78d-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e78d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e78d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e78d-149">-WhatIf</span></span>
<span data-ttu-id="0e78d-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e78d-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e78d-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e78d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e78d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e78d-152">CommonParameters</span></span>
<span data-ttu-id="0e78d-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e78d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e78d-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e78d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e78d-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e78d-155">INPUTS</span></span>

### <span data-ttu-id="0e78d-156">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="0e78d-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="0e78d-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e78d-157">OUTPUTS</span></span>

### <span data-ttu-id="0e78d-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="0e78d-158">System.Object</span></span>

## <span data-ttu-id="0e78d-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e78d-159">NOTES</span></span>

## <span data-ttu-id="0e78d-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e78d-160">RELATED LINKS</span></span>

