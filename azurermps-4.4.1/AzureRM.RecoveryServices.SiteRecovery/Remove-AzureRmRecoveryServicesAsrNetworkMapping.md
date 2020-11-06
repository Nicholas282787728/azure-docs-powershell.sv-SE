---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575890"
---
# <span data-ttu-id="0f350-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0f350-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0f350-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f350-102">SYNOPSIS</span></span>
<span data-ttu-id="0f350-103">Tar bort den angivna nätverks mappningen för automatisk system återställning från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="0f350-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f350-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f350-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f350-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f350-105">DESCRIPTION</span></span>
<span data-ttu-id="0f350-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrNetworkMapping** tar bort den angivna nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="0f350-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="0f350-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f350-107">EXAMPLES</span></span>

### <span data-ttu-id="0f350-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f350-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="0f350-109">Tar bort den angivna nätverks mappningen för automatisk återställning och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="0f350-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0f350-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f350-110">PARAMETERS</span></span>

### <span data-ttu-id="0f350-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f350-111">-InputObject</span></span>
<span data-ttu-id="0f350-112">Indatavärdet till cmdlet: det objekt för ASR-nätverket som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="0f350-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f350-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f350-113">-Confirm</span></span>
<span data-ttu-id="0f350-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f350-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f350-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f350-115">-WhatIf</span></span>
<span data-ttu-id="0f350-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f350-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f350-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f350-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f350-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f350-118">CommonParameters</span></span>
<span data-ttu-id="0f350-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f350-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f350-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f350-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f350-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f350-121">INPUTS</span></span>

### <span data-ttu-id="0f350-122">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0f350-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="0f350-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f350-123">OUTPUTS</span></span>

### <span data-ttu-id="0f350-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0f350-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0f350-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f350-125">NOTES</span></span>

## <span data-ttu-id="0f350-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f350-126">RELATED LINKS</span></span>

[<span data-ttu-id="0f350-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0f350-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0f350-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0f350-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
