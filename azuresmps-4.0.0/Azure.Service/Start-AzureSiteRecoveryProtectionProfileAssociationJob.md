---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099078"
---
# <span data-ttu-id="7d750-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="7d750-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="7d750-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d750-102">SYNOPSIS</span></span>
<span data-ttu-id="7d750-103">Startar ett projekt för en replikeringsprincip för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="7d750-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="7d750-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d750-104">SYNTAX</span></span>

### <span data-ttu-id="7d750-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="7d750-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d750-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7d750-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d750-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d750-107">DESCRIPTION</span></span>
<span data-ttu-id="7d750-108">Cmdleten **Start-AzureSiteRecoveryProtectionProfileAssociationJob** initierar ett Associations jobb för att koppla en replikeringsprincip till en Azure Site Recovery Protection-behållare.</span><span class="sxs-lookup"><span data-stu-id="7d750-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="7d750-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d750-109">EXAMPLES</span></span>

### <span data-ttu-id="7d750-110">Exempel 1: associera en skydds profil</span><span class="sxs-lookup"><span data-stu-id="7d750-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="7d750-111">Det första kommandot får en skydds behållare med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan behållaren i variabeln $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="7d750-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="7d750-112">Det andra kommandot skapar en skydds profil med hjälp av **New-AzureSiteRecoveryProtectionProfileObject** cmdlet och lagrar den skydds profilen i variabeln $ProtectionProfile.</span><span class="sxs-lookup"><span data-stu-id="7d750-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="7d750-113">Det tredje kommandot får en skydds behållare och lagrar det sedan i $ProtectionContainer 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="7d750-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="7d750-114">Det sista kommandot associerar skydds profilen som lagras i $ProtectionProfile till behållaren som är lagrad i $ProtectionContainer 01 som primär skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="7d750-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="7d750-115">Kommandot kopplar behållaren som lagras i $ProtectionContainer 02 som behållare för återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="7d750-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="7d750-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d750-116">PARAMETERS</span></span>

### <span data-ttu-id="7d750-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d750-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="7d750-118">Anger den primära skydds behållaren där inställningarna för skydds profilen ska tillämpas.</span><span class="sxs-lookup"><span data-stu-id="7d750-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d750-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="7d750-119">-Profile</span></span>
<span data-ttu-id="7d750-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7d750-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d750-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7d750-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d750-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="7d750-122">-ProtectionProfile</span></span>
<span data-ttu-id="7d750-123">Anger inställningar för skydds profil som ska gälla för skydds skåpen.</span><span class="sxs-lookup"><span data-stu-id="7d750-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="7d750-124">Använd New-AzureSiteRecoveryProtectionProfileObject cmdlet för att få ett **ASRProtectionProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7d750-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d750-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d750-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="7d750-126">Anger återställnings skydds behållaren där inställningarna för skydds profilen ska tillämpas.</span><span class="sxs-lookup"><span data-stu-id="7d750-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d750-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d750-127">CommonParameters</span></span>
<span data-ttu-id="7d750-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d750-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d750-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d750-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d750-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d750-130">INPUTS</span></span>

## <span data-ttu-id="7d750-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d750-131">OUTPUTS</span></span>

## <span data-ttu-id="7d750-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d750-132">NOTES</span></span>

## <span data-ttu-id="7d750-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d750-133">RELATED LINKS</span></span>

[<span data-ttu-id="7d750-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d750-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7d750-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="7d750-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="7d750-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="7d750-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


