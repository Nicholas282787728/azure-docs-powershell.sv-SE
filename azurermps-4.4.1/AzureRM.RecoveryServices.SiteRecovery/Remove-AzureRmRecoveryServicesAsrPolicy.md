---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575891"
---
# <span data-ttu-id="5dddd-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5dddd-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5dddd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5dddd-102">SYNOPSIS</span></span>
<span data-ttu-id="5dddd-103">Tar bort den angivna principen för automatisk ASR från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="5dddd-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dddd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5dddd-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dddd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5dddd-105">DESCRIPTION</span></span>
<span data-ttu-id="5dddd-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrPolicy** tog bort den angivna Replikeringsprincipen från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="5dddd-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5dddd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5dddd-107">EXAMPLES</span></span>

### <span data-ttu-id="5dddd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5dddd-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="5dddd-109">Tar bort den angivna replikeringsprincipen och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5dddd-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5dddd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5dddd-110">PARAMETERS</span></span>

### <span data-ttu-id="5dddd-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dddd-111">-InputObject</span></span>
<span data-ttu-id="5dddd-112">Indatavärdet till cmdleten: objektet ASR-replikeringsprincip som motsvarar den replikeringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5dddd-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dddd-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5dddd-113">-Confirm</span></span>
<span data-ttu-id="5dddd-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5dddd-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dddd-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dddd-115">-WhatIf</span></span>
<span data-ttu-id="5dddd-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5dddd-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5dddd-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5dddd-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dddd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dddd-118">CommonParameters</span></span>
<span data-ttu-id="5dddd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dddd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dddd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dddd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dddd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5dddd-121">INPUTS</span></span>

### <span data-ttu-id="5dddd-122">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5dddd-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5dddd-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5dddd-123">OUTPUTS</span></span>

### <span data-ttu-id="5dddd-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="5dddd-124">System.Object</span></span>

## <span data-ttu-id="5dddd-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5dddd-125">NOTES</span></span>

## <span data-ttu-id="5dddd-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5dddd-126">RELATED LINKS</span></span>

[<span data-ttu-id="5dddd-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5dddd-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="5dddd-128">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5dddd-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
