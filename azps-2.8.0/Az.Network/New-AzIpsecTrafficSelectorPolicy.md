---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: cbdfb990e14e995ddd5404b98a72424744170eed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918631"
---
# <span data-ttu-id="ab205-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ab205-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="ab205-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab205-102">SYNOPSIS</span></span>
<span data-ttu-id="ab205-103">Skapar en princip för trafik väljaren.</span><span class="sxs-lookup"><span data-stu-id="ab205-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="ab205-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab205-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab205-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab205-105">DESCRIPTION</span></span>
<span data-ttu-id="ab205-106">New-AzTrafficSelectorPolicy-cmdleten skapar ett princip förslag för trafik väljaren som ska användas i en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="ab205-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="ab205-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab205-107">EXAMPLES</span></span>

### <span data-ttu-id="ab205-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab205-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="ab205-109">Skapar en instans av en princip för trafik väljaren och lägger till den som en parameter när du skapar en anslutning till en virtuell nätverks-Gateway med ett IKEv2-protokoll.</span><span class="sxs-lookup"><span data-stu-id="ab205-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="ab205-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab205-110">PARAMETERS</span></span>

### <span data-ttu-id="ab205-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab205-111">-DefaultProfile</span></span>
<span data-ttu-id="ab205-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab205-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab205-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="ab205-113">-LocalAddressRange</span></span>
<span data-ttu-id="ab205-114">En samling CIDR-adressintervall</span><span class="sxs-lookup"><span data-stu-id="ab205-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="ab205-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="ab205-115">-RemoteAddressRange</span></span>
<span data-ttu-id="ab205-116">En samling CIDR-adressintervall</span><span class="sxs-lookup"><span data-stu-id="ab205-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="ab205-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab205-117">CommonParameters</span></span>
<span data-ttu-id="ab205-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab205-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab205-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab205-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab205-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab205-120">INPUTS</span></span>

### <span data-ttu-id="ab205-121">System. string []</span><span class="sxs-lookup"><span data-stu-id="ab205-121">System.String[]</span></span>

## <span data-ttu-id="ab205-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab205-122">OUTPUTS</span></span>

### <span data-ttu-id="ab205-123">Microsoft. Azure. commands. Networks. Models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ab205-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="ab205-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab205-124">NOTES</span></span>

## <span data-ttu-id="ab205-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab205-125">RELATED LINKS</span></span>
