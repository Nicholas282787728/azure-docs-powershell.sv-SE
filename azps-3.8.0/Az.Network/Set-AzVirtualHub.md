---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928046"
---
# <span data-ttu-id="17c8c-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17c8c-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="17c8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="17c8c-103">Ändrar ett virtuellt nav för att lägga till en virtuell hubb till det.</span><span class="sxs-lookup"><span data-stu-id="17c8c-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="17c8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17c8c-104">SYNTAX</span></span>

### <span data-ttu-id="17c8c-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="17c8c-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17c8c-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="17c8c-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17c8c-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="17c8c-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17c8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17c8c-108">DESCRIPTION</span></span>
<span data-ttu-id="17c8c-109">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="17c8c-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="17c8c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="17c8c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17c8c-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="17c8c-112">Först skapar vi ett objekt för virtuell hubb och använder det för att skapa en tabell resurs för virtuell hubb.</span><span class="sxs-lookup"><span data-stu-id="17c8c-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="17c8c-113">Därefter angav vi den här väg tabell resursen till det virtuella navet med kommandot Set-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="17c8c-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="17c8c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17c8c-114">PARAMETERS</span></span>

### <span data-ttu-id="17c8c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17c8c-115">-AsJob</span></span>
<span data-ttu-id="17c8c-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="17c8c-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c8c-117">-DefaultProfile</span></span>
<span data-ttu-id="17c8c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17c8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17c8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17c8c-119">-InputObject</span></span>
<span data-ttu-id="17c8c-120">Det virtuella nav-objekt som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="17c8c-120">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="17c8c-121">-Name</span></span>
<span data-ttu-id="17c8c-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="17c8c-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="17c8c-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="17c8c-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17c8c-125">-ResourceId</span></span>
<span data-ttu-id="17c8c-126">Resurs-ID för det virtuella nav som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="17c8c-126">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="17c8c-127">-RouteTable</span></span>
<span data-ttu-id="17c8c-128">De väg tabeller som är kopplade till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="17c8c-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="17c8c-129">-Tag</span></span>
<span data-ttu-id="17c8c-130">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="17c8c-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17c8c-131">-Confirm</span></span>
<span data-ttu-id="17c8c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17c8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17c8c-133">-WhatIf</span></span>
<span data-ttu-id="17c8c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17c8c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17c8c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17c8c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c8c-136">CommonParameters</span></span>
<span data-ttu-id="17c8c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c8c-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17c8c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c8c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17c8c-139">INPUTS</span></span>

### <span data-ttu-id="17c8c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="17c8c-140">System.String</span></span>

### <span data-ttu-id="17c8c-141">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17c8c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="17c8c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17c8c-142">OUTPUTS</span></span>

### <span data-ttu-id="17c8c-143">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17c8c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="17c8c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17c8c-144">NOTES</span></span>

## <span data-ttu-id="17c8c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17c8c-145">RELATED LINKS</span></span>
