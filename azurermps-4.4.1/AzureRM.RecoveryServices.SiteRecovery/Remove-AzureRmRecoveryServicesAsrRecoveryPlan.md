---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758020"
---
# <span data-ttu-id="d8e1b-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8e1b-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d8e1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e1b-103">Avhjälper den angivna planen för ASR-återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8e1b-104">SYNTAX</span></span>

### <span data-ttu-id="d8e1b-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="d8e1b-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e1b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8e1b-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e1b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8e1b-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e1b-108">Cmdleten **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** tar bort den angivna återställnings planen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="d8e1b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8e1b-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e1b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8e1b-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="d8e1b-111">Tar bort den angivna återställnings planen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d8e1b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8e1b-112">PARAMETERS</span></span>

### <span data-ttu-id="d8e1b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e1b-113">-InputObject</span></span>
<span data-ttu-id="d8e1b-114">Indatavärdet till cmdleten: det objekt för ASR-återställning som motsvarar återställnings planen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e1b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8e1b-115">-Name</span></span>
<span data-ttu-id="d8e1b-116">Anger namnet på den återställnings plan som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e1b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8e1b-117">-Confirm</span></span>
<span data-ttu-id="d8e1b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e1b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e1b-119">-WhatIf</span></span>
<span data-ttu-id="d8e1b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8e1b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e1b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e1b-122">CommonParameters</span></span>
<span data-ttu-id="d8e1b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e1b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e1b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e1b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e1b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8e1b-125">INPUTS</span></span>

### <span data-ttu-id="d8e1b-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8e1b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d8e1b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8e1b-127">OUTPUTS</span></span>

### <span data-ttu-id="d8e1b-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="d8e1b-128">System.Object</span></span>

## <span data-ttu-id="d8e1b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8e1b-129">NOTES</span></span>

## <span data-ttu-id="d8e1b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8e1b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d8e1b-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8e1b-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d8e1b-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8e1b-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d8e1b-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8e1b-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


