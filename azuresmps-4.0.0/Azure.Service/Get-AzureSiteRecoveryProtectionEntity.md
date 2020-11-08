---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093314"
---
# <span data-ttu-id="04d59-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="04d59-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="04d59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04d59-102">SYNOPSIS</span></span>
<span data-ttu-id="04d59-103">Får skydds bara eller skyddade enheter i ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="04d59-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="04d59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04d59-104">SYNTAX</span></span>

### <span data-ttu-id="04d59-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="04d59-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="04d59-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="04d59-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04d59-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="04d59-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="04d59-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="04d59-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04d59-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="04d59-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04d59-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="04d59-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="04d59-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04d59-111">DESCRIPTION</span></span>
<span data-ttu-id="04d59-112">Cmdleten **Get-AzureSiteRecoveryProtectionEntity** får skydd bara eller skyddade enheter, till exempel virtuella datorer, i det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="04d59-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="04d59-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04d59-113">EXAMPLES</span></span>

### <span data-ttu-id="04d59-114">Exempel 1: Visa en skyddad virtuell dator i en behållare</span><span class="sxs-lookup"><span data-stu-id="04d59-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="04d59-115">Det första kommandot får en skyddad container med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan objektet i variabeln $container.</span><span class="sxs-lookup"><span data-stu-id="04d59-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="04d59-116">Det andra kommandot hämtar den skyddade virtuella datorn som tillhör behållaren i $Container och visar den.</span><span class="sxs-lookup"><span data-stu-id="04d59-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="04d59-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04d59-117">PARAMETERS</span></span>

### <span data-ttu-id="04d59-118">-ID</span><span class="sxs-lookup"><span data-stu-id="04d59-118">-Id</span></span>
<span data-ttu-id="04d59-119">Anger ID för en skydds enhet att hämta.</span><span class="sxs-lookup"><span data-stu-id="04d59-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d59-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="04d59-120">-Name</span></span>
<span data-ttu-id="04d59-121">Anger namnet på en skydds enhet som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="04d59-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d59-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="04d59-122">-Profile</span></span>
<span data-ttu-id="04d59-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="04d59-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04d59-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="04d59-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04d59-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="04d59-125">-ProtectionContainer</span></span>
<span data-ttu-id="04d59-126">Anger en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="04d59-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04d59-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="04d59-127">-ProtectionContainerId</span></span>
<span data-ttu-id="04d59-128">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="04d59-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d59-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d59-129">CommonParameters</span></span>
<span data-ttu-id="04d59-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d59-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d59-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d59-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d59-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04d59-132">INPUTS</span></span>

## <span data-ttu-id="04d59-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04d59-133">OUTPUTS</span></span>

## <span data-ttu-id="04d59-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04d59-134">NOTES</span></span>

## <span data-ttu-id="04d59-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04d59-135">RELATED LINKS</span></span>

[<span data-ttu-id="04d59-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="04d59-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="04d59-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="04d59-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="04d59-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="04d59-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


