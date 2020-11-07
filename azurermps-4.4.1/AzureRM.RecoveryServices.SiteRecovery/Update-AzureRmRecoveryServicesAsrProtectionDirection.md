---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756876"
---
# <span data-ttu-id="387e3-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="387e3-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="387e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="387e3-102">SYNOPSIS</span></span>
<span data-ttu-id="387e3-103">Uppdaterar replikeringsfrekvensen för det angivna replikerade skyddade objektet eller återställnings planen.</span><span class="sxs-lookup"><span data-stu-id="387e3-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="387e3-104">Används för att återaktivera/omvända replikera ett misslyckat över replikerat objekt eller återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="387e3-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="387e3-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="387e3-105">SYNTAX</span></span>

### <span data-ttu-id="387e3-106">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="387e3-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387e3-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="387e3-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387e3-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="387e3-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="387e3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="387e3-109">DESCRIPTION</span></span>
<span data-ttu-id="387e3-110">Cmdleten **Update-AzureRmRecoveryServicesAsrProtectionDirection** uppdaterar replikeringsfrekvensen för det angivna Azure Site Recovery-objektet efter att commit-åtgärden slutförts.</span><span class="sxs-lookup"><span data-stu-id="387e3-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="387e3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="387e3-111">EXAMPLES</span></span>

### <span data-ttu-id="387e3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="387e3-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="387e3-113">Starta uppdaterings åtgärden för det angivna recoveyr-abonnemanget och returnerar det ASR-objekt som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="387e3-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="387e3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="387e3-114">PARAMETERS</span></span>

### <span data-ttu-id="387e3-115">-Riktning</span><span class="sxs-lookup"><span data-stu-id="387e3-115">-Direction</span></span>
<span data-ttu-id="387e3-116">Anger i vilken riktning som ska användas för uppdaterings åtgärden publicera en redundans.</span><span class="sxs-lookup"><span data-stu-id="387e3-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="387e3-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="387e3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="387e3-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="387e3-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="387e3-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="387e3-119">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387e3-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="387e3-120">-RecoveryPlan</span></span>
<span data-ttu-id="387e3-121">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="387e3-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="387e3-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="387e3-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="387e3-123">Anger ett skyddat objekt i ASR-replikering</span><span class="sxs-lookup"><span data-stu-id="387e3-123">Specifies an ASR replication protected item</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="387e3-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="387e3-124">-Confirm</span></span>
<span data-ttu-id="387e3-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="387e3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387e3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387e3-126">-WhatIf</span></span>
<span data-ttu-id="387e3-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="387e3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="387e3-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="387e3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387e3-129">CommonParameters</span></span>
<span data-ttu-id="387e3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387e3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387e3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="387e3-132">INPUTS</span></span>

### <span data-ttu-id="387e3-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="387e3-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="387e3-134">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="387e3-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="387e3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="387e3-135">OUTPUTS</span></span>

### <span data-ttu-id="387e3-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="387e3-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="387e3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="387e3-137">NOTES</span></span>

## <span data-ttu-id="387e3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="387e3-138">RELATED LINKS</span></span>

