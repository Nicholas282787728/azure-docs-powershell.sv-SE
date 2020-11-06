---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584563"
---
# <span data-ttu-id="c964d-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c964d-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="c964d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c964d-102">SYNOPSIS</span></span>
<span data-ttu-id="c964d-103">Hämtar de tillgängliga (upptäckta) ASR-säkerhetsfunktionerna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c964d-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c964d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c964d-104">SYNTAX</span></span>

### <span data-ttu-id="c964d-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c964d-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="c964d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c964d-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="c964d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c964d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="c964d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c964d-108">DESCRIPTION</span></span>
<span data-ttu-id="c964d-109">Cmdleten **Get-AzureRmRecoveryServicesAsrStorageClassification** hämtar information om de UPPTÄCKta ASR-lagrings klassificeringarna i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c964d-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="c964d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c964d-110">EXAMPLES</span></span>

### <span data-ttu-id="c964d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c964d-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="c964d-112">Lista över upptäckta lagrings klassificeringar som motsvarar den angivna ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="c964d-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="c964d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c964d-113">PARAMETERS</span></span>

### <span data-ttu-id="c964d-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c964d-114">-Fabric</span></span>
<span data-ttu-id="c964d-115">Anger ett ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="c964d-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="c964d-116">Cmdleten får information om upptäckta lagrings klassificeringar motsvarande den angivna ASR Fabric.</span><span class="sxs-lookup"><span data-stu-id="c964d-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c964d-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c964d-117">-FriendlyName</span></span>
<span data-ttu-id="c964d-118">Anger det egna namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c964d-118">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c964d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c964d-119">-Name</span></span>
<span data-ttu-id="c964d-120">Anger namnet på det lagrings klassificerings objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c964d-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="c964d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c964d-121">CommonParameters</span></span>
<span data-ttu-id="c964d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c964d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c964d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c964d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c964d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c964d-124">INPUTS</span></span>

### <span data-ttu-id="c964d-125">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c964d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c964d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c964d-126">OUTPUTS</span></span>

### <span data-ttu-id="c964d-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c964d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c964d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c964d-128">NOTES</span></span>

## <span data-ttu-id="c964d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c964d-129">RELATED LINKS</span></span>

