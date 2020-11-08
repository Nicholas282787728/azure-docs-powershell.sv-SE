---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102028"
---
# <span data-ttu-id="c3030-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c3030-101">Get-AzPeering</span></span>

## <span data-ttu-id="c3030-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3030-102">SYNOPSIS</span></span>
<span data-ttu-id="c3030-103">Hämtar peering-resurserna för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c3030-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="c3030-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3030-104">SYNTAX</span></span>

### <span data-ttu-id="c3030-105">BySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="c3030-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3030-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c3030-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3030-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3030-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3030-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3030-108">DESCRIPTION</span></span>
<span data-ttu-id="c3030-109">Hämtar Peerer från ett abonnemang, en resurs grupp eller efter namn.</span><span class="sxs-lookup"><span data-stu-id="c3030-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="c3030-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3030-110">EXAMPLES</span></span>

### <span data-ttu-id="c3030-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3030-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="c3030-112">Hämtar alla resurser för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c3030-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="c3030-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c3030-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="c3030-114">Hämtar Exchange-peering med namnet `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="c3030-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="c3030-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c3030-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="c3030-116">Hämtar Exchange-peering `myExchangePeering1` baserat på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c3030-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="c3030-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3030-117">PARAMETERS</span></span>

### <span data-ttu-id="c3030-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3030-118">-DefaultProfile</span></span>
<span data-ttu-id="c3030-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3030-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3030-120">-Sort</span><span class="sxs-lookup"><span data-stu-id="c3030-120">-Kind</span></span>
<span data-ttu-id="c3030-121">Visar alla peering-resurser av typen.</span><span class="sxs-lookup"><span data-stu-id="c3030-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3030-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3030-122">-Name</span></span>
<span data-ttu-id="c3030-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c3030-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3030-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3030-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3030-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c3030-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3030-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3030-126">-ResourceId</span></span>
<span data-ttu-id="c3030-127">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c3030-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3030-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3030-128">CommonParameters</span></span>
<span data-ttu-id="c3030-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3030-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3030-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3030-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3030-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3030-131">INPUTS</span></span>

### <span data-ttu-id="c3030-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c3030-132">System.String</span></span>

## <span data-ttu-id="c3030-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3030-133">OUTPUTS</span></span>

### <span data-ttu-id="c3030-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c3030-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="c3030-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3030-135">NOTES</span></span>

## <span data-ttu-id="c3030-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3030-136">RELATED LINKS</span></span>
