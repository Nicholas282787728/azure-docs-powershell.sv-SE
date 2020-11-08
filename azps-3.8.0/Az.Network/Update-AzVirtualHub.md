---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925789"
---
# <span data-ttu-id="790fd-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="790fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="790fd-102">SYNOPSIS</span></span>
<span data-ttu-id="790fd-103">Uppdaterar ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="790fd-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="790fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="790fd-104">SYNTAX</span></span>

### <span data-ttu-id="790fd-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="790fd-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="790fd-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="790fd-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="790fd-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="790fd-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="790fd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="790fd-108">DESCRIPTION</span></span>
<span data-ttu-id="790fd-109">Cmdleten **Update-AzVirtualHub** uppdaterar en virtuell hubb.</span><span class="sxs-lookup"><span data-stu-id="790fd-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="790fd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="790fd-110">EXAMPLES</span></span>

### <span data-ttu-id="790fd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="790fd-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="790fd-112">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="790fd-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="790fd-113">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="790fd-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="790fd-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="790fd-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="790fd-115">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="790fd-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="790fd-116">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="790fd-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="790fd-117">Det här exemplet liknar exempel 1 men bifogar en routningstabell till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="790fd-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="790fd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="790fd-118">PARAMETERS</span></span>

### <span data-ttu-id="790fd-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="790fd-119">-AddressPrefix</span></span>
<span data-ttu-id="790fd-120">Adress utrymmes strängen för det här virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="790fd-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="790fd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="790fd-121">-AsJob</span></span>
<span data-ttu-id="790fd-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="790fd-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="790fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790fd-123">-DefaultProfile</span></span>
<span data-ttu-id="790fd-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="790fd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="790fd-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="790fd-125">-HubVnetConnection</span></span>
<span data-ttu-id="790fd-126">De virtuella hubb nätverks anslutningarna som är kopplade till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="790fd-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="790fd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="790fd-127">-InputObject</span></span>
<span data-ttu-id="790fd-128">Det virtuella nav-objekt som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="790fd-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="790fd-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="790fd-129">-Name</span></span>
<span data-ttu-id="790fd-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="790fd-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790fd-131">-ResourceGroupName</span></span>
<span data-ttu-id="790fd-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="790fd-132">The resource group name.</span></span>

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

### <span data-ttu-id="790fd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="790fd-133">-ResourceId</span></span>
<span data-ttu-id="790fd-134">Resurs-ID för det virtuella nav som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="790fd-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="790fd-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="790fd-135">-RouteTable</span></span>
<span data-ttu-id="790fd-136">Väg tabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="790fd-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="790fd-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="790fd-137">-Sku</span></span>
<span data-ttu-id="790fd-138">SKU för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="790fd-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="790fd-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="790fd-139">-Tag</span></span>
<span data-ttu-id="790fd-140">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="790fd-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="790fd-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="790fd-141">-Confirm</span></span>
<span data-ttu-id="790fd-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="790fd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="790fd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="790fd-143">-WhatIf</span></span>
<span data-ttu-id="790fd-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="790fd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="790fd-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="790fd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="790fd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790fd-146">CommonParameters</span></span>
<span data-ttu-id="790fd-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790fd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790fd-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="790fd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790fd-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="790fd-149">INPUTS</span></span>

### <span data-ttu-id="790fd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="790fd-150">System.String</span></span>

### <span data-ttu-id="790fd-151">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="790fd-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="790fd-152">OUTPUTS</span></span>

### <span data-ttu-id="790fd-153">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="790fd-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="790fd-154">NOTES</span></span>

## <span data-ttu-id="790fd-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="790fd-155">RELATED LINKS</span></span>

[<span data-ttu-id="790fd-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="790fd-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="790fd-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="790fd-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)