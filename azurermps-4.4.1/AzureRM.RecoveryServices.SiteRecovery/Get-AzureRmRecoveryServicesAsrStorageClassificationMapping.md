---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756889"
---
# <span data-ttu-id="f5d40-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f5d40-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f5d40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5d40-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d40-103">Hämtar klassificeringar av lagrings plats för automatisk förvaring.</span><span class="sxs-lookup"><span data-stu-id="f5d40-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5d40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5d40-104">SYNTAX</span></span>

### <span data-ttu-id="f5d40-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f5d40-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="f5d40-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f5d40-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="f5d40-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5d40-107">DESCRIPTION</span></span>
<span data-ttu-id="f5d40-108">Cmdleten **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** innehåller information om en klassificerings mappning för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="f5d40-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f5d40-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5d40-109">EXAMPLES</span></span>

### <span data-ttu-id="f5d40-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5d40-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f5d40-111">Visa alla lagrings klassificerings mappningar som motsvarar den angivna lagrings klassificeringen.</span><span class="sxs-lookup"><span data-stu-id="f5d40-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f5d40-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5d40-112">PARAMETERS</span></span>

### <span data-ttu-id="f5d40-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5d40-113">-Name</span></span>
<span data-ttu-id="f5d40-114">Anger namnet på den mappning för lagrings klassificering som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f5d40-114">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d40-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="f5d40-115">-StorageClassification</span></span>
<span data-ttu-id="f5d40-116">Anger ett objekt för lagrings klassificering för ASR.</span><span class="sxs-lookup"><span data-stu-id="f5d40-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f5d40-117">Cmdleten hämtar klassificerings mappningar för automatisk lagring som motsvarar den angivna lagrings klassificeringen</span><span class="sxs-lookup"><span data-stu-id="f5d40-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="f5d40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d40-118">CommonParameters</span></span>
<span data-ttu-id="f5d40-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d40-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d40-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5d40-121">INPUTS</span></span>

### <span data-ttu-id="f5d40-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="f5d40-122">None</span></span>

## <span data-ttu-id="f5d40-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5d40-123">OUTPUTS</span></span>

### <span data-ttu-id="f5d40-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f5d40-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f5d40-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5d40-125">NOTES</span></span>

## <span data-ttu-id="f5d40-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5d40-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5d40-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f5d40-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f5d40-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f5d40-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
