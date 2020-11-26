---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259294"
---
# <span data-ttu-id="73819-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="73819-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="73819-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73819-102">SYNOPSIS</span></span>
<span data-ttu-id="73819-103">Skapar en princip för trafik väljaren.</span><span class="sxs-lookup"><span data-stu-id="73819-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="73819-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73819-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73819-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73819-105">DESCRIPTION</span></span>
<span data-ttu-id="73819-106">New-AzTrafficSelectorPolicy-cmdleten skapar ett princip förslag för trafik väljaren som ska användas i en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="73819-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="73819-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73819-107">EXAMPLES</span></span>

### <span data-ttu-id="73819-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73819-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="73819-109">Skapar en instans av en princip för trafik väljaren och lägger till den som en parameter när du skapar en anslutning till en virtuell nätverks-Gateway med ett IKEv2-protokoll.</span><span class="sxs-lookup"><span data-stu-id="73819-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="73819-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73819-110">PARAMETERS</span></span>

### <span data-ttu-id="73819-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73819-111">-DefaultProfile</span></span>
<span data-ttu-id="73819-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73819-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73819-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="73819-113">-LocalAddressRange</span></span>
<span data-ttu-id="73819-114">En samling CIDR-adressintervall</span><span class="sxs-lookup"><span data-stu-id="73819-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73819-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="73819-115">-RemoteAddressRange</span></span>
<span data-ttu-id="73819-116">En samling CIDR-adressintervall</span><span class="sxs-lookup"><span data-stu-id="73819-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73819-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73819-117">CommonParameters</span></span>
<span data-ttu-id="73819-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73819-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73819-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73819-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73819-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73819-120">INPUTS</span></span>

### <span data-ttu-id="73819-121">System. string []</span><span class="sxs-lookup"><span data-stu-id="73819-121">System.String[]</span></span>

## <span data-ttu-id="73819-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73819-122">OUTPUTS</span></span>

### <span data-ttu-id="73819-123">Microsoft. Azure. commands. Networks. Models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="73819-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="73819-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73819-124">NOTES</span></span>

## <span data-ttu-id="73819-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73819-125">RELATED LINKS</span></span>