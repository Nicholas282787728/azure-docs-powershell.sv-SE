---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584572"
---
# <span data-ttu-id="a61c5-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a61c5-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="a61c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a61c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a61c5-103">Få skydds bara objekt i en system skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="a61c5-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a61c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a61c5-104">SYNTAX</span></span>

### <span data-ttu-id="a61c5-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="a61c5-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="a61c5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a61c5-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="a61c5-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a61c5-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="a61c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a61c5-108">DESCRIPTION</span></span>
<span data-ttu-id="a61c5-109">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectableItem** hämtar de objekt som skyddas i en behållare för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="a61c5-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="a61c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a61c5-110">EXAMPLES</span></span>

### <span data-ttu-id="a61c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a61c5-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="a61c5-112">Hämtar alla objekt som skyddas i angiven ASR-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="a61c5-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="a61c5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a61c5-113">PARAMETERS</span></span>

### <span data-ttu-id="a61c5-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a61c5-114">-FriendlyName</span></span>
<span data-ttu-id="a61c5-115">Anger det egna namnet på det skrivskyddade ASR-objektet.</span><span class="sxs-lookup"><span data-stu-id="a61c5-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="a61c5-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a61c5-116">-Name</span></span>
<span data-ttu-id="a61c5-117">Anger namnet på objektet som skyddas av säkerhets system.</span><span class="sxs-lookup"><span data-stu-id="a61c5-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="a61c5-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a61c5-118">-ProtectionContainer</span></span>
<span data-ttu-id="a61c5-119">Anger objekt för objektet för Azure Site Recovery-skyddet.</span><span class="sxs-lookup"><span data-stu-id="a61c5-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a61c5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61c5-120">CommonParameters</span></span>
<span data-ttu-id="a61c5-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a61c5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61c5-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a61c5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61c5-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a61c5-123">INPUTS</span></span>

### <span data-ttu-id="a61c5-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a61c5-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="a61c5-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a61c5-125">OUTPUTS</span></span>

### <span data-ttu-id="a61c5-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a61c5-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a61c5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a61c5-127">NOTES</span></span>

## <span data-ttu-id="a61c5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a61c5-128">RELATED LINKS</span></span>

[<span data-ttu-id="a61c5-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a61c5-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="a61c5-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a61c5-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
