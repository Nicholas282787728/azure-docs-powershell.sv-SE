---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099630"
---
# <span data-ttu-id="f87ed-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="f87ed-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="f87ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f87ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f87ed-103">Uppdaterar käll-och mål servern för att skydda ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="f87ed-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="f87ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f87ed-104">SYNTAX</span></span>

### <span data-ttu-id="f87ed-105">ByRPObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f87ed-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f87ed-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="f87ed-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f87ed-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="f87ed-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f87ed-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f87ed-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f87ed-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f87ed-109">DESCRIPTION</span></span>
<span data-ttu-id="f87ed-110">Cmdleten **Update-AzureSiteRecoveryProtectionDirection** uppdaterar käll-och mål servern för att skydda ett Azure Site Recovery-objekt när en redundans utförs.</span><span class="sxs-lookup"><span data-stu-id="f87ed-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="f87ed-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f87ed-111">EXAMPLES</span></span>

### <span data-ttu-id="f87ed-112">Exempel 1: ändra riktningen för ett skyddat objekt i en behållare</span><span class="sxs-lookup"><span data-stu-id="f87ed-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
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

<span data-ttu-id="f87ed-113">Det första kommandot hämtar de skyddade behållarna i det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar dem sedan i $container variabel.</span><span class="sxs-lookup"><span data-stu-id="f87ed-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="f87ed-114">Det andra kommandot får de virtuella datorerna som tillhör behållaren som lagras i $Container genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="f87ed-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="f87ed-115">Kommandot lagrar resultaten i variabeln $Protected.</span><span class="sxs-lookup"><span data-stu-id="f87ed-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="f87ed-116">Det sista kommandot ställer in riktningen på RecoverToPrimary för de objekt som finns i $Protected.</span><span class="sxs-lookup"><span data-stu-id="f87ed-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="f87ed-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f87ed-117">PARAMETERS</span></span>

### <span data-ttu-id="f87ed-118">-Riktning</span><span class="sxs-lookup"><span data-stu-id="f87ed-118">-Direction</span></span>
<span data-ttu-id="f87ed-119">Anger riktningen för bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="f87ed-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="f87ed-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f87ed-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f87ed-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f87ed-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="f87ed-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f87ed-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f87ed-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="f87ed-123">-Profile</span></span>
<span data-ttu-id="f87ed-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f87ed-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f87ed-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f87ed-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f87ed-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f87ed-126">-ProtectionContainerId</span></span>
<span data-ttu-id="f87ed-127">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="f87ed-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="f87ed-128">Denna cmdlet ändrar riktningen för en skyddad virtuell dator som tillhör den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f87ed-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="f87ed-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f87ed-129">-ProtectionEntity</span></span>
<span data-ttu-id="f87ed-130">Anger objektet skydd.</span><span class="sxs-lookup"><span data-stu-id="f87ed-130">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="f87ed-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="f87ed-131">-ProtectionEntityId</span></span>
<span data-ttu-id="f87ed-132">Anger ID för en skyddad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f87ed-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="f87ed-133">Denna cmdlet ändrar riktningen för den skyddade virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f87ed-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f87ed-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f87ed-134">-RecoveryPlan</span></span>
<span data-ttu-id="f87ed-135">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="f87ed-135">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="f87ed-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="f87ed-136">-RPId</span></span>
<span data-ttu-id="f87ed-137">Anger ID för en återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="f87ed-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="f87ed-138">Denna cmdlet ändrar riktningen för det återställnings abonnemang som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f87ed-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

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

### <span data-ttu-id="f87ed-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f87ed-139">-WaitForCompletion</span></span>
<span data-ttu-id="f87ed-140">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="f87ed-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f87ed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87ed-141">CommonParameters</span></span>
<span data-ttu-id="f87ed-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87ed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87ed-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87ed-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87ed-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f87ed-144">INPUTS</span></span>

## <span data-ttu-id="f87ed-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f87ed-145">OUTPUTS</span></span>

## <span data-ttu-id="f87ed-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f87ed-146">NOTES</span></span>

## <span data-ttu-id="f87ed-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f87ed-147">RELATED LINKS</span></span>

[<span data-ttu-id="f87ed-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f87ed-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f87ed-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f87ed-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


