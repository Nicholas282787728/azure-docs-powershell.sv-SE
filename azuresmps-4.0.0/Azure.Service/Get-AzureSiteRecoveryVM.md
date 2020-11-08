---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099799"
---
# <span data-ttu-id="fef3e-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="fef3e-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="fef3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fef3e-102">SYNOPSIS</span></span>
<span data-ttu-id="fef3e-103">Hämtar information om virtuella datorer som hanteras av webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="fef3e-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="fef3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fef3e-104">SYNTAX</span></span>

### <span data-ttu-id="fef3e-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="fef3e-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef3e-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="fef3e-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef3e-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="fef3e-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef3e-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fef3e-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fef3e-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="fef3e-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef3e-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="fef3e-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fef3e-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fef3e-111">DESCRIPTION</span></span>
<span data-ttu-id="fef3e-112">Cmdleten **Get-AzureSiteRecoveryVM** hämtar information om virtuella datorer som hanteras i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fef3e-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="fef3e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fef3e-113">EXAMPLES</span></span>

### <span data-ttu-id="fef3e-114">Exempel 1: Hämta information om en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fef3e-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="fef3e-115">Det första kommandot använder cmdleten **Get-AzureSiteRecoveryProtectionContainer** för att hämta en skyddad container och lagrar den sedan i $ProtectionContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="fef3e-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="fef3e-116">Det andra kommandot får information om de virtuella datorerna i $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="fef3e-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="fef3e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fef3e-117">PARAMETERS</span></span>

### <span data-ttu-id="fef3e-118">-ID</span><span class="sxs-lookup"><span data-stu-id="fef3e-118">-Id</span></span>
<span data-ttu-id="fef3e-119">Anger ID för den virtuella dator som du vill hämta information om.</span><span class="sxs-lookup"><span data-stu-id="fef3e-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="fef3e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fef3e-120">-Name</span></span>
<span data-ttu-id="fef3e-121">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fef3e-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fef3e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="fef3e-122">-Profile</span></span>
<span data-ttu-id="fef3e-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fef3e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fef3e-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fef3e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fef3e-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fef3e-125">-ProtectionContainer</span></span>
<span data-ttu-id="fef3e-126">Anger objekt för objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="fef3e-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="fef3e-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="fef3e-127">-ProtectionContainerId</span></span>
<span data-ttu-id="fef3e-128">Anger ID för en skyddad behållare för vilken du vill få information.</span><span class="sxs-lookup"><span data-stu-id="fef3e-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="fef3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef3e-129">CommonParameters</span></span>
<span data-ttu-id="fef3e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef3e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef3e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef3e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fef3e-132">INPUTS</span></span>

## <span data-ttu-id="fef3e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fef3e-133">OUTPUTS</span></span>

## <span data-ttu-id="fef3e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fef3e-134">NOTES</span></span>

## <span data-ttu-id="fef3e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fef3e-135">RELATED LINKS</span></span>

[<span data-ttu-id="fef3e-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="fef3e-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


