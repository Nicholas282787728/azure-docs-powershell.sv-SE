---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758027"
---
# <span data-ttu-id="494ac-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="494ac-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="494ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="494ac-102">SYNOPSIS</span></span>
<span data-ttu-id="494ac-103">Hämtar information om nätverks mappningar för webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="494ac-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="494ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="494ac-104">SYNTAX</span></span>

### <span data-ttu-id="494ac-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="494ac-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="494ac-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="494ac-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="494ac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="494ac-107">DESCRIPTION</span></span>
<span data-ttu-id="494ac-108">Cmdleten **Get-AzureRmRecoveryServicesAsrNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="494ac-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="494ac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="494ac-109">EXAMPLES</span></span>

### <span data-ttu-id="494ac-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="494ac-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="494ac-111">Hämtar alla nätverks mappningar för det skickade nätverket.</span><span class="sxs-lookup"><span data-stu-id="494ac-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="494ac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="494ac-112">PARAMETERS</span></span>

### <span data-ttu-id="494ac-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="494ac-113">-Name</span></span>
<span data-ttu-id="494ac-114">Namnet på det objekt för automatisk nätverks mappning som ska visas.</span><span class="sxs-lookup"><span data-stu-id="494ac-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="494ac-115">-Network</span><span class="sxs-lookup"><span data-stu-id="494ac-115">-Network</span></span>
<span data-ttu-id="494ac-116">Skaffa de nätverks mappningar för automatisk återställning som motsvarar det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="494ac-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="494ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="494ac-117">CommonParameters</span></span>
<span data-ttu-id="494ac-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="494ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="494ac-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="494ac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="494ac-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="494ac-120">INPUTS</span></span>

### <span data-ttu-id="494ac-121">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="494ac-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="494ac-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="494ac-122">OUTPUTS</span></span>

### <span data-ttu-id="494ac-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="494ac-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="494ac-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="494ac-124">NOTES</span></span>

## <span data-ttu-id="494ac-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="494ac-125">RELATED LINKS</span></span>

[<span data-ttu-id="494ac-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="494ac-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="494ac-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="494ac-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)