---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574198"
---
# <span data-ttu-id="69f91-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="69f91-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="69f91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69f91-102">SYNOPSIS</span></span>
<span data-ttu-id="69f91-103">Startar en planerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="69f91-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69f91-104">SYNTAX</span></span>

### <span data-ttu-id="69f91-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="69f91-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69f91-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="69f91-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69f91-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69f91-107">DESCRIPTION</span></span>
<span data-ttu-id="69f91-108">Cmdleten **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** startar en planerad redundans för ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="69f91-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="69f91-109">Du kan kontrol lera om jobbet följer med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69f91-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="69f91-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69f91-110">EXAMPLES</span></span>

### <span data-ttu-id="69f91-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69f91-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="69f91-112">Startar den planerade redundansväxlingen för den angivna processen för ASR-återställning och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="69f91-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="69f91-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69f91-113">PARAMETERS</span></span>

### <span data-ttu-id="69f91-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69f91-114">-Confirm</span></span>
<span data-ttu-id="69f91-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69f91-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f91-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="69f91-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="69f91-117">Skapa den virtuella datorn om den inte finns och inte går att återställa till det primära området (används i en alternativ plats återställning.) De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="69f91-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69f91-118">Ja</span><span class="sxs-lookup"><span data-stu-id="69f91-118">Yes</span></span>
- <span data-ttu-id="69f91-119">Nej</span><span class="sxs-lookup"><span data-stu-id="69f91-119">No</span></span>

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

### <span data-ttu-id="69f91-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="69f91-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="69f91-121">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="69f91-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="69f91-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="69f91-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="69f91-123">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="69f91-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="69f91-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f91-124">-DefaultProfile</span></span>
<span data-ttu-id="69f91-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69f91-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="69f91-126">-Riktning</span><span class="sxs-lookup"><span data-stu-id="69f91-126">-Direction</span></span>
<span data-ttu-id="69f91-127">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="69f91-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="69f91-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="69f91-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69f91-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="69f91-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="69f91-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="69f91-130">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="69f91-131">-Optimera</span><span class="sxs-lookup"><span data-stu-id="69f91-131">-Optimize</span></span>
<span data-ttu-id="69f91-132">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="69f91-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="69f91-133">Den här parametern gäller när redundans görs från en Azure-webbplats till en lokal plats som kräver omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="69f91-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="69f91-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="69f91-134">Valid values are:</span></span>

- <span data-ttu-id="69f91-135">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="69f91-135">ForDowntime</span></span>
- <span data-ttu-id="69f91-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="69f91-136">ForSynchronization</span></span>

<span data-ttu-id="69f91-137">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="69f91-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="69f91-138">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="69f91-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="69f91-139">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="69f91-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="69f91-140">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="69f91-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="69f91-141">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="69f91-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="69f91-142">Med den här inställningen aktive ras den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="69f91-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="69f91-143">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="69f91-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="69f91-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69f91-144">-RecoveryPlan</span></span>
<span data-ttu-id="69f91-145">Anger det återställnings plan objekt för ASR som motsvarar återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="69f91-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="69f91-146">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69f91-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="69f91-147">Anger det skyddade objektet för ASR-replikering som motsvarar det replikerade objekt som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="69f91-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="69f91-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="69f91-148">-ServicesProvider</span></span>
<span data-ttu-id="69f91-149">Identifierar värden som du vill använda för att skapa den virtuella datorn när du går över till en annan plats genom att ange det kryptografiprovider för ASR-tjänsten som motsvarar den ASR-leverantör som körs på värden.</span><span class="sxs-lookup"><span data-stu-id="69f91-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="69f91-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f91-150">-WhatIf</span></span>
<span data-ttu-id="69f91-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69f91-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69f91-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69f91-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f91-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f91-153">CommonParameters</span></span>
<span data-ttu-id="69f91-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f91-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f91-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f91-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f91-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69f91-156">INPUTS</span></span>

### <span data-ttu-id="69f91-157">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69f91-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="69f91-158">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69f91-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="69f91-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69f91-159">OUTPUTS</span></span>

### <span data-ttu-id="69f91-160">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="69f91-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="69f91-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69f91-161">NOTES</span></span>

## <span data-ttu-id="69f91-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69f91-162">RELATED LINKS</span></span>
