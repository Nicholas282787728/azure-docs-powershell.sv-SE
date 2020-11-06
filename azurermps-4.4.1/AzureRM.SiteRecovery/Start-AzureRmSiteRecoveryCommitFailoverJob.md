---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575802"
---
# <span data-ttu-id="f9318-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f9318-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="f9318-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9318-102">SYNOPSIS</span></span>
<span data-ttu-id="f9318-103">Startar åtgärden redundans för ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="f9318-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9318-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9318-104">SYNTAX</span></span>

### <span data-ttu-id="f9318-105">ByRPIObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f9318-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9318-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f9318-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9318-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f9318-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9318-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9318-108">DESCRIPTION</span></span>
<span data-ttu-id="f9318-109">Cmdleten **Start-AzureRmSiteRecoveryCommitFailoverJob** startar redundansväxlingen för ett Azure Site Recovery-objekt efter en redundansväxling.</span><span class="sxs-lookup"><span data-stu-id="f9318-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="f9318-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9318-110">EXAMPLES</span></span>

## <span data-ttu-id="f9318-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9318-111">PARAMETERS</span></span>

### <span data-ttu-id="f9318-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f9318-112">-ProtectionEntity</span></span>
<span data-ttu-id="f9318-113">Anger objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="f9318-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9318-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9318-114">-RecoveryPlan</span></span>
<span data-ttu-id="f9318-115">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="f9318-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9318-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9318-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9318-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9318-117">-DefaultProfile</span></span>
<span data-ttu-id="f9318-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9318-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9318-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9318-119">CommonParameters</span></span>
<span data-ttu-id="f9318-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9318-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9318-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9318-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9318-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9318-122">INPUTS</span></span>

### <span data-ttu-id="f9318-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f9318-123">ASRProtectionEntity</span></span>
<span data-ttu-id="f9318-124">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f9318-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="f9318-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9318-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="f9318-126">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f9318-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="f9318-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9318-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f9318-128">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f9318-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f9318-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9318-129">OUTPUTS</span></span>

### <span data-ttu-id="f9318-130">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f9318-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f9318-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9318-131">NOTES</span></span>

## <span data-ttu-id="f9318-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9318-132">RELATED LINKS</span></span>

