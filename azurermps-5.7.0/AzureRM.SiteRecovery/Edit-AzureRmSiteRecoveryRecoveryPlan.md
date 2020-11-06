---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581963"
---
# <span data-ttu-id="0e331-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e331-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="0e331-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e331-102">SYNOPSIS</span></span>
<span data-ttu-id="0e331-103">Redigerar en plan för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="0e331-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e331-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e331-104">SYNTAX</span></span>

### <span data-ttu-id="0e331-105">AppendGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="0e331-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e331-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0e331-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e331-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="0e331-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e331-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="0e331-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e331-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0e331-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e331-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0e331-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e331-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e331-111">DESCRIPTION</span></span>
<span data-ttu-id="0e331-112">Cmdleten **Edit-AzureRmSiteRecoveryRecoveryPlan** redigerar en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="0e331-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="0e331-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e331-113">EXAMPLES</span></span>

## <span data-ttu-id="0e331-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e331-114">PARAMETERS</span></span>

### <span data-ttu-id="0e331-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="0e331-115">-AddProtectedEntities</span></span>
<span data-ttu-id="0e331-116">Anger en matris med skyddade enheter som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="0e331-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0e331-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="0e331-118">-AppendGroup</span></span>
<span data-ttu-id="0e331-119">Anger att gruppen läggs till i återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="0e331-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e331-120">-DefaultProfile</span></span>
<span data-ttu-id="0e331-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e331-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-122">-Grupp</span><span class="sxs-lookup"><span data-stu-id="0e331-122">-Group</span></span>
<span data-ttu-id="0e331-123">Anger en plan för webbplats återställnings planer.</span><span class="sxs-lookup"><span data-stu-id="0e331-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e331-124">-RecoveryPlan</span></span>
<span data-ttu-id="0e331-125">Anger en återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="0e331-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0e331-126">-RemoveGroup</span></span>
<span data-ttu-id="0e331-127">Tar bort den angivna plan för återställning av arbets återställning.</span><span class="sxs-lookup"><span data-stu-id="0e331-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="0e331-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="0e331-129">Anger en matris med skyddade enheter.</span><span class="sxs-lookup"><span data-stu-id="0e331-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0e331-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e331-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e331-131">CommonParameters</span></span>
<span data-ttu-id="0e331-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e331-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e331-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e331-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e331-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e331-134">INPUTS</span></span>

### <span data-ttu-id="0e331-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e331-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="0e331-136">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0e331-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="0e331-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e331-137">OUTPUTS</span></span>

## <span data-ttu-id="0e331-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e331-138">NOTES</span></span>

## <span data-ttu-id="0e331-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e331-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e331-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e331-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="0e331-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0e331-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
