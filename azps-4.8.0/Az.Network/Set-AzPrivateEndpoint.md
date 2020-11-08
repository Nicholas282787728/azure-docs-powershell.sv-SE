---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260692"
---
# <span data-ttu-id="70a3e-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="70a3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="70a3e-103">Uppdaterar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="70a3e-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="70a3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70a3e-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70a3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="70a3e-106">Cmdleten **set-AzPrivateEndpoint** uppdaterar en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="70a3e-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="70a3e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70a3e-107">EXAMPLES</span></span>

### <span data-ttu-id="70a3e-108">1: skapar en privat slut punkt och ersätter en av dess undernät med en annan</span><span class="sxs-lookup"><span data-stu-id="70a3e-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="70a3e-109">I det här exemplet skapas en privat slut punkt med ett undernät och sedan ersätts det med ett annat undernät från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="70a3e-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="70a3e-110">Set-PrivateEndpoint-cmdleten används sedan för att skriva det ändrade privata slut punkts tillståndet på tjänstens sida.</span><span class="sxs-lookup"><span data-stu-id="70a3e-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="70a3e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70a3e-111">PARAMETERS</span></span>

### <span data-ttu-id="70a3e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a3e-112">-AsJob</span></span>
<span data-ttu-id="70a3e-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="70a3e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70a3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a3e-114">-DefaultProfile</span></span>
<span data-ttu-id="70a3e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70a3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a3e-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-116">-PrivateEndpoint</span></span>
<span data-ttu-id="70a3e-117">Anger ett privat objekt som representerar tillståndet som den privata slut punkten ska anges för.</span><span class="sxs-lookup"><span data-stu-id="70a3e-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="70a3e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a3e-118">CommonParameters</span></span>
<span data-ttu-id="70a3e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a3e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a3e-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70a3e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a3e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70a3e-121">INPUTS</span></span>

### <span data-ttu-id="70a3e-122">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="70a3e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70a3e-123">OUTPUTS</span></span>

### <span data-ttu-id="70a3e-124">Microsoft. Azure. commands. Networks. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="70a3e-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70a3e-125">NOTES</span></span>

## <span data-ttu-id="70a3e-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70a3e-126">RELATED LINKS</span></span>

[<span data-ttu-id="70a3e-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="70a3e-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="70a3e-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="70a3e-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


