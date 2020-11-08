---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271925"
---
# <span data-ttu-id="18a1a-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="18a1a-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="18a1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="18a1a-103">Hämtar information om ett enskilt Eventhub-kluster eller listan över kluster i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="18a1a-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="18a1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18a1a-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="18a1a-106">Listan Get-AzEventHubClustersAvailableRegion-cmdlet med regioner där det finns dedikerade att skapa.</span><span class="sxs-lookup"><span data-stu-id="18a1a-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="18a1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="18a1a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18a1a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="18a1a-109">Lista över regioner returneras var</span><span class="sxs-lookup"><span data-stu-id="18a1a-109">List of regions is returned where</span></span>

## <span data-ttu-id="18a1a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="18a1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a1a-111">-DefaultProfile</span></span>
<span data-ttu-id="18a1a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18a1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a1a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a1a-113">CommonParameters</span></span>
<span data-ttu-id="18a1a-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a1a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a1a-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a1a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a1a-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18a1a-116">INPUTS</span></span>

### <span data-ttu-id="18a1a-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="18a1a-117">None</span></span>

## <span data-ttu-id="18a1a-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18a1a-118">OUTPUTS</span></span>

### <span data-ttu-id="18a1a-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. EventHub. Models. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. cmdletar. EventHub, version = 1.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="18a1a-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="18a1a-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18a1a-120">NOTES</span></span>

## <span data-ttu-id="18a1a-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18a1a-121">RELATED LINKS</span></span>
