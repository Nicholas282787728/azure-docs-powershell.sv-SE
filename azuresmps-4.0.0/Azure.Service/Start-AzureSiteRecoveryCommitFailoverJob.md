---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099008"
---
# <span data-ttu-id="25285-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="25285-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="25285-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25285-102">SYNOPSIS</span></span>
<span data-ttu-id="25285-103">Startar åtgärden redundans för ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="25285-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="25285-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25285-104">SYNTAX</span></span>

### <span data-ttu-id="25285-105">ByRPId (standard)</span><span class="sxs-lookup"><span data-stu-id="25285-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25285-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="25285-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25285-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="25285-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25285-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="25285-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25285-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25285-109">DESCRIPTION</span></span>
<span data-ttu-id="25285-110">Cmdleten **Start-AzureSiteRecoveryCommitFailoverJob** startar redundansväxlingen för ett Azure Site Recovery-objekt efter en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="25285-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="25285-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25285-111">EXAMPLES</span></span>

### <span data-ttu-id="25285-112">Exempel 1: påbörja jobbet genomföra redundans</span><span class="sxs-lookup"><span data-stu-id="25285-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="25285-113">Det första kommandot får alla skyddade behållare för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan resultatet i variabeln $container.</span><span class="sxs-lookup"><span data-stu-id="25285-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="25285-114">Det andra kommandot hämtar de skyddade virtuella datorerna som tillhör behållaren som lagras i $Container genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="25285-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="25285-115">Kommandot lagrar resultaten i variabeln $Protected.</span><span class="sxs-lookup"><span data-stu-id="25285-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="25285-116">Med kommandot sista startas jobbet redundans för de skyddade objekten i $Protected.</span><span class="sxs-lookup"><span data-stu-id="25285-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="25285-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25285-117">PARAMETERS</span></span>

### <span data-ttu-id="25285-118">-Riktning</span><span class="sxs-lookup"><span data-stu-id="25285-118">-Direction</span></span>
<span data-ttu-id="25285-119">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="25285-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="25285-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25285-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25285-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="25285-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="25285-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="25285-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="25285-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="25285-123">-Profile</span></span>
<span data-ttu-id="25285-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="25285-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25285-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="25285-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25285-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="25285-126">-ProtectionContainerId</span></span>
<span data-ttu-id="25285-127">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="25285-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="25285-128">Den här cmdleten startar jobbet för en skyddad virtuell dator som tillhör behållaren som den här cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="25285-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="25285-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25285-129">-ProtectionEntity</span></span>
<span data-ttu-id="25285-130">Anger ett **ASRProtectionEntity** -objekt som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="25285-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="25285-131">För att få ett **ASRProtectionEntity** -objekt, Använd cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="25285-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="25285-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="25285-132">-ProtectionEntityId</span></span>
<span data-ttu-id="25285-133">Anger ID för en skyddad virtuell dator för vilken jobbet ska startas.</span><span class="sxs-lookup"><span data-stu-id="25285-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="25285-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25285-134">-RecoveryPlan</span></span>
<span data-ttu-id="25285-135">Anger ett återställnings plan objekt som jobbet ska startas för.</span><span class="sxs-lookup"><span data-stu-id="25285-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="25285-136">För att få ett **ASRRecoveryPlan** -objekt, Använd cmdleten **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="25285-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="25285-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="25285-137">-RPId</span></span>
<span data-ttu-id="25285-138">Anger ID för en återhämtnings plan som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="25285-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="25285-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="25285-139">-WaitForCompletion</span></span>
<span data-ttu-id="25285-140">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="25285-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="25285-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25285-141">CommonParameters</span></span>
<span data-ttu-id="25285-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25285-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25285-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25285-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25285-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25285-144">INPUTS</span></span>

## <span data-ttu-id="25285-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25285-145">OUTPUTS</span></span>

## <span data-ttu-id="25285-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25285-146">NOTES</span></span>

## <span data-ttu-id="25285-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25285-147">RELATED LINKS</span></span>

[<span data-ttu-id="25285-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25285-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="25285-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="25285-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="25285-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25285-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


