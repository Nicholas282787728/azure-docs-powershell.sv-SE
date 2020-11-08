---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271763"
---
# <span data-ttu-id="c25a7-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c25a7-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="c25a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c25a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c25a7-103">Skapar en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="c25a7-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c25a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c25a7-104">SYNTAX</span></span>

### <span data-ttu-id="c25a7-105">ByVirtualWanObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c25a7-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25a7-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c25a7-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c25a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c25a7-108">Skapar en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="c25a7-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c25a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c25a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c25a7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c25a7-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="c25a7-111">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="c25a7-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c25a7-112">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c25a7-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="c25a7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c25a7-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="c25a7-114">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="c25a7-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c25a7-115">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c25a7-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="c25a7-116">Det här exemplet liknar exempel 1, men använder ett resurs-ID för att referera till det virtuella WAN som krävs för att skapa det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="c25a7-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c25a7-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="c25a7-118">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="c25a7-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c25a7-119">Det virtuella navet har adress utrymmet "10.0.1.0/24" och en väg tabell bifogad.</span><span class="sxs-lookup"><span data-stu-id="c25a7-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="c25a7-120">Det här exemplet liknar exempel 2 men kopplar också en väg tabell till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="c25a7-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c25a7-121">PARAMETERS</span></span>

### <span data-ttu-id="c25a7-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c25a7-122">-AddressPrefix</span></span>
<span data-ttu-id="c25a7-123">Adress utrymmes strängen för det här virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="c25a7-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c25a7-124">-AsJob</span></span>
<span data-ttu-id="c25a7-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c25a7-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c25a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25a7-126">-DefaultProfile</span></span>
<span data-ttu-id="c25a7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c25a7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25a7-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c25a7-128">-HubVnetConnection</span></span>
<span data-ttu-id="c25a7-129">De virtuella hubb nätverks anslutningarna som är kopplade till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="c25a7-130">-Location</span></span>
<span data-ttu-id="c25a7-131">plats.</span><span class="sxs-lookup"><span data-stu-id="c25a7-131">location.</span></span>

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

### <span data-ttu-id="c25a7-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="c25a7-132">-Name</span></span>
<span data-ttu-id="c25a7-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c25a7-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25a7-134">-ResourceGroupName</span></span>
<span data-ttu-id="c25a7-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c25a7-135">The resource group name.</span></span>

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

### <span data-ttu-id="c25a7-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c25a7-136">-RouteTable</span></span>
<span data-ttu-id="c25a7-137">Väg tabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="c25a7-138">-Sku</span></span>
<span data-ttu-id="c25a7-139">SKU för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c25a7-140">-Tag</span></span>
<span data-ttu-id="c25a7-141">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="c25a7-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c25a7-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="c25a7-142">-VirtualWan</span></span>
<span data-ttu-id="c25a7-143">Det virtuella WAN-objekt som navet är kopplat till.</span><span class="sxs-lookup"><span data-stu-id="c25a7-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="c25a7-144">-VirtualWanId</span></span>
<span data-ttu-id="c25a7-145">ID för det virtuella WAN-objekt som navet är kopplat till.</span><span class="sxs-lookup"><span data-stu-id="c25a7-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25a7-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c25a7-146">-Confirm</span></span>
<span data-ttu-id="c25a7-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c25a7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25a7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25a7-148">-WhatIf</span></span>
<span data-ttu-id="c25a7-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c25a7-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25a7-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c25a7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25a7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25a7-151">CommonParameters</span></span>
<span data-ttu-id="c25a7-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25a7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25a7-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c25a7-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25a7-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c25a7-154">INPUTS</span></span>

### <span data-ttu-id="c25a7-155">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c25a7-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c25a7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c25a7-156">System.String</span></span>

## <span data-ttu-id="c25a7-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c25a7-157">OUTPUTS</span></span>

### <span data-ttu-id="c25a7-158">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c25a7-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c25a7-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c25a7-159">NOTES</span></span>

## <span data-ttu-id="c25a7-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c25a7-160">RELATED LINKS</span></span>

[<span data-ttu-id="c25a7-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c25a7-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="c25a7-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c25a7-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="c25a7-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c25a7-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
