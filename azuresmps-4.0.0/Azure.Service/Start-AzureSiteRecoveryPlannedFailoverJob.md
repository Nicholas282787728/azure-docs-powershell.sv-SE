---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093477"
---
# <span data-ttu-id="52b28-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="52b28-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="52b28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52b28-102">SYNOPSIS</span></span>
<span data-ttu-id="52b28-103">Startar en planerad redundansväxling för en webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="52b28-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="52b28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52b28-104">SYNTAX</span></span>

### <span data-ttu-id="52b28-105">ByRPId (standard)</span><span class="sxs-lookup"><span data-stu-id="52b28-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52b28-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="52b28-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52b28-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="52b28-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52b28-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="52b28-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52b28-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52b28-109">DESCRIPTION</span></span>
<span data-ttu-id="52b28-110">Cmdleten **Start-AzureSiteRecoveryPlannedFailoverJob** startar en planerad redundans för en entitet eller återställnings plan för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="52b28-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="52b28-111">Du kan kontrol lera om jobbet följer med cmdleten **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="52b28-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="52b28-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52b28-112">EXAMPLES</span></span>

### <span data-ttu-id="52b28-113">Exempel 1: starta ett planerat redundans jobb</span><span class="sxs-lookup"><span data-stu-id="52b28-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="52b28-114">Det första kommandot får alla skyddade behållare i det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan resultatet i variabeln $container.</span><span class="sxs-lookup"><span data-stu-id="52b28-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="52b28-115">I det här exemplet finns det en enda behållare.</span><span class="sxs-lookup"><span data-stu-id="52b28-115">In this example, there is a single container.</span></span>

<span data-ttu-id="52b28-116">Det andra kommandot hämtar de skyddade virtuella datorerna som tillhör behållaren som lagras i $Container genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="52b28-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="52b28-117">Kommandot lagrar resultaten i variabeln $Protected.</span><span class="sxs-lookup"><span data-stu-id="52b28-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="52b28-118">Med kommandot sista startas jobbet redundans i riktningen PrimaryToRecovery för de skyddade virtuella datorerna i $Protected.</span><span class="sxs-lookup"><span data-stu-id="52b28-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="52b28-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52b28-119">PARAMETERS</span></span>

### <span data-ttu-id="52b28-120">-Riktning</span><span class="sxs-lookup"><span data-stu-id="52b28-120">-Direction</span></span>
<span data-ttu-id="52b28-121">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="52b28-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="52b28-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="52b28-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52b28-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="52b28-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="52b28-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="52b28-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="52b28-125">-Optimera</span><span class="sxs-lookup"><span data-stu-id="52b28-125">-Optimize</span></span>
<span data-ttu-id="52b28-126">Ange vad du vill optimera för.</span><span class="sxs-lookup"><span data-stu-id="52b28-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="52b28-127">Den här parametern gäller för redundans från en Azure-webbplats till en lokal plats som kräver en omfattande datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="52b28-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="52b28-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="52b28-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52b28-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="52b28-129">ForDowntime</span></span>
- <span data-ttu-id="52b28-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="52b28-130">ForSynchronization</span></span>

<span data-ttu-id="52b28-131">När **ForDowntime** anges visar detta att data är synkroniserade innan redundans för att minimera nertid.</span><span class="sxs-lookup"><span data-stu-id="52b28-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="52b28-132">Synkroniseringen utförs utan att stänga av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="52b28-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="52b28-133">När synkroniseringen är klar är jobbet inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="52b28-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="52b28-134">Återuppta jobbet för att utföra ytterligare en synkronisering som stänger av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="52b28-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="52b28-135">När **ForSynchronization** anges visar detta att data synkroniseras endast under redundans så att datasynkroniseringen är minimerad.</span><span class="sxs-lookup"><span data-stu-id="52b28-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="52b28-136">Eftersom den här inställningen är aktive rad avslutas den virtuella datorn omedelbart.</span><span class="sxs-lookup"><span data-stu-id="52b28-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="52b28-137">Synkroniseringen startar efter avstängning för att slutföra redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="52b28-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="52b28-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="52b28-138">-Profile</span></span>
<span data-ttu-id="52b28-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="52b28-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52b28-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="52b28-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b28-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="52b28-141">-ProtectionContainerId</span></span>
<span data-ttu-id="52b28-142">Anger ID: t för den skyddade behållare som jobbet ska startas för.</span><span class="sxs-lookup"><span data-stu-id="52b28-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b28-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="52b28-143">-ProtectionEntity</span></span>
<span data-ttu-id="52b28-144">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="52b28-144">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="52b28-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="52b28-145">-ProtectionEntityId</span></span>
<span data-ttu-id="52b28-146">Anger ett **ASRProtectionEntity** -objekt som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="52b28-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="52b28-147">För att få ett **ASRProtectionEntity** -objekt, Använd cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="52b28-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b28-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="52b28-148">-RecoveryPlan</span></span>
<span data-ttu-id="52b28-149">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="52b28-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="52b28-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="52b28-150">-RPId</span></span>
<span data-ttu-id="52b28-151">Anger ID för en återhämtnings plan som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="52b28-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b28-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="52b28-152">-WaitForCompletion</span></span>
<span data-ttu-id="52b28-153">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="52b28-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b28-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b28-154">CommonParameters</span></span>
<span data-ttu-id="52b28-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b28-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b28-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b28-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b28-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52b28-157">INPUTS</span></span>

## <span data-ttu-id="52b28-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52b28-158">OUTPUTS</span></span>

## <span data-ttu-id="52b28-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52b28-159">NOTES</span></span>

## <span data-ttu-id="52b28-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52b28-160">RELATED LINKS</span></span>

[<span data-ttu-id="52b28-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="52b28-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="52b28-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="52b28-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


