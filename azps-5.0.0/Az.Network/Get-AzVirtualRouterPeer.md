---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270133"
---
# <span data-ttu-id="9da51-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9da51-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="9da51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9da51-102">SYNOPSIS</span></span>
<span data-ttu-id="9da51-103">Hämtar en VirtualRouter-peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9da51-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="9da51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9da51-104">SYNTAX</span></span>

### <span data-ttu-id="9da51-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9da51-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9da51-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9da51-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9da51-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9da51-107">DESCRIPTION</span></span>
<span data-ttu-id="9da51-108">Cmdleten **Get-AzVirtualRouterPeer** får en peer i en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9da51-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="9da51-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9da51-109">EXAMPLES</span></span>

### <span data-ttu-id="9da51-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9da51-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="9da51-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9da51-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="9da51-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9da51-112">PARAMETERS</span></span>

### <span data-ttu-id="9da51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da51-113">-DefaultProfile</span></span>
<span data-ttu-id="9da51-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9da51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da51-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="9da51-115">-PeerName</span></span>
<span data-ttu-id="9da51-116">Namnet på den virtuella peer-datorn.</span><span class="sxs-lookup"><span data-stu-id="9da51-116">The name of the virtual router peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da51-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da51-117">-ResourceGroupName</span></span>
<span data-ttu-id="9da51-118">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9da51-118">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da51-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da51-119">-ResourceId</span></span>
<span data-ttu-id="9da51-120">ResourceId för den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="9da51-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da51-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="9da51-121">-VirtualRouterName</span></span>
<span data-ttu-id="9da51-122">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="9da51-122">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da51-123">CommonParameters</span></span>
<span data-ttu-id="9da51-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da51-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9da51-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da51-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9da51-126">INPUTS</span></span>

### <span data-ttu-id="9da51-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9da51-127">System.String</span></span>

## <span data-ttu-id="9da51-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9da51-128">OUTPUTS</span></span>

### <span data-ttu-id="9da51-129">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9da51-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="9da51-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9da51-130">NOTES</span></span>

## <span data-ttu-id="9da51-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9da51-131">RELATED LINKS</span></span>
