---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577411"
---
# <span data-ttu-id="22ef3-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="22ef3-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="22ef3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="22ef3-103">Startar en planerad redundansväxling för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="22ef3-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22ef3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22ef3-104">SYNTAX</span></span>

### <span data-ttu-id="22ef3-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="22ef3-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22ef3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="22ef3-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22ef3-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="22ef3-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ef3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22ef3-108">DESCRIPTION</span></span>
<span data-ttu-id="22ef3-109">Cmdleten **Start-AzureRmSiteRecoveryPlannedFailoverJob** startar en planerad redundans för en entitet eller återställnings plan för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="22ef3-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="22ef3-110">Du kan kontrol lera om jobbet följer med Get-AzureRmSiteRecoveryJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22ef3-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="22ef3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22ef3-111">EXAMPLES</span></span>

## <span data-ttu-id="22ef3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22ef3-112">PARAMETERS</span></span>

### <span data-ttu-id="22ef3-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="22ef3-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="22ef3-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="22ef3-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22ef3-115">Ja</span><span class="sxs-lookup"><span data-stu-id="22ef3-115">Yes</span></span>
- <span data-ttu-id="22ef3-116">Nej</span><span class="sxs-lookup"><span data-stu-id="22ef3-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="22ef3-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="22ef3-118">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="22ef3-118">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="22ef3-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="22ef3-120">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="22ef3-120">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-121">-Riktning</span><span class="sxs-lookup"><span data-stu-id="22ef3-121">-Direction</span></span>
<span data-ttu-id="22ef3-122">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="22ef3-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="22ef3-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="22ef3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22ef3-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="22ef3-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="22ef3-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="22ef3-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-126">-Optimera</span><span class="sxs-lookup"><span data-stu-id="22ef3-126">-Optimize</span></span>
<span data-ttu-id="22ef3-127">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="22ef3-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="22ef3-128">Den här parametern gäller när redundans görs från en Azure-webbplats till en lokal plats som kräver en omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="22ef3-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="22ef3-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="22ef3-129">Valid values are:</span></span>

- <span data-ttu-id="22ef3-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="22ef3-130">ForDowntime</span></span>
- <span data-ttu-id="22ef3-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="22ef3-131">ForSynchronization</span></span>

<span data-ttu-id="22ef3-132">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="22ef3-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="22ef3-133">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="22ef3-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="22ef3-134">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="22ef3-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="22ef3-135">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="22ef3-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="22ef3-136">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="22ef3-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="22ef3-137">Med den här inställningen aktive ras den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="22ef3-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="22ef3-138">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="22ef3-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="22ef3-139">-ProtectionEntity</span></span>
<span data-ttu-id="22ef3-140">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="22ef3-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22ef3-141">-RecoveryPlan</span></span>
<span data-ttu-id="22ef3-142">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="22ef3-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22ef3-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-144">-Server</span><span class="sxs-lookup"><span data-stu-id="22ef3-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="22ef3-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ef3-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ef3-146">-DefaultProfile</span></span>
<span data-ttu-id="22ef3-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22ef3-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ef3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ef3-148">CommonParameters</span></span>
<span data-ttu-id="22ef3-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ef3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ef3-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ef3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ef3-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22ef3-151">INPUTS</span></span>

### <span data-ttu-id="22ef3-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="22ef3-152">ASRProtectionEntity</span></span>
<span data-ttu-id="22ef3-153">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="22ef3-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="22ef3-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22ef3-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="22ef3-155">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="22ef3-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="22ef3-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22ef3-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="22ef3-157">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="22ef3-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="22ef3-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22ef3-158">OUTPUTS</span></span>

### <span data-ttu-id="22ef3-159">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="22ef3-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22ef3-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22ef3-160">NOTES</span></span>

## <span data-ttu-id="22ef3-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22ef3-161">RELATED LINKS</span></span>

