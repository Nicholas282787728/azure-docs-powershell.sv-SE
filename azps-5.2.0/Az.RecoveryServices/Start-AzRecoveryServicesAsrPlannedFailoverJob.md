---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390162"
---
# <span data-ttu-id="59267-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="59267-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="59267-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59267-102">SYNOPSIS</span></span>
<span data-ttu-id="59267-103">Startar en planerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="59267-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="59267-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59267-104">SYNTAX</span></span>

### <span data-ttu-id="59267-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="59267-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59267-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="59267-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59267-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59267-107">DESCRIPTION</span></span>
<span data-ttu-id="59267-108">Cmdleten **Start-AzRecoveryServicesAsrPlannedFailoverJob** startar en planerad redundans för ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59267-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="59267-109">Du kan kontrol lera om jobbet följer med Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59267-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="59267-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59267-110">EXAMPLES</span></span>

### <span data-ttu-id="59267-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59267-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="59267-112">Startar den planerade redundansväxlingen för den angivna processen för ASR-återställning och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="59267-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="59267-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59267-113">PARAMETERS</span></span>

### <span data-ttu-id="59267-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="59267-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="59267-115">Skapa den virtuella datorn om den inte finns och inte går att återställa till det primära området (används i en alternativ plats återställning.) De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="59267-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59267-116">Ja</span><span class="sxs-lookup"><span data-stu-id="59267-116">Yes</span></span>
- <span data-ttu-id="59267-117">Nej</span><span class="sxs-lookup"><span data-stu-id="59267-117">No</span></span>

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

### <span data-ttu-id="59267-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="59267-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="59267-119">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="59267-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="59267-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="59267-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="59267-121">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="59267-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="59267-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59267-122">-DefaultProfile</span></span>
<span data-ttu-id="59267-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59267-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="59267-124">-Riktning</span><span class="sxs-lookup"><span data-stu-id="59267-124">-Direction</span></span>
<span data-ttu-id="59267-125">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="59267-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="59267-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="59267-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59267-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="59267-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="59267-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="59267-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="59267-129">-Optimera</span><span class="sxs-lookup"><span data-stu-id="59267-129">-Optimize</span></span>
<span data-ttu-id="59267-130">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="59267-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="59267-131">Den här parametern gäller när redundans görs från en Azure-webbplats till en lokal plats som kräver omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="59267-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="59267-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="59267-132">Valid values are:</span></span>

- <span data-ttu-id="59267-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="59267-133">ForDowntime</span></span>
- <span data-ttu-id="59267-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="59267-134">ForSynchronization</span></span>

<span data-ttu-id="59267-135">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="59267-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="59267-136">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="59267-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="59267-137">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="59267-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="59267-138">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="59267-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="59267-139">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="59267-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="59267-140">Med den här inställningen aktive ras den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="59267-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="59267-141">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="59267-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="59267-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="59267-142">-RecoveryPlan</span></span>
<span data-ttu-id="59267-143">Anger det återställnings plan objekt för ASR som motsvarar återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="59267-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59267-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="59267-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="59267-145">Anger det skyddade objektet för ASR-replikering som motsvarar det replikerade objekt som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="59267-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59267-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59267-146">-ServicesProvider</span></span>
<span data-ttu-id="59267-147">Identifierar värden som du vill använda för att skapa den virtuella datorn när du går över till en annan plats genom att ange det kryptografiprovider för ASR-tjänsten som motsvarar den ASR-leverantör som körs på värden.</span><span class="sxs-lookup"><span data-stu-id="59267-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59267-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59267-148">-Confirm</span></span>
<span data-ttu-id="59267-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59267-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59267-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59267-150">-WhatIf</span></span>
<span data-ttu-id="59267-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59267-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59267-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59267-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59267-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59267-153">CommonParameters</span></span>
<span data-ttu-id="59267-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59267-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59267-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59267-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59267-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59267-156">INPUTS</span></span>

### <span data-ttu-id="59267-157">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="59267-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="59267-158">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="59267-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="59267-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59267-159">OUTPUTS</span></span>

### <span data-ttu-id="59267-160">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="59267-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="59267-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59267-161">NOTES</span></span>

## <span data-ttu-id="59267-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59267-162">RELATED LINKS</span></span>
