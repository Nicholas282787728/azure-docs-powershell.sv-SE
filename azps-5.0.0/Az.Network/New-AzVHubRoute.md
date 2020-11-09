---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323688"
---
# <span data-ttu-id="6b9a9-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="6b9a9-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="6b9a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9a9-103">Skapar ett VHubRoute-objekt som kan skickas som parameter till kommandot New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="6b9a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b9a9-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b9a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b9a9-105">DESCRIPTION</span></span>

<span data-ttu-id="6b9a9-106">Skapar ett VHubRoute-objekt.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="6b9a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="6b9a9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6b9a9-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="6b9a9-109">Med kommandot ovan skapas ett VHubRoute-objekt med nextHop som den angivna brand väggen som sedan kan läggas till i en VHubRouteTable-resurs.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="6b9a9-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6b9a9-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="6b9a9-111">Med kommandot ovan skapas ett VHubRoute-objekt med nextHop som det angivna hubVnetConnection som sedan kan läggas till i en VHubRouteTable-resurs.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="6b9a9-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6b9a9-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="6b9a9-113">Ovanstående kommandon kommer att få RoutingConfiguration för en redan befintlig AzVHubRoute och sedan lägga till en statisk väg på anslutningen.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="6b9a9-114">Om du vill skapa en ny anslutning med den statiska vägen inom den kan du se exempel 1 [här.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="6b9a9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b9a9-115">PARAMETERS</span></span>

### <span data-ttu-id="6b9a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9a9-116">-DefaultProfile</span></span>
<span data-ttu-id="6b9a9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9a9-118">-Mål</span><span class="sxs-lookup"><span data-stu-id="6b9a9-118">-Destination</span></span>
<span data-ttu-id="6b9a9-119">Lista med destinationer.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-119">List of Destinations.</span></span>

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

### <span data-ttu-id="6b9a9-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="6b9a9-120">-DestinationType</span></span>
<span data-ttu-id="6b9a9-121">Typ av destinationer.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="6b9a9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b9a9-122">-Name</span></span>
<span data-ttu-id="6b9a9-123">Vägens namn.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9a9-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="6b9a9-124">-NextHop</span></span>
<span data-ttu-id="6b9a9-125">Nästa hopp.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-125">The next hop.</span></span>

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

### <span data-ttu-id="6b9a9-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6b9a9-126">-NextHopType</span></span>
<span data-ttu-id="6b9a9-127">Nästa hopp typ.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="6b9a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9a9-128">CommonParameters</span></span>
<span data-ttu-id="6b9a9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9a9-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b9a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9a9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b9a9-131">INPUTS</span></span>

### <span data-ttu-id="6b9a9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6b9a9-132">System.String</span></span>

## <span data-ttu-id="6b9a9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b9a9-133">OUTPUTS</span></span>

### <span data-ttu-id="6b9a9-134">Microsoft. Azure. commands. Networks. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="6b9a9-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="6b9a9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b9a9-135">NOTES</span></span>

## <span data-ttu-id="6b9a9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b9a9-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b9a9-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b9a9-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="6b9a9-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b9a9-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="6b9a9-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b9a9-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="6b9a9-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b9a9-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)