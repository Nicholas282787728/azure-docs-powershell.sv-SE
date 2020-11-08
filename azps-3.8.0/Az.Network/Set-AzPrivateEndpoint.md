---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090826"
---
# <span data-ttu-id="1e0f2-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="1e0f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0f2-103">Uppdaterar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="1e0f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e0f2-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e0f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e0f2-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0f2-106">Cmdleten **set-AzPrivateEndpoint** uppdaterar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="1e0f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e0f2-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0f2-108">1: skapar en privat slut punkt och ersätter en av dess undernät med en annan</span><span class="sxs-lookup"><span data-stu-id="1e0f2-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="1e0f2-109">I det här exemplet skapas en privat slut punkt med ett undernät och sedan ersätts det med ett annat undernät från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1e0f2-110">Set-PrivateEndpoint-cmdleten används sedan för att skriva det ändrade privata slut punkts tillståndet på tjänstens sida.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="1e0f2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e0f2-111">PARAMETERS</span></span>

### <span data-ttu-id="1e0f2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e0f2-112">-AsJob</span></span>
<span data-ttu-id="1e0f2-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1e0f2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e0f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0f2-114">-DefaultProfile</span></span>
<span data-ttu-id="1e0f2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e0f2-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-116">-PrivateEndpoint</span></span>
<span data-ttu-id="1e0f2-117">Anger ett privat objekt som representerar tillståndet som den privata slut punkten ska anges för.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0f2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0f2-118">CommonParameters</span></span>
<span data-ttu-id="1e0f2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0f2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0f2-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e0f2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0f2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e0f2-121">INPUTS</span></span>

### <span data-ttu-id="1e0f2-122">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="1e0f2-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e0f2-123">OUTPUTS</span></span>

### <span data-ttu-id="1e0f2-124">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="1e0f2-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e0f2-125">NOTES</span></span>

## <span data-ttu-id="1e0f2-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e0f2-126">RELATED LINKS</span></span>

[<span data-ttu-id="1e0f2-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="1e0f2-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="1e0f2-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e0f2-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


