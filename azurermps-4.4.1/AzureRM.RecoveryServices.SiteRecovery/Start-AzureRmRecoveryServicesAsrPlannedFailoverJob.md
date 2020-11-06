---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575888"
---
# <span data-ttu-id="1dab1-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1dab1-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="1dab1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dab1-102">SYNOPSIS</span></span>
<span data-ttu-id="1dab1-103">Startar en planerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="1dab1-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dab1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dab1-104">SYNTAX</span></span>

### <span data-ttu-id="1dab1-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1dab1-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dab1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1dab1-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dab1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dab1-107">DESCRIPTION</span></span>
<span data-ttu-id="1dab1-108">Cmdleten **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** startar en planerad redundans för ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1dab1-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1dab1-109">Du kan kontrol lera om jobbet följer med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dab1-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1dab1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dab1-110">EXAMPLES</span></span>

### <span data-ttu-id="1dab1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1dab1-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="1dab1-112">Startar den planerade redundansväxlingen för den angivna processen för ASR-återställning och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="1dab1-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1dab1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dab1-113">PARAMETERS</span></span>

### <span data-ttu-id="1dab1-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="1dab1-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="1dab1-115">Skapa den virtuella datorn om den inte finns och inte går att återställa till det primära området (används i en alternativ plats återställning.) De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1dab1-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dab1-116">Ja</span><span class="sxs-lookup"><span data-stu-id="1dab1-116">Yes</span></span>
- <span data-ttu-id="1dab1-117">Nej</span><span class="sxs-lookup"><span data-stu-id="1dab1-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dab1-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1dab1-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1dab1-119">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="1dab1-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1dab1-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1dab1-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1dab1-121">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="1dab1-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1dab1-122">-Riktning</span><span class="sxs-lookup"><span data-stu-id="1dab1-122">-Direction</span></span>
<span data-ttu-id="1dab1-123">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="1dab1-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="1dab1-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1dab1-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dab1-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1dab1-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="1dab1-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1dab1-126">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dab1-127">-Optimera</span><span class="sxs-lookup"><span data-stu-id="1dab1-127">-Optimize</span></span>
<span data-ttu-id="1dab1-128">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="1dab1-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="1dab1-129">Den här parametern gäller när redundans görs från en Azure-webbplats till en lokal plats som kräver en omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="1dab1-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="1dab1-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1dab1-130">Valid values are:</span></span>

- <span data-ttu-id="1dab1-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="1dab1-131">ForDowntime</span></span>
- <span data-ttu-id="1dab1-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="1dab1-132">ForSynchronization</span></span>

<span data-ttu-id="1dab1-133">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="1dab1-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="1dab1-134">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1dab1-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="1dab1-135">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="1dab1-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="1dab1-136">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1dab1-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="1dab1-137">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="1dab1-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="1dab1-138">Med den här inställningen aktive ras den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="1dab1-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="1dab1-139">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="1dab1-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dab1-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1dab1-140">-RecoveryPlan</span></span>
<span data-ttu-id="1dab1-141">Anger det återställnings plan objekt för ASR som motsvarar återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="1dab1-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="1dab1-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1dab1-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1dab1-143">Anger det skyddade objektet för ASR-replikering som motsvarar det replikerade objekt som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="1dab1-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dab1-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1dab1-144">-ServicesProvider</span></span>
<span data-ttu-id="1dab1-145">Identifierar värden som du vill använda för att skapa den virtuella datorn när du går över till en annan plats genom att ange det kryptografiprovider för ASR-tjänsten som motsvarar den ASR-leverantör som körs på värden.</span><span class="sxs-lookup"><span data-stu-id="1dab1-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dab1-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dab1-146">-Confirm</span></span>
<span data-ttu-id="1dab1-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dab1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dab1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dab1-148">-WhatIf</span></span>
<span data-ttu-id="1dab1-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dab1-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dab1-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dab1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dab1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dab1-151">CommonParameters</span></span>
<span data-ttu-id="1dab1-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dab1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dab1-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dab1-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dab1-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dab1-154">INPUTS</span></span>

### <span data-ttu-id="1dab1-155">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1dab1-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="1dab1-156">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1dab1-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1dab1-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dab1-157">OUTPUTS</span></span>

### <span data-ttu-id="1dab1-158">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1dab1-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1dab1-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dab1-159">NOTES</span></span>

## <span data-ttu-id="1dab1-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dab1-160">RELATED LINKS</span></span>

