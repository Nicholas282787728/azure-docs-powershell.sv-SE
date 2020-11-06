---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579359"
---
# <span data-ttu-id="c8751-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c8751-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="c8751-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8751-102">SYNOPSIS</span></span>
<span data-ttu-id="c8751-103">Tar bort en mappning av lagrings klassificering från webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="c8751-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8751-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8751-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8751-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8751-105">DESCRIPTION</span></span>
<span data-ttu-id="c8751-106">Cmdleten **Remove-AzureRmSiteRecoveryStorageClassificationMapping** tar bort en mappning av lagrings klassificering från Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c8751-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="c8751-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8751-107">EXAMPLES</span></span>

## <span data-ttu-id="c8751-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8751-108">PARAMETERS</span></span>

### <span data-ttu-id="c8751-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8751-109">-DefaultProfile</span></span>
<span data-ttu-id="c8751-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8751-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8751-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c8751-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="c8751-112">Anger en mappning för lagrings klassificering som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="c8751-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8751-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8751-113">CommonParameters</span></span>
<span data-ttu-id="c8751-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8751-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8751-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8751-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8751-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8751-116">INPUTS</span></span>

### <span data-ttu-id="c8751-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c8751-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="c8751-118">Parametern ' StorageClassificationMapping ' godkänner värdet av typen ' ASRStorageClassificationMapping ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c8751-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="c8751-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8751-119">OUTPUTS</span></span>

### <span data-ttu-id="c8751-120">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c8751-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c8751-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8751-121">NOTES</span></span>

## <span data-ttu-id="c8751-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8751-122">RELATED LINKS</span></span>

[<span data-ttu-id="c8751-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c8751-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="c8751-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c8751-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
