---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756882"
---
# <span data-ttu-id="ddc00-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ddc00-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="ddc00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddc00-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc00-103">Startar en oplanerad redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="ddc00-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddc00-104">SYNTAX</span></span>

### <span data-ttu-id="ddc00-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="ddc00-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc00-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ddc00-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc00-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddc00-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc00-108">Cmdleten **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** startar den oplanerade redundansväxlingen av ett skyddat objekt eller en återställnings plan för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ddc00-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ddc00-109">Du kan kontrol lera om jobbet följer med Get-AzureRmRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc00-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ddc00-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddc00-110">EXAMPLES</span></span>

### <span data-ttu-id="ddc00-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddc00-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="ddc00-112">Startar den oväntade redundansväxlingen för den angivna återställnings planen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ddc00-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ddc00-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddc00-113">PARAMETERS</span></span>

### <span data-ttu-id="ddc00-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ddc00-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ddc00-115">Anger den primära certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="ddc00-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="ddc00-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ddc00-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ddc00-117">Anger den sekundära certifikats filen.</span><span class="sxs-lookup"><span data-stu-id="ddc00-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="ddc00-118">-Riktning</span><span class="sxs-lookup"><span data-stu-id="ddc00-118">-Direction</span></span>
<span data-ttu-id="ddc00-119">Anger riktningen för redundansväxlingen.</span><span class="sxs-lookup"><span data-stu-id="ddc00-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ddc00-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ddc00-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddc00-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ddc00-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="ddc00-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ddc00-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ddc00-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="ddc00-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="ddc00-124">Anger att eventuella käll webbplats operationer som anges i återställnings planen måste göras som en del av fail over.</span><span class="sxs-lookup"><span data-stu-id="ddc00-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc00-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ddc00-125">-RecoveryPlan</span></span>
<span data-ttu-id="ddc00-126">Anger ett plan objekt för ASR som motsvarar återställnings planen som ska användas för att redundansväxla redundans ska utföras.</span><span class="sxs-lookup"><span data-stu-id="ddc00-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="ddc00-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ddc00-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ddc00-128">Anger det skyddade objektet för ASR-replikerade objekt som motsvarar det replikerade objekt som redundansväxlingen ska utföras på.</span><span class="sxs-lookup"><span data-stu-id="ddc00-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="ddc00-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddc00-129">-Confirm</span></span>
<span data-ttu-id="ddc00-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddc00-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc00-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc00-131">-WhatIf</span></span>
<span data-ttu-id="ddc00-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddc00-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddc00-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddc00-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc00-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc00-134">CommonParameters</span></span>
<span data-ttu-id="ddc00-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc00-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc00-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc00-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc00-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddc00-137">INPUTS</span></span>

### <span data-ttu-id="ddc00-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ddc00-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="ddc00-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ddc00-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ddc00-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddc00-140">OUTPUTS</span></span>

### <span data-ttu-id="ddc00-141">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ddc00-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ddc00-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddc00-142">NOTES</span></span>

## <span data-ttu-id="ddc00-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddc00-143">RELATED LINKS</span></span>

[<span data-ttu-id="ddc00-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ddc00-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


