---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755633"
---
# <span data-ttu-id="7b0ca-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b0ca-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="7b0ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0ca-103">Redigerar en plan för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b0ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b0ca-104">SYNTAX</span></span>

### <span data-ttu-id="7b0ca-105">AppendGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="7b0ca-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0ca-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="7b0ca-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0ca-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7b0ca-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0ca-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7b0ca-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0ca-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b0ca-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0ca-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b0ca-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b0ca-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b0ca-111">DESCRIPTION</span></span>
<span data-ttu-id="7b0ca-112">Cmdleten **Edit-AzureRmSiteRecoveryRecoveryPlan** redigerar en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="7b0ca-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b0ca-113">EXAMPLES</span></span>

## <span data-ttu-id="7b0ca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b0ca-114">PARAMETERS</span></span>

### <span data-ttu-id="7b0ca-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7b0ca-115">-AddProtectedEntities</span></span>
<span data-ttu-id="7b0ca-116">Anger en matris med skyddade enheter som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b0ca-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="7b0ca-118">-AppendGroup</span></span>
<span data-ttu-id="7b0ca-119">Anger att gruppen läggs till i återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-120">-Grupp</span><span class="sxs-lookup"><span data-stu-id="7b0ca-120">-Group</span></span>
<span data-ttu-id="7b0ca-121">Anger en plan för webbplats återställnings planer.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b0ca-122">-RecoveryPlan</span></span>
<span data-ttu-id="7b0ca-123">Anger en återställnings plan.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="7b0ca-124">-RemoveGroup</span></span>
<span data-ttu-id="7b0ca-125">Tar bort den angivna plan för återställning av arbets återställning.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7b0ca-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="7b0ca-127">Anger en matris med skyddade enheter.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7b0ca-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0ca-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0ca-129">-DefaultProfile</span></span>
<span data-ttu-id="7b0ca-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b0ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0ca-131">CommonParameters</span></span>
<span data-ttu-id="7b0ca-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0ca-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0ca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0ca-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b0ca-134">INPUTS</span></span>

### <span data-ttu-id="7b0ca-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b0ca-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="7b0ca-136">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7b0ca-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="7b0ca-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b0ca-137">OUTPUTS</span></span>

## <span data-ttu-id="7b0ca-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b0ca-138">NOTES</span></span>

## <span data-ttu-id="7b0ca-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b0ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="7b0ca-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b0ca-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7b0ca-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7b0ca-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
