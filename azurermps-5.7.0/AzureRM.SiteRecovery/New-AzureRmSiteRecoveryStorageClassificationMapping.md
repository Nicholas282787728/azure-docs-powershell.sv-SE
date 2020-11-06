---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575490"
---
# <span data-ttu-id="3ce0b-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3ce0b-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="3ce0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ce0b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce0b-103">Skapar en mappning för lagrings klassificering i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ce0b-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ce0b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce0b-106">Cmdleten **New-AzureRmSiteRecoveryStorageClassificationMapping** skapar en mappning för lagrings klassificering i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="3ce0b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ce0b-107">EXAMPLES</span></span>

## <span data-ttu-id="3ce0b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ce0b-108">PARAMETERS</span></span>

### <span data-ttu-id="3ce0b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce0b-109">-DefaultProfile</span></span>
<span data-ttu-id="3ce0b-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ce0b-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ce0b-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0b-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="3ce0b-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="3ce0b-113">Anger primär mappning för lagrings klassificering.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0b-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="3ce0b-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="3ce0b-115">Anger en klassificerings mappning för en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce0b-116">CommonParameters</span></span>
<span data-ttu-id="3ce0b-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce0b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce0b-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce0b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce0b-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ce0b-119">INPUTS</span></span>

### <span data-ttu-id="3ce0b-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="3ce0b-120">ASRStorageClassification</span></span>
<span data-ttu-id="3ce0b-121">Parametern ' PrimaryStorageClassification ' godkänner värdet av typen ' ASRStorageClassification ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3ce0b-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="3ce0b-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ce0b-122">OUTPUTS</span></span>

### <span data-ttu-id="3ce0b-123">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3ce0b-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3ce0b-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ce0b-124">NOTES</span></span>

## <span data-ttu-id="3ce0b-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ce0b-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ce0b-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3ce0b-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="3ce0b-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3ce0b-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
