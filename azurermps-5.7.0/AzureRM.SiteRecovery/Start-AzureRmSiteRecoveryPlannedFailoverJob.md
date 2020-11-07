---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757185"
---
# <span data-ttu-id="852bb-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="852bb-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="852bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="852bb-102">SYNOPSIS</span></span>
<span data-ttu-id="852bb-103">Startar en planerad redundansväxling för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="852bb-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="852bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="852bb-104">SYNTAX</span></span>

### <span data-ttu-id="852bb-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="852bb-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="852bb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="852bb-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="852bb-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="852bb-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="852bb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="852bb-108">DESCRIPTION</span></span>
<span data-ttu-id="852bb-109">Cmdleten **Start-AzureRmSiteRecoveryPlannedFailoverJob** startar en planerad redundans för en entitet eller återställnings plan för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="852bb-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="852bb-110">Du kan kontrol lera om jobbet följer med Get-AzureRmSiteRecoveryJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="852bb-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="852bb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="852bb-111">EXAMPLES</span></span>

## <span data-ttu-id="852bb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="852bb-112">PARAMETERS</span></span>

### <span data-ttu-id="852bb-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="852bb-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="852bb-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="852bb-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="852bb-115">Ja</span><span class="sxs-lookup"><span data-stu-id="852bb-115">Yes</span></span>
- <span data-ttu-id="852bb-116">Nej</span><span class="sxs-lookup"><span data-stu-id="852bb-116">No</span></span>

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

### <span data-ttu-id="852bb-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="852bb-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="852bb-118">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="852bb-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="852bb-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="852bb-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="852bb-120">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="852bb-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="852bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852bb-121">-DefaultProfile</span></span>
<span data-ttu-id="852bb-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="852bb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="852bb-123">-Riktning</span><span class="sxs-lookup"><span data-stu-id="852bb-123">-Direction</span></span>
<span data-ttu-id="852bb-124">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="852bb-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="852bb-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="852bb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="852bb-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="852bb-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="852bb-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="852bb-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="852bb-128">-Optimera</span><span class="sxs-lookup"><span data-stu-id="852bb-128">-Optimize</span></span>
<span data-ttu-id="852bb-129">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="852bb-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="852bb-130">Den här parametern gäller när redundans görs från en Azure-webbplats till en lokal plats som kräver en omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="852bb-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="852bb-131">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="852bb-131">Valid values are:</span></span>

- <span data-ttu-id="852bb-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="852bb-132">ForDowntime</span></span>
- <span data-ttu-id="852bb-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="852bb-133">ForSynchronization</span></span>

<span data-ttu-id="852bb-134">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="852bb-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="852bb-135">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="852bb-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="852bb-136">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="852bb-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="852bb-137">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="852bb-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="852bb-138">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="852bb-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="852bb-139">Med den här inställningen aktive ras den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="852bb-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="852bb-140">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="852bb-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="852bb-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="852bb-141">-ProtectionEntity</span></span>
<span data-ttu-id="852bb-142">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="852bb-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="852bb-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="852bb-143">-RecoveryPlan</span></span>
<span data-ttu-id="852bb-144">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="852bb-144">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="852bb-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="852bb-145">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="852bb-146">-Server</span><span class="sxs-lookup"><span data-stu-id="852bb-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852bb-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="852bb-147">-ServicesProvider</span></span>
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

### <span data-ttu-id="852bb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852bb-148">CommonParameters</span></span>
<span data-ttu-id="852bb-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="852bb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852bb-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="852bb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852bb-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="852bb-151">INPUTS</span></span>

### <span data-ttu-id="852bb-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="852bb-152">ASRProtectionEntity</span></span>
<span data-ttu-id="852bb-153">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="852bb-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="852bb-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="852bb-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="852bb-155">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="852bb-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="852bb-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="852bb-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="852bb-157">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="852bb-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="852bb-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="852bb-158">OUTPUTS</span></span>

### <span data-ttu-id="852bb-159">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="852bb-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="852bb-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="852bb-160">NOTES</span></span>

## <span data-ttu-id="852bb-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="852bb-161">RELATED LINKS</span></span>

