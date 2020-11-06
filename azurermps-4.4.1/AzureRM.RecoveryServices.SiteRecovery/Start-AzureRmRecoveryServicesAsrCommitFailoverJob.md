---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581359"
---
# <span data-ttu-id="91ada-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="91ada-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="91ada-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91ada-102">SYNOPSIS</span></span>
<span data-ttu-id="91ada-103">Startar åtgärden redundans för ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="91ada-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91ada-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91ada-104">SYNTAX</span></span>

### <span data-ttu-id="91ada-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="91ada-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ada-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="91ada-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91ada-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91ada-107">DESCRIPTION</span></span>
<span data-ttu-id="91ada-108">Cmdleten **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** startar redundansväxlingen för ett Azure Site Recovery-objekt efter en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="91ada-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="91ada-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91ada-109">EXAMPLES</span></span>

### <span data-ttu-id="91ada-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="91ada-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="91ada-111">Startar redundans för den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="91ada-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="91ada-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91ada-112">PARAMETERS</span></span>

### <span data-ttu-id="91ada-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="91ada-113">-RecoveryPlan</span></span>
<span data-ttu-id="91ada-114">Anger ett plan objekt för ASR-återställning.</span><span class="sxs-lookup"><span data-stu-id="91ada-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="91ada-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91ada-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="91ada-116">Anger ett skyddat objekt-objekt för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="91ada-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="91ada-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91ada-117">-Confirm</span></span>
<span data-ttu-id="91ada-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91ada-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ada-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ada-119">-WhatIf</span></span>
<span data-ttu-id="91ada-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91ada-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91ada-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91ada-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ada-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ada-122">CommonParameters</span></span>
<span data-ttu-id="91ada-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ada-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ada-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ada-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ada-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91ada-125">INPUTS</span></span>

### <span data-ttu-id="91ada-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="91ada-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="91ada-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="91ada-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="91ada-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91ada-128">OUTPUTS</span></span>

### <span data-ttu-id="91ada-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="91ada-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91ada-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91ada-130">NOTES</span></span>

## <span data-ttu-id="91ada-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91ada-131">RELATED LINKS</span></span>

