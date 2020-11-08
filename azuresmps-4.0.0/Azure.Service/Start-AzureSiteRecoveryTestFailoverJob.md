---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099258"
---
# <span data-ttu-id="13ad7-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="13ad7-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="13ad7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="13ad7-103">Startar en redundanstest för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="13ad7-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="13ad7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13ad7-104">SYNTAX</span></span>

### <span data-ttu-id="13ad7-105">ByPEId (standard)</span><span class="sxs-lookup"><span data-stu-id="13ad7-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="13ad7-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="13ad7-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="13ad7-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="13ad7-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="13ad7-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="13ad7-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad7-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="13ad7-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13ad7-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="13ad7-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ad7-121">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13ad7-121">DESCRIPTION</span></span>
<span data-ttu-id="13ad7-122">Cmdleten **Start-AzureSiteRecoveryTestFailoverJob** startar redundanstestning för en Azure Site Recovery-enhet eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="13ad7-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="13ad7-123">Du kan kontrol lera om jobbet lyckades med cmdleten **Get-AzureRMSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="13ad7-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="13ad7-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13ad7-124">EXAMPLES</span></span>

### <span data-ttu-id="13ad7-125">Exempel 1: starta en redundanstest</span><span class="sxs-lookup"><span data-stu-id="13ad7-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="13ad7-126">Det första kommandot använder cmdleten **Get-AzureSiteRecoveryProtectionContainer** för att hämta en skyddad container och lagrar den sedan i $ProtectionContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="13ad7-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="13ad7-127">Det andra kommandot får de skyddade enheterna som tillhör den skyddade behållaren som lagras i $ProtectionContainer genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="13ad7-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="13ad7-128">Kommandot lagrar resultaten i variabeln $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="13ad7-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="13ad7-129">Det sista kommandot startar redundanstestning för de skyddade enheterna som lagras i $ProtectionEntity och anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="13ad7-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="13ad7-130">Exempel 2: starta en redundanstestning med en återställnings plan</span><span class="sxs-lookup"><span data-stu-id="13ad7-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="13ad7-131">Det här kommandot får återställnings planen med namnet RecoveryPlan01 för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="13ad7-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="13ad7-132">Kommandot lagrar planen i $RecoveryPlan variabel.</span><span class="sxs-lookup"><span data-stu-id="13ad7-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="13ad7-133">Det andra kommandot startar redundanstestning för att återställnings planen är lagrad i $RecoveryPlan och anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="13ad7-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="13ad7-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13ad7-134">PARAMETERS</span></span>

### <span data-ttu-id="13ad7-135">-Riktning</span><span class="sxs-lookup"><span data-stu-id="13ad7-135">-Direction</span></span>
<span data-ttu-id="13ad7-136">Anger växlings riktning.</span><span class="sxs-lookup"><span data-stu-id="13ad7-136">Specifies the failover direction.</span></span>
<span data-ttu-id="13ad7-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="13ad7-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13ad7-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="13ad7-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="13ad7-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="13ad7-139">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="13ad7-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="13ad7-140">-LogicalNetworkId</span></span>
<span data-ttu-id="13ad7-141">Anger det logiska nätverkets ID.</span><span class="sxs-lookup"><span data-stu-id="13ad7-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-142">-Network</span><span class="sxs-lookup"><span data-stu-id="13ad7-142">-Network</span></span>
<span data-ttu-id="13ad7-143">Anger det nätverks objekt som ska användas för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="13ad7-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="13ad7-144">Använd cmdleten **Get-AzureSiteRecoveryNetwork** för att få ett nätverk.</span><span class="sxs-lookup"><span data-stu-id="13ad7-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="13ad7-145">-NetworkType</span></span>
<span data-ttu-id="13ad7-146">Anger vilken nätverks typ som ska användas för testning av redundans.</span><span class="sxs-lookup"><span data-stu-id="13ad7-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="13ad7-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="13ad7-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13ad7-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="13ad7-148">None</span></span>
- <span data-ttu-id="13ad7-149">Nya</span><span class="sxs-lookup"><span data-stu-id="13ad7-149">New</span></span>
- <span data-ttu-id="13ad7-150">Existerande</span><span class="sxs-lookup"><span data-stu-id="13ad7-150">Existing</span></span>

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

### <span data-ttu-id="13ad7-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="13ad7-151">-Profile</span></span>
<span data-ttu-id="13ad7-152">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="13ad7-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13ad7-153">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="13ad7-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13ad7-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="13ad7-154">-ProtectionContainerId</span></span>
<span data-ttu-id="13ad7-155">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="13ad7-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="13ad7-156">Den här cmdleten startar jobbet för en skyddad virtuell dator som tillhör behållaren som den här cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="13ad7-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="13ad7-157">-ProtectionEntity</span></span>
<span data-ttu-id="13ad7-158">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="13ad7-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="13ad7-159">-ProtectionEntityId</span></span>
<span data-ttu-id="13ad7-160">Anger ID för en skyddad virtuell dator för vilken jobbet ska startas.</span><span class="sxs-lookup"><span data-stu-id="13ad7-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13ad7-161">-RecoveryPlan</span></span>
<span data-ttu-id="13ad7-162">Anger en återställnings plan för vilken jobbet ska startas.</span><span class="sxs-lookup"><span data-stu-id="13ad7-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="13ad7-163">-RpId</span></span>
<span data-ttu-id="13ad7-164">Anger ID för en återhämtnings plan som jobbet ska startas med.</span><span class="sxs-lookup"><span data-stu-id="13ad7-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="13ad7-165">-VmNetworkId</span></span>
<span data-ttu-id="13ad7-166">Anger ID för den virtuella datorns nätverk.</span><span class="sxs-lookup"><span data-stu-id="13ad7-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ad7-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="13ad7-167">-WaitForCompletion</span></span>
<span data-ttu-id="13ad7-168">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="13ad7-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="13ad7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ad7-169">CommonParameters</span></span>
<span data-ttu-id="13ad7-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ad7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ad7-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ad7-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ad7-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13ad7-172">INPUTS</span></span>

## <span data-ttu-id="13ad7-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13ad7-173">OUTPUTS</span></span>

## <span data-ttu-id="13ad7-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13ad7-174">NOTES</span></span>

## <span data-ttu-id="13ad7-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13ad7-175">RELATED LINKS</span></span>

[<span data-ttu-id="13ad7-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13ad7-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="13ad7-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="13ad7-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="13ad7-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="13ad7-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="13ad7-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13ad7-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="13ad7-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="13ad7-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


