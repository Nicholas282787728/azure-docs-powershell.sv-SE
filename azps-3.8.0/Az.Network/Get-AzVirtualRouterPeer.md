---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089088"
---
# <span data-ttu-id="a27b6-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a27b6-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="a27b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a27b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a27b6-103">Hämtar en VirtualRouter-peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a27b6-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="a27b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a27b6-104">SYNTAX</span></span>

### <span data-ttu-id="a27b6-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a27b6-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27b6-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a27b6-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a27b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a27b6-107">DESCRIPTION</span></span>
<span data-ttu-id="a27b6-108">Cmdleten **Get-AzVirtualRouterPeer** får en peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a27b6-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="a27b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a27b6-109">EXAMPLES</span></span>

### <span data-ttu-id="a27b6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a27b6-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="a27b6-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a27b6-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="a27b6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a27b6-112">PARAMETERS</span></span>

### <span data-ttu-id="a27b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27b6-113">-DefaultProfile</span></span>
<span data-ttu-id="a27b6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a27b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="a27b6-115">-PeerName</span></span>
<span data-ttu-id="a27b6-116">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="a27b6-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="a27b6-118">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a27b6-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a27b6-119">-ResourceId</span></span>
<span data-ttu-id="a27b6-120">ResourceId för den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="a27b6-120">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="a27b6-121">-VirtualRouterName</span></span>
<span data-ttu-id="a27b6-122">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="a27b6-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27b6-123">CommonParameters</span></span>
<span data-ttu-id="a27b6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27b6-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a27b6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27b6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a27b6-126">INPUTS</span></span>

### <span data-ttu-id="a27b6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a27b6-127">System.String</span></span>

## <span data-ttu-id="a27b6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a27b6-128">OUTPUTS</span></span>

### <span data-ttu-id="a27b6-129">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="a27b6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="a27b6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a27b6-130">NOTES</span></span>

## <span data-ttu-id="a27b6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a27b6-131">RELATED LINKS</span></span>
