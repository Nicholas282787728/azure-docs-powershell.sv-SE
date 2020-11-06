---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581036"
---
# <span data-ttu-id="83d46-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="83d46-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="83d46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83d46-102">SYNOPSIS</span></span>
<span data-ttu-id="83d46-103">Redigerar en plan för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="83d46-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83d46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83d46-104">SYNTAX</span></span>

### <span data-ttu-id="83d46-105">AppendGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="83d46-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d46-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="83d46-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d46-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="83d46-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d46-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="83d46-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d46-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83d46-109">DESCRIPTION</span></span>
<span data-ttu-id="83d46-110">Cmdleten **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** redigerar en Azure Site Recovery-plan.</span><span class="sxs-lookup"><span data-stu-id="83d46-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="83d46-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83d46-111">EXAMPLES</span></span>

### <span data-ttu-id="83d46-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83d46-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="83d46-113">Lägger till en grupp till befintlig Azure Site Recovery-plan och returnerar den uppdaterade återställnings planen i minnet.</span><span class="sxs-lookup"><span data-stu-id="83d46-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="83d46-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83d46-114">PARAMETERS</span></span>

### <span data-ttu-id="83d46-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83d46-115">-AddProtectedItem</span></span>
<span data-ttu-id="83d46-116">Lista över skyddade objekt i ASR som ska läggas till i återställnings Plans gruppen i återställnings Plans objekt.</span><span class="sxs-lookup"><span data-stu-id="83d46-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d46-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="83d46-117">-AppendGroup</span></span>
<span data-ttu-id="83d46-118">Växla parameter för att lägga till en återställnings Plans grupp i återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="83d46-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="83d46-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83d46-119">-Confirm</span></span>
<span data-ttu-id="83d46-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83d46-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d46-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d46-121">-DefaultProfile</span></span>
<span data-ttu-id="83d46-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="83d46-123">-Grupp</span><span class="sxs-lookup"><span data-stu-id="83d46-123">-Group</span></span>
<span data-ttu-id="83d46-124">Anger en återställnings Plans grupp.</span><span class="sxs-lookup"><span data-stu-id="83d46-124">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d46-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d46-125">-InputObject</span></span>
<span data-ttu-id="83d46-126">Det objekt för ASR-återställning som ska redige ras (i minnes operation.</span><span class="sxs-lookup"><span data-stu-id="83d46-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="83d46-127">Om du vill uppdatera återställnings planen kör Update-AzureRmASRRecoveryPlan med det redigerade objektet för återställnings plan.)</span><span class="sxs-lookup"><span data-stu-id="83d46-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d46-128">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="83d46-128">-RemoveGroup</span></span>
<span data-ttu-id="83d46-129">Tar bort den angivna gruppen från återställnings planens objekt.</span><span class="sxs-lookup"><span data-stu-id="83d46-129">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="83d46-130">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="83d46-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="83d46-131">Lista över skyddade objekt i ASR som ska tas bort från gruppen återställnings plan i återställnings Plans objekt.</span><span class="sxs-lookup"><span data-stu-id="83d46-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d46-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d46-132">-WhatIf</span></span>
<span data-ttu-id="83d46-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83d46-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83d46-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83d46-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d46-135">CommonParameters</span></span>
<span data-ttu-id="83d46-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d46-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d46-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d46-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83d46-138">INPUTS</span></span>

### <span data-ttu-id="83d46-139">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="83d46-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="83d46-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83d46-140">OUTPUTS</span></span>

### <span data-ttu-id="83d46-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="83d46-141">System.Object</span></span>

## <span data-ttu-id="83d46-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83d46-142">NOTES</span></span>

## <span data-ttu-id="83d46-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83d46-143">RELATED LINKS</span></span>

[<span data-ttu-id="83d46-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="83d46-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="83d46-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="83d46-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
