---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258230"
---
# <span data-ttu-id="f6f58-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f6f58-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="f6f58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6f58-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f58-103">Skapar ett VHubRoute-objekt som kan skickas som parameter till kommandot New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f6f58-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="f6f58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6f58-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6f58-105">DESCRIPTION</span></span>

<span data-ttu-id="f6f58-106">Skapar ett VHubRoute-objekt.</span><span class="sxs-lookup"><span data-stu-id="f6f58-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="f6f58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6f58-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f58-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6f58-108">Example 1</span></span>

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

<span data-ttu-id="f6f58-109">Med kommandot ovan skapas ett VHubRoute-objekt med nextHop som den angivna brand väggen som sedan kan läggas till i en VHubRouteTable-resurs.</span><span class="sxs-lookup"><span data-stu-id="f6f58-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="f6f58-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f6f58-110">Example 2</span></span>

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

<span data-ttu-id="f6f58-111">Med kommandot ovan skapas ett VHubRoute-objekt med nextHop som det angivna hubVnetConnection som sedan kan läggas till i en VHubRouteTable-resurs.</span><span class="sxs-lookup"><span data-stu-id="f6f58-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="f6f58-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6f58-112">PARAMETERS</span></span>

### <span data-ttu-id="f6f58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f58-113">-DefaultProfile</span></span>
<span data-ttu-id="f6f58-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f58-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="f6f58-115">-Destination</span></span>
<span data-ttu-id="f6f58-116">Lista med destinationer.</span><span class="sxs-lookup"><span data-stu-id="f6f58-116">List of Destinations.</span></span>

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

### <span data-ttu-id="f6f58-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="f6f58-117">-DestinationType</span></span>
<span data-ttu-id="f6f58-118">Typ av destinationer.</span><span class="sxs-lookup"><span data-stu-id="f6f58-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="f6f58-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6f58-119">-Name</span></span>
<span data-ttu-id="f6f58-120">Vägens namn.</span><span class="sxs-lookup"><span data-stu-id="f6f58-120">The route name.</span></span>

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

### <span data-ttu-id="f6f58-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="f6f58-121">-NextHop</span></span>
<span data-ttu-id="f6f58-122">Nästa hopp.</span><span class="sxs-lookup"><span data-stu-id="f6f58-122">The next hop.</span></span>

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

### <span data-ttu-id="f6f58-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f6f58-123">-NextHopType</span></span>
<span data-ttu-id="f6f58-124">Nästa hopp typ.</span><span class="sxs-lookup"><span data-stu-id="f6f58-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="f6f58-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f58-125">CommonParameters</span></span>
<span data-ttu-id="f6f58-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f58-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f58-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f58-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f58-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6f58-128">INPUTS</span></span>

### <span data-ttu-id="f6f58-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f6f58-129">System.String</span></span>

## <span data-ttu-id="f6f58-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6f58-130">OUTPUTS</span></span>

### <span data-ttu-id="f6f58-131">Microsoft. Azure. commands. Networks. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f6f58-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="f6f58-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6f58-132">NOTES</span></span>

## <span data-ttu-id="f6f58-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6f58-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6f58-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6f58-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="f6f58-135">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6f58-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="f6f58-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6f58-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="f6f58-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6f58-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)