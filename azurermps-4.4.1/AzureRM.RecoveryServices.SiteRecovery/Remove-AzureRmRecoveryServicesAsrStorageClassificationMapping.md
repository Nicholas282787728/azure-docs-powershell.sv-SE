---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582259"
---
# <span data-ttu-id="ec16b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ec16b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ec16b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec16b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec16b-103">Tar bort den angivna mappningen för ASR-lagringsenheten.</span><span class="sxs-lookup"><span data-stu-id="ec16b-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec16b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec16b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec16b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec16b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec16b-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** tar bort den angivna klassificerings mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ec16b-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="ec16b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec16b-107">EXAMPLES</span></span>

### <span data-ttu-id="ec16b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec16b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="ec16b-109">Påbörjar borttagning av angiven mappning av lagrings klassificering och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ec16b-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ec16b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec16b-110">PARAMETERS</span></span>

### <span data-ttu-id="ec16b-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec16b-111">-InputObject</span></span>
<span data-ttu-id="ec16b-112">Indatavärdet till cmdleten: mappnings objekt för ASR-filklassificering som motsvarar mappnings klassificeringen för automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="ec16b-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec16b-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec16b-113">-Confirm</span></span>
<span data-ttu-id="ec16b-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec16b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec16b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec16b-115">-WhatIf</span></span>
<span data-ttu-id="ec16b-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec16b-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec16b-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec16b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec16b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec16b-118">CommonParameters</span></span>
<span data-ttu-id="ec16b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec16b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec16b-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec16b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec16b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec16b-121">INPUTS</span></span>

### <span data-ttu-id="ec16b-122">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ec16b-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ec16b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec16b-123">OUTPUTS</span></span>

### <span data-ttu-id="ec16b-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ec16b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ec16b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec16b-125">NOTES</span></span>

## <span data-ttu-id="ec16b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec16b-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec16b-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ec16b-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ec16b-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ec16b-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
