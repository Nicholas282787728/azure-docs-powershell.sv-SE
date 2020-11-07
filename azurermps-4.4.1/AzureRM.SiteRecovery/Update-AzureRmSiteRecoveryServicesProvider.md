---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756843"
---
# <span data-ttu-id="736b9-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="736b9-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="736b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="736b9-102">SYNOPSIS</span></span>
<span data-ttu-id="736b9-103">Uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="736b9-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="736b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="736b9-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="736b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="736b9-105">DESCRIPTION</span></span>
<span data-ttu-id="736b9-106">Cmdleten **Update-AzureRmSiteRecoveryServicesProvider** uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="736b9-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="736b9-107">Du kan använda denna cmdlet för att utlösa en uppdatering av informationen från Recovery Services-leverantören.</span><span class="sxs-lookup"><span data-stu-id="736b9-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="736b9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="736b9-108">EXAMPLES</span></span>

## <span data-ttu-id="736b9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="736b9-109">PARAMETERS</span></span>

### <span data-ttu-id="736b9-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="736b9-110">-ServicesProvider</span></span>
<span data-ttu-id="736b9-111">Anger Azure Site Recovery Services-leverantörens objekt.</span><span class="sxs-lookup"><span data-stu-id="736b9-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="736b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736b9-112">-DefaultProfile</span></span>
<span data-ttu-id="736b9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="736b9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="736b9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736b9-114">CommonParameters</span></span>
<span data-ttu-id="736b9-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736b9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736b9-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736b9-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736b9-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="736b9-117">INPUTS</span></span>

### <span data-ttu-id="736b9-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="736b9-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="736b9-119">Parametern ' ServicesProvider ' godkänner värdet av typen ' ASRRecoveryServicesProvider ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="736b9-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="736b9-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="736b9-120">OUTPUTS</span></span>

## <span data-ttu-id="736b9-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="736b9-121">NOTES</span></span>

## <span data-ttu-id="736b9-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="736b9-122">RELATED LINKS</span></span>

[<span data-ttu-id="736b9-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="736b9-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="736b9-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="736b9-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
