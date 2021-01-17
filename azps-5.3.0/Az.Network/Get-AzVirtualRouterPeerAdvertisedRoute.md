---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422083"
---
# <span data-ttu-id="c9886-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="c9886-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="c9886-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9886-102">SYNOPSIS</span></span>
<span data-ttu-id="c9886-103">Visa vägar som annonseras av viss peer med virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="c9886-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="c9886-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9886-104">SYNTAX</span></span>

### <span data-ttu-id="c9886-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c9886-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9886-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9886-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9886-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9886-107">DESCRIPTION</span></span>
<span data-ttu-id="c9886-108">Med en virtuell router-peer med namn eller efter objekt räknas vägarna som annonseras till den motparten av en viss virtuell router.</span><span class="sxs-lookup"><span data-stu-id="c9886-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="c9886-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9886-109">EXAMPLES</span></span>

### <span data-ttu-id="c9886-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9886-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="c9886-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c9886-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="c9886-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9886-112">PARAMETERS</span></span>

### <span data-ttu-id="c9886-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9886-113">-AsJob</span></span>
<span data-ttu-id="c9886-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c9886-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9886-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9886-115">-DefaultProfile</span></span>
<span data-ttu-id="c9886-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9886-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9886-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9886-117">-InputObject</span></span>
<span data-ttu-id="c9886-118">Peer-indatavärdet för virtuella routrar.</span><span class="sxs-lookup"><span data-stu-id="c9886-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9886-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c9886-119">-PeerName</span></span>
<span data-ttu-id="c9886-120">Peer-namn för virtuell router</span><span class="sxs-lookup"><span data-stu-id="c9886-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="c9886-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9886-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9886-122">Namn på peer-resurs grupp för virtuell router</span><span class="sxs-lookup"><span data-stu-id="c9886-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="c9886-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c9886-123">-VirtualRouterName</span></span>
<span data-ttu-id="c9886-124">Namn på virtuell router</span><span class="sxs-lookup"><span data-stu-id="c9886-124">Virtual router name</span></span>

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

### <span data-ttu-id="c9886-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9886-125">CommonParameters</span></span>
<span data-ttu-id="c9886-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9886-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9886-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9886-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9886-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9886-128">INPUTS</span></span>

### <span data-ttu-id="c9886-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9886-129">System.String</span></span>

### <span data-ttu-id="c9886-130">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c9886-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c9886-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9886-131">OUTPUTS</span></span>

### <span data-ttu-id="c9886-132">Microsoft. Azure. commands. Networks. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="c9886-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="c9886-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9886-133">NOTES</span></span>

## <span data-ttu-id="c9886-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9886-134">RELATED LINKS</span></span>
