---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573942"
---
# <span data-ttu-id="63fd5-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="63fd5-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="63fd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="63fd5-103">Startar åtgärden redundans för ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="63fd5-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63fd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63fd5-104">SYNTAX</span></span>

### <span data-ttu-id="63fd5-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="63fd5-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fd5-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="63fd5-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fd5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63fd5-107">DESCRIPTION</span></span>
<span data-ttu-id="63fd5-108">Cmdleten **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** startar redundansväxlingen för ett Azure Site Recovery-objekt efter en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="63fd5-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="63fd5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63fd5-109">EXAMPLES</span></span>

### <span data-ttu-id="63fd5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63fd5-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="63fd5-111">Startar redundans för den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="63fd5-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63fd5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63fd5-112">PARAMETERS</span></span>

### <span data-ttu-id="63fd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fd5-113">-DefaultProfile</span></span>
<span data-ttu-id="63fd5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63fd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fd5-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63fd5-115">-RecoveryPlan</span></span>
<span data-ttu-id="63fd5-116">Anger ett plan objekt för ASR för automatisk återställning motsvarande återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="63fd5-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="63fd5-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63fd5-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="63fd5-118">Anger ett skyddat objekt-objekt för ASR som motsvarar det replikerade objekt som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="63fd5-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="63fd5-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63fd5-119">-Confirm</span></span>
<span data-ttu-id="63fd5-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63fd5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fd5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fd5-121">-WhatIf</span></span>
<span data-ttu-id="63fd5-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63fd5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63fd5-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63fd5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fd5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fd5-124">CommonParameters</span></span>
<span data-ttu-id="63fd5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fd5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fd5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fd5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fd5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63fd5-127">INPUTS</span></span>

### <span data-ttu-id="63fd5-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63fd5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="63fd5-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63fd5-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="63fd5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63fd5-130">OUTPUTS</span></span>

### <span data-ttu-id="63fd5-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="63fd5-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63fd5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63fd5-132">NOTES</span></span>

## <span data-ttu-id="63fd5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63fd5-133">RELATED LINKS</span></span>
