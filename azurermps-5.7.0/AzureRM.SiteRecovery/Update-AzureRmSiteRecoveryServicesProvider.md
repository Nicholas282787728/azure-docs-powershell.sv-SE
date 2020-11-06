---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580968"
---
# <span data-ttu-id="a5141-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a5141-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="a5141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5141-102">SYNOPSIS</span></span>
<span data-ttu-id="a5141-103">Uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5141-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5141-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5141-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5141-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5141-105">DESCRIPTION</span></span>
<span data-ttu-id="a5141-106">Cmdleten **Update-AzureRmSiteRecoveryServicesProvider** uppdaterar informationen från Azure Site Recovery Services-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5141-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="a5141-107">Du kan använda denna cmdlet för att utlösa en uppdatering av informationen från Recovery Services-leverantören.</span><span class="sxs-lookup"><span data-stu-id="a5141-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="a5141-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5141-108">EXAMPLES</span></span>

## <span data-ttu-id="a5141-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5141-109">PARAMETERS</span></span>

### <span data-ttu-id="a5141-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5141-110">-DefaultProfile</span></span>
<span data-ttu-id="a5141-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5141-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5141-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a5141-112">-ServicesProvider</span></span>
<span data-ttu-id="a5141-113">Anger Azure Site Recovery Services-leverantörens objekt.</span><span class="sxs-lookup"><span data-stu-id="a5141-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5141-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5141-114">CommonParameters</span></span>
<span data-ttu-id="a5141-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5141-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5141-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5141-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5141-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5141-117">INPUTS</span></span>

### <span data-ttu-id="a5141-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a5141-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="a5141-119">Parametern ' ServicesProvider ' godkänner värdet av typen ' ASRRecoveryServicesProvider ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a5141-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="a5141-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5141-120">OUTPUTS</span></span>

## <span data-ttu-id="a5141-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5141-121">NOTES</span></span>

## <span data-ttu-id="a5141-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5141-122">RELATED LINKS</span></span>

[<span data-ttu-id="a5141-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a5141-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="a5141-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a5141-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
