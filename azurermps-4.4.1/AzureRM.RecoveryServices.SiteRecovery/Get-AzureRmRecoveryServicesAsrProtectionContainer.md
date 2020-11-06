---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585372"
---
# <span data-ttu-id="70375-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="70375-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="70375-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70375-102">SYNOPSIS</span></span>
<span data-ttu-id="70375-103">Får ASR-skydds behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="70375-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70375-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70375-104">SYNTAX</span></span>

### <span data-ttu-id="70375-105">ByFabricObject (standard)</span><span class="sxs-lookup"><span data-stu-id="70375-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="70375-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="70375-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="70375-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="70375-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="70375-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70375-108">DESCRIPTION</span></span>
<span data-ttu-id="70375-109">Cmdleten **Get-AzureRmRecoveryServicesAsrProtectionContainer** får Azure Site Recovery-behållare i Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="70375-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="70375-110">En skydds behållare är en logisk behållare för skydd bara (upptäckta) och skyddade objekt, till exempel virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="70375-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="70375-111">Replikeringsprinciper definierar replikeringsinställningar för skyddade objekt och kan associeras med en skydds behållare och tillämpas på ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="70375-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="70375-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70375-112">EXAMPLES</span></span>

### <span data-ttu-id="70375-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70375-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="70375-114">Hämtar alla systemladdade system för automatisk system återställning i den angivna ASR-fabricen (pipelinen i ovanstående exempel.)</span><span class="sxs-lookup"><span data-stu-id="70375-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="70375-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70375-115">PARAMETERS</span></span>

### <span data-ttu-id="70375-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="70375-116">-Fabric</span></span>
<span data-ttu-id="70375-117">Leta efter skydds behållaren i den angivna ASR-fabricen.</span><span class="sxs-lookup"><span data-stu-id="70375-117">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="70375-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="70375-118">-FriendlyName</span></span>
<span data-ttu-id="70375-119">Anger det egna namnet på den systemsystem för ASR-skydd som du letar efter.</span><span class="sxs-lookup"><span data-stu-id="70375-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="70375-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="70375-120">-Name</span></span>
<span data-ttu-id="70375-121">Anger namnet på den behållare för automatisk system återställning som ska sökas efter.</span><span class="sxs-lookup"><span data-stu-id="70375-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="70375-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70375-122">CommonParameters</span></span>
<span data-ttu-id="70375-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70375-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70375-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70375-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70375-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70375-125">INPUTS</span></span>

### <span data-ttu-id="70375-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="70375-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="70375-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70375-127">OUTPUTS</span></span>

### <span data-ttu-id="70375-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70375-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="70375-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70375-129">NOTES</span></span>

## <span data-ttu-id="70375-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70375-130">RELATED LINKS</span></span>

