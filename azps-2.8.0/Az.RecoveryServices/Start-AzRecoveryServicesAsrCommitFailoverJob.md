---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 1e453f8b11929b96e6e0f2dbe96164c2bf351ae7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920186"
---
# <span data-ttu-id="63544-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="63544-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="63544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63544-102">SYNOPSIS</span></span>
<span data-ttu-id="63544-103">Startar åtgärden redundans för ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="63544-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="63544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63544-104">SYNTAX</span></span>

### <span data-ttu-id="63544-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="63544-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63544-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="63544-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63544-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63544-107">DESCRIPTION</span></span>
<span data-ttu-id="63544-108">Cmdleten **Start-AzRecoveryServicesAsrCommitFailoverJob** startar redundansväxlingen för ett Azure Site Recovery-objekt efter en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="63544-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="63544-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63544-109">EXAMPLES</span></span>

### <span data-ttu-id="63544-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63544-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="63544-111">Startar redundans för den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="63544-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63544-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63544-112">PARAMETERS</span></span>

### <span data-ttu-id="63544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63544-113">-DefaultProfile</span></span>
<span data-ttu-id="63544-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63544-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63544-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63544-115">-RecoveryPlan</span></span>
<span data-ttu-id="63544-116">Anger ett plan objekt för ASR för automatisk återställning motsvarande återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="63544-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63544-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63544-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="63544-118">Anger ett skyddat objekt-objekt för ASR som motsvarar det replikerade objekt som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="63544-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63544-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63544-119">-Confirm</span></span>
<span data-ttu-id="63544-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63544-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63544-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63544-121">-WhatIf</span></span>
<span data-ttu-id="63544-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63544-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63544-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63544-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63544-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63544-124">CommonParameters</span></span>
<span data-ttu-id="63544-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63544-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63544-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63544-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63544-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63544-127">INPUTS</span></span>

### <span data-ttu-id="63544-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63544-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="63544-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63544-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="63544-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63544-130">OUTPUTS</span></span>

### <span data-ttu-id="63544-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="63544-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63544-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63544-132">NOTES</span></span>

## <span data-ttu-id="63544-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63544-133">RELATED LINKS</span></span>
