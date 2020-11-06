---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574551"
---
# <span data-ttu-id="46551-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46551-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="46551-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46551-102">SYNOPSIS</span></span>
<span data-ttu-id="46551-103">Få information om en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="46551-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46551-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46551-104">SYNTAX</span></span>

### <span data-ttu-id="46551-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="46551-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="46551-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46551-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="46551-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="46551-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="46551-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46551-108">DESCRIPTION</span></span>
<span data-ttu-id="46551-109">Cmdleten **Get-AzureRmRecoveryServicesAsrFabric** hämtar egenskaperna för en angiven Azure Site Recovery-infrastruktur eller alla Azure Site Recovery-Fabric i ett valv för återhämtnings tjänst.</span><span class="sxs-lookup"><span data-stu-id="46551-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="46551-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46551-110">EXAMPLES</span></span>

### <span data-ttu-id="46551-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46551-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="46551-112">Returnerar alla Azure Site Recovery-Fabric i valvet.</span><span class="sxs-lookup"><span data-stu-id="46551-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="46551-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46551-113">PARAMETERS</span></span>

### <span data-ttu-id="46551-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="46551-114">-FriendlyName</span></span>
<span data-ttu-id="46551-115">Sök efter ASR-Fabric med eget namn på Fabric.</span><span class="sxs-lookup"><span data-stu-id="46551-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="46551-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="46551-116">-Name</span></span>
<span data-ttu-id="46551-117">Sök efter ASR-Fabric genom namnet på infrastruktur resursen.</span><span class="sxs-lookup"><span data-stu-id="46551-117">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="46551-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46551-118">CommonParameters</span></span>
<span data-ttu-id="46551-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46551-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46551-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46551-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46551-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46551-121">INPUTS</span></span>

### <span data-ttu-id="46551-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="46551-122">None</span></span>

## <span data-ttu-id="46551-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46551-123">OUTPUTS</span></span>

### <span data-ttu-id="46551-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46551-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="46551-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46551-125">NOTES</span></span>

## <span data-ttu-id="46551-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46551-126">RELATED LINKS</span></span>

[<span data-ttu-id="46551-127">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46551-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="46551-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46551-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
