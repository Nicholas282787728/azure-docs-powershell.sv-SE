---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323729"
---
# <span data-ttu-id="acf2e-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf2e-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="acf2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="acf2e-103">Skapar ett RoutingConfiguration-objekt.</span><span class="sxs-lookup"><span data-stu-id="acf2e-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="acf2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acf2e-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="acf2e-106">Skapar ett RoutingConfiguration-objekt.</span><span class="sxs-lookup"><span data-stu-id="acf2e-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="acf2e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acf2e-107">EXAMPLES</span></span>

### <span data-ttu-id="acf2e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="acf2e-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="acf2e-109">Med kommandot ovan skapas ett RoutingConfiguration-objekt som sedan kan läggas till i en anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="acf2e-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="acf2e-110">Statiska vägar är bara tillåtna med ett HubVirtualNetworkConnection-objekt.</span><span class="sxs-lookup"><span data-stu-id="acf2e-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="acf2e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acf2e-111">PARAMETERS</span></span>

### <span data-ttu-id="acf2e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf2e-112">-DefaultProfile</span></span>
<span data-ttu-id="acf2e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acf2e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf2e-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="acf2e-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="acf2e-115">NAV flödes tabellen som är kopplad till denna Dirigerings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="acf2e-115">The hub route table associated with this routing configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf2e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="acf2e-116">-Id</span></span>
<span data-ttu-id="acf2e-117">Listan med resurs-ID: n för alla nav-vägfilter för att annonsera vägarna till egenskapen PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="acf2e-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf2e-118">-Etikett</span><span class="sxs-lookup"><span data-stu-id="acf2e-118">-Label</span></span>
<span data-ttu-id="acf2e-119">Listan med etiketter för egenskapen PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="acf2e-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf2e-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="acf2e-120">-StaticRoute</span></span>
<span data-ttu-id="acf2e-121">Lista över vägar som styr routning från VirtualHub till en virtuell nätverks anslutning.</span><span class="sxs-lookup"><span data-stu-id="acf2e-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf2e-122">CommonParameters</span></span>
<span data-ttu-id="acf2e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf2e-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acf2e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf2e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acf2e-125">INPUTS</span></span>

### <span data-ttu-id="acf2e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="acf2e-126">System.String</span></span>

### <span data-ttu-id="acf2e-127">Microsoft. Azure. commands. Networks. Models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="acf2e-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="acf2e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acf2e-128">OUTPUTS</span></span>

### <span data-ttu-id="acf2e-129">Microsoft. Azure. commands. Networks. Models. PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="acf2e-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="acf2e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acf2e-130">NOTES</span></span>

## <span data-ttu-id="acf2e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acf2e-131">RELATED LINKS</span></span>

[<span data-ttu-id="acf2e-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="acf2e-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="acf2e-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="acf2e-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="acf2e-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="acf2e-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="acf2e-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="acf2e-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="acf2e-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="acf2e-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="acf2e-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="acf2e-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="acf2e-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)