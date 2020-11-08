---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099036"
---
# <span data-ttu-id="db913-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="db913-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="db913-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db913-102">SYNOPSIS</span></span>
<span data-ttu-id="db913-103">Startar den oplanerade redundansväxlingen för en entitet eller återställnings plan för återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="db913-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="db913-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db913-104">SYNTAX</span></span>

### <span data-ttu-id="db913-105">ByRPId (standard)</span><span class="sxs-lookup"><span data-stu-id="db913-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="db913-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="db913-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="db913-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="db913-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="db913-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="db913-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db913-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db913-109">DESCRIPTION</span></span>
<span data-ttu-id="db913-110">Cmdleten **Start-AzureSiteRecoveryUnplannedFailoverJob** startar den oplanerade redundansväxlingen av en Azure Site Recovery-enhet eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="db913-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="db913-111">Du kan kontrol lera om jobbet följer med cmdleten **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="db913-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="db913-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db913-112">EXAMPLES</span></span>

### <span data-ttu-id="db913-113">Exempel 1: starta ett oplanerat failover-jobb</span><span class="sxs-lookup"><span data-stu-id="db913-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="db913-114">Det första kommandot får en skyddad container med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar den sedan i $ProtectionContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="db913-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="db913-115">Det andra kommandot får de skyddade enheterna som tillhör den skyddade behållaren som lagras i $ProtectionContainer genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="db913-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="db913-116">Kommandot lagrar resultaten i variabeln $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="db913-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="db913-117">Det sista kommandot startar redundansväxlingen för skyddade enheter som lagras i $ProtectionEntity och anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="db913-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="db913-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db913-118">PARAMETERS</span></span>

### <span data-ttu-id="db913-119">-Riktning</span><span class="sxs-lookup"><span data-stu-id="db913-119">-Direction</span></span>
<span data-ttu-id="db913-120">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="db913-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="db913-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="db913-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db913-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="db913-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="db913-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="db913-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="db913-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="db913-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="db913-125">Visar att åtgärden kan utföras på käll sidans åtgärder.</span><span class="sxs-lookup"><span data-stu-id="db913-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="db913-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="db913-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="db913-127">Anger att käll webbplats åtgärder kan utföras.</span><span class="sxs-lookup"><span data-stu-id="db913-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db913-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="db913-128">-PrimaryAction</span></span>
<span data-ttu-id="db913-129">Anger att primära webbplats åtgärder krävs.</span><span class="sxs-lookup"><span data-stu-id="db913-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db913-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="db913-130">-Profile</span></span>
<span data-ttu-id="db913-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="db913-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db913-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="db913-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db913-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="db913-133">-ProtectionContainerId</span></span>
<span data-ttu-id="db913-134">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="db913-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="db913-135">Den här cmdleten startar jobbet för en skyddad virtuell dator som tillhör behållaren som den här cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="db913-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="db913-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="db913-136">-ProtectionEntity</span></span>
<span data-ttu-id="db913-137">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="db913-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="db913-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="db913-138">-ProtectionEntityId</span></span>
<span data-ttu-id="db913-139">Anger ID för en skyddad virtuell dator för vilken jobbet ska startas.</span><span class="sxs-lookup"><span data-stu-id="db913-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="db913-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db913-140">-RecoveryPlan</span></span>
<span data-ttu-id="db913-141">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="db913-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="db913-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="db913-142">-RPId</span></span>
<span data-ttu-id="db913-143">Anger ID för en återhämtnings plan som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="db913-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="db913-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="db913-144">-WaitForCompletion</span></span>
<span data-ttu-id="db913-145">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="db913-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="db913-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db913-146">CommonParameters</span></span>
<span data-ttu-id="db913-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db913-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db913-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db913-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db913-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db913-149">INPUTS</span></span>

## <span data-ttu-id="db913-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db913-150">OUTPUTS</span></span>

## <span data-ttu-id="db913-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db913-151">NOTES</span></span>

## <span data-ttu-id="db913-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db913-152">RELATED LINKS</span></span>

[<span data-ttu-id="db913-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="db913-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="db913-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="db913-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="db913-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="db913-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="db913-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="db913-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


