---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927573"
---
# <span data-ttu-id="0839e-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0839e-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="0839e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0839e-102">SYNOPSIS</span></span>
<span data-ttu-id="0839e-103">Redigerar en plan för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="0839e-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="0839e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0839e-104">SYNTAX</span></span>

### <span data-ttu-id="0839e-105">AppendGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="0839e-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0839e-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0839e-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0839e-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0839e-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0839e-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0839e-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0839e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0839e-109">DESCRIPTION</span></span>
<span data-ttu-id="0839e-110">Cmdleten **Edit-AzRecoveryServicesAsrRecoveryPlan** redigerar en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="0839e-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="0839e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0839e-111">EXAMPLES</span></span>

### <span data-ttu-id="0839e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0839e-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="0839e-113">Lägger till en grupp till befintlig Azure Site Recovery-plan och returnerar den uppdaterade återställnings planen i minnet.</span><span class="sxs-lookup"><span data-stu-id="0839e-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="0839e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0839e-114">PARAMETERS</span></span>

### <span data-ttu-id="0839e-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0839e-115">-AddProtectedItem</span></span>
<span data-ttu-id="0839e-116">Lista över skyddade objekt i ASR som ska läggas till i återställnings Plans gruppen i återställnings Plans objekt.</span><span class="sxs-lookup"><span data-stu-id="0839e-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0839e-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="0839e-117">-AppendGroup</span></span>
<span data-ttu-id="0839e-118">Växla parameter för att lägga till en återställnings Plans grupp i återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="0839e-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="0839e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0839e-119">-DefaultProfile</span></span>
<span data-ttu-id="0839e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0839e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0839e-121">-Grupp</span><span class="sxs-lookup"><span data-stu-id="0839e-121">-Group</span></span>
<span data-ttu-id="0839e-122">Anger en återställnings Plans grupp.</span><span class="sxs-lookup"><span data-stu-id="0839e-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0839e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0839e-123">-InputObject</span></span>
<span data-ttu-id="0839e-124">Det objekt för ASR-återställning som ska redige ras (i minnes operation.</span><span class="sxs-lookup"><span data-stu-id="0839e-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="0839e-125">Om du vill uppdatera återställnings planen kör Update-AzASRRecoveryPlan med det redigerade objektet för återställnings plan.)</span><span class="sxs-lookup"><span data-stu-id="0839e-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0839e-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0839e-126">-RemoveGroup</span></span>
<span data-ttu-id="0839e-127">Tar bort den angivna gruppen från återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="0839e-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0839e-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0839e-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="0839e-129">Lista över skyddade objekt i ASR som ska tas bort från gruppen återställnings plan i återställnings Plans objekt.</span><span class="sxs-lookup"><span data-stu-id="0839e-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0839e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0839e-130">-Confirm</span></span>
<span data-ttu-id="0839e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0839e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0839e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0839e-132">-WhatIf</span></span>
<span data-ttu-id="0839e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0839e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0839e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0839e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0839e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0839e-135">CommonParameters</span></span>
<span data-ttu-id="0839e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0839e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0839e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0839e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0839e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0839e-138">INPUTS</span></span>

### <span data-ttu-id="0839e-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0839e-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0839e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0839e-140">OUTPUTS</span></span>

### <span data-ttu-id="0839e-141">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0839e-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0839e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0839e-142">NOTES</span></span>

## <span data-ttu-id="0839e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0839e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0839e-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0839e-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0839e-145">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0839e-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
