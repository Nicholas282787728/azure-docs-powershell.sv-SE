---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099640"
---
# <span data-ttu-id="80598-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="80598-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="80598-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80598-102">SYNOPSIS</span></span>
<span data-ttu-id="80598-103">Startar ett länkat jobb på en replikeringsprincip som är associerad med en behållare för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="80598-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="80598-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80598-104">SYNTAX</span></span>

### <span data-ttu-id="80598-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="80598-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="80598-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="80598-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80598-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80598-107">DESCRIPTION</span></span>
<span data-ttu-id="80598-108">Cmdleten **Start-AzureSiteRecoveryProtectionProfileDissociationJob** initierar ett länkat jobb på den replikeringsprincip som är kopplad till en Azure Site Recovery-behållare.</span><span class="sxs-lookup"><span data-stu-id="80598-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="80598-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80598-109">EXAMPLES</span></span>

### <span data-ttu-id="80598-110">Exempel 1: koppla från en skydds profil</span><span class="sxs-lookup"><span data-stu-id="80598-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="80598-111">Det första kommandot får en skydds behållare med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar sedan behållaren i variabeln $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="80598-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="80598-112">Det andra kommandot får en skydds behållare och lagrar det sedan i $ProtectionContainer 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="80598-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="80598-113">Med kommandot slut kopplas skydds profilen från behållaren som lagras i $ProtectionContainer 01 som primär skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="80598-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="80598-114">Kommandot kopplas från behållaren som lagras i $ProtectionContainer 02 som behållare för återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="80598-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="80598-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80598-115">PARAMETERS</span></span>

### <span data-ttu-id="80598-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="80598-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="80598-117">Anger en primär skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="80598-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="80598-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="80598-118">-Profile</span></span>
<span data-ttu-id="80598-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="80598-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80598-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="80598-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80598-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="80598-121">-ProtectionProfile</span></span>
<span data-ttu-id="80598-122">Anger inställningar för skydds profil som ska avassocieras från skydds skåpen.</span><span class="sxs-lookup"><span data-stu-id="80598-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="80598-123">Anger inställningar för skydds profil som ska gälla för skydds skåpen.</span><span class="sxs-lookup"><span data-stu-id="80598-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="80598-124">Använd New-AzureSiteRecoveryProtectionProfileObject cmdlet för att få ett **ASRProtectionProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="80598-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="80598-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="80598-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="80598-126">Anger en återställnings skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="80598-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="80598-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80598-127">CommonParameters</span></span>
<span data-ttu-id="80598-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80598-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80598-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80598-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80598-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80598-130">INPUTS</span></span>

## <span data-ttu-id="80598-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80598-131">OUTPUTS</span></span>

## <span data-ttu-id="80598-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80598-132">NOTES</span></span>

## <span data-ttu-id="80598-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80598-133">RELATED LINKS</span></span>

[<span data-ttu-id="80598-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="80598-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="80598-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="80598-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="80598-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="80598-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


