---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756890"
---
# <span data-ttu-id="d92c3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d92c3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="d92c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d92c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d92c3-103">Hämtar information om de ASR Recovery Services-leverantörer som registrerats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="d92c3-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d92c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d92c3-104">SYNTAX</span></span>

### <span data-ttu-id="d92c3-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="d92c3-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="d92c3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d92c3-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="d92c3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d92c3-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="d92c3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d92c3-108">DESCRIPTION</span></span>
<span data-ttu-id="d92c3-109">Cmdleten **Get-AzureRmRecoveryServicesAsrServicesProvider** hämtar information om Azure Site Recovery-leverantörer i valvet.</span><span class="sxs-lookup"><span data-stu-id="d92c3-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="d92c3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d92c3-110">EXAMPLES</span></span>

### <span data-ttu-id="d92c3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d92c3-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="d92c3-112">Lista alla ASR-leverantörer registrerade i det Recovery Services-valv som motsvarar den angivna Fabric-resursen.</span><span class="sxs-lookup"><span data-stu-id="d92c3-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="d92c3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d92c3-113">PARAMETERS</span></span>

### <span data-ttu-id="d92c3-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d92c3-114">-Fabric</span></span>
<span data-ttu-id="d92c3-115">Anger ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="d92c3-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="d92c3-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d92c3-116">-FriendlyName</span></span>
<span data-ttu-id="d92c3-117">Anger det egna namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="d92c3-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d92c3-118">-Name</span></span>
<span data-ttu-id="d92c3-119">Anger namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="d92c3-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92c3-120">CommonParameters</span></span>
<span data-ttu-id="d92c3-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d92c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92c3-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92c3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92c3-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d92c3-123">INPUTS</span></span>

### <span data-ttu-id="d92c3-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d92c3-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d92c3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d92c3-125">OUTPUTS</span></span>

### <span data-ttu-id="d92c3-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d92c3-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d92c3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d92c3-127">NOTES</span></span>

## <span data-ttu-id="d92c3-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d92c3-128">RELATED LINKS</span></span>

[<span data-ttu-id="d92c3-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d92c3-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="d92c3-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d92c3-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
