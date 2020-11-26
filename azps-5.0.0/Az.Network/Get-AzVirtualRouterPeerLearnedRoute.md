---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270131"
---
# <span data-ttu-id="b24b6-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="b24b6-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="b24b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b24b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b24b6-103">Lista över vägar som upptäckts av en viss peer med virtuella routrar</span><span class="sxs-lookup"><span data-stu-id="b24b6-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="b24b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b24b6-104">SYNTAX</span></span>

### <span data-ttu-id="b24b6-105">VirtualRouterPeerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b24b6-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b24b6-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24b6-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b24b6-107">DESCRIPTION</span></span>
<span data-ttu-id="b24b6-108">Räkna upp vägar som lärts av en virtuell router-peer från andra källor.</span><span class="sxs-lookup"><span data-stu-id="b24b6-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="b24b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b24b6-109">EXAMPLES</span></span>

### <span data-ttu-id="b24b6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b24b6-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="b24b6-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b24b6-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="b24b6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b24b6-112">PARAMETERS</span></span>

### <span data-ttu-id="b24b6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b24b6-113">-AsJob</span></span>
<span data-ttu-id="b24b6-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b24b6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b24b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24b6-115">-DefaultProfile</span></span>
<span data-ttu-id="b24b6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b24b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b24b6-117">-InputObject</span></span>
<span data-ttu-id="b24b6-118">Peer-indatavärdet för virtuella routrar.</span><span class="sxs-lookup"><span data-stu-id="b24b6-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="b24b6-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="b24b6-119">-PeerName</span></span>
<span data-ttu-id="b24b6-120">Peer-namn för virtuell router</span><span class="sxs-lookup"><span data-stu-id="b24b6-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="b24b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="b24b6-122">Namn på peer-resurs grupp för virtuell router</span><span class="sxs-lookup"><span data-stu-id="b24b6-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="b24b6-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="b24b6-123">-VirtualRouterName</span></span>
<span data-ttu-id="b24b6-124">Namn på virtuell router</span><span class="sxs-lookup"><span data-stu-id="b24b6-124">Virtual router name</span></span>

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

### <span data-ttu-id="b24b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24b6-125">CommonParameters</span></span>
<span data-ttu-id="b24b6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24b6-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b24b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24b6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b24b6-128">INPUTS</span></span>

### <span data-ttu-id="b24b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b24b6-129">System.String</span></span>

### <span data-ttu-id="b24b6-130">Microsoft. Azure. commands. Networks. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="b24b6-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="b24b6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b24b6-131">OUTPUTS</span></span>

### <span data-ttu-id="b24b6-132">Microsoft. Azure. commands. Networks. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="b24b6-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="b24b6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b24b6-133">NOTES</span></span>

## <span data-ttu-id="b24b6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b24b6-134">RELATED LINKS</span></span>