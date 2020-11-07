---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756874"
---
# <span data-ttu-id="bc3c2-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bc3c2-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="bc3c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3c2-103">Uppdateringar (uppdatera Server) informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc3c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc3c2-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc3c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc3c2-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3c2-106">Cmdleten **Update-AzureRmRecoveryServicesAsrServicesProvider** uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="bc3c2-107">Du kan använda denna cmdlet för att utlösa en uppdatering av informationen från Recovery Services-leverantören.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="bc3c2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc3c2-108">EXAMPLES</span></span>

### <span data-ttu-id="bc3c2-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bc3c2-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="bc3c2-110">Startar uppdateringen av informationen från den angivna ASR-leverantören och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="bc3c2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc3c2-111">PARAMETERS</span></span>

### <span data-ttu-id="bc3c2-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc3c2-112">-InputObject</span></span>
<span data-ttu-id="bc3c2-113">Input-objekt: anger det ASR Services Provider-objekt som motsvarar ASR-leverantören som identifierar den server där informationen ska uppdateras (uppdateras).</span><span class="sxs-lookup"><span data-stu-id="bc3c2-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3c2-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc3c2-114">-Confirm</span></span>
<span data-ttu-id="bc3c2-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc3c2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc3c2-116">-WhatIf</span></span>
<span data-ttu-id="bc3c2-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc3c2-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc3c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3c2-119">CommonParameters</span></span>
<span data-ttu-id="bc3c2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3c2-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc3c2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3c2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc3c2-122">INPUTS</span></span>

### <span data-ttu-id="bc3c2-123">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bc3c2-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="bc3c2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc3c2-124">OUTPUTS</span></span>

### <span data-ttu-id="bc3c2-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="bc3c2-125">System.Object</span></span>

## <span data-ttu-id="bc3c2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc3c2-126">NOTES</span></span>

## <span data-ttu-id="bc3c2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc3c2-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc3c2-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bc3c2-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="bc3c2-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bc3c2-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
