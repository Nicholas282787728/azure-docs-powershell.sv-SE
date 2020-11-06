---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584567"
---
# <span data-ttu-id="e3dfe-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e3dfe-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="e3dfe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="e3dfe-103">Hämtar mappningar för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3dfe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3dfe-104">SYNTAX</span></span>

### <span data-ttu-id="e3dfe-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e3dfe-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="e3dfe-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e3dfe-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="e3dfe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3dfe-107">DESCRIPTION</span></span>
<span data-ttu-id="e3dfe-108">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** hämtar information om skydds behållaren för att mappa (associeringar) i valvet för den angivna ASR-skyddsagenten.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="e3dfe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3dfe-109">EXAMPLES</span></span>

### <span data-ttu-id="e3dfe-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3dfe-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="e3dfe-111">Hämtar alla skydds behållas mappningar för den angivna skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="e3dfe-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3dfe-112">PARAMETERS</span></span>

### <span data-ttu-id="e3dfe-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3dfe-113">-Name</span></span>
<span data-ttu-id="e3dfe-114">Anger namnet på den mappning för skydds behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="e3dfe-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e3dfe-115">-ProtectionContainer</span></span>
<span data-ttu-id="e3dfe-116">Hämta mappningar för skydds behållare för det angivna objektet för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="e3dfe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3dfe-117">CommonParameters</span></span>
<span data-ttu-id="e3dfe-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3dfe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3dfe-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3dfe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3dfe-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3dfe-120">INPUTS</span></span>

### <span data-ttu-id="e3dfe-121">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e3dfe-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="e3dfe-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3dfe-122">OUTPUTS</span></span>

### <span data-ttu-id="e3dfe-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3dfe-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3dfe-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3dfe-124">NOTES</span></span>

## <span data-ttu-id="e3dfe-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3dfe-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3dfe-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e3dfe-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="e3dfe-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e3dfe-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
