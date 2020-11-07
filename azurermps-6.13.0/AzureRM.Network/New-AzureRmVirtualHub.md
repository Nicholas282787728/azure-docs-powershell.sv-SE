---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756383"
---
# <span data-ttu-id="106ad-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="106ad-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="106ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="106ad-102">SYNOPSIS</span></span>
<span data-ttu-id="106ad-103">Skapar en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="106ad-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="106ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="106ad-104">SYNTAX</span></span>

### <span data-ttu-id="106ad-105">ByVirtualWanObject (standard)</span><span class="sxs-lookup"><span data-stu-id="106ad-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="106ad-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="106ad-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="106ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="106ad-107">DESCRIPTION</span></span>
<span data-ttu-id="106ad-108">Skapar en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="106ad-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="106ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="106ad-109">EXAMPLES</span></span>

### <span data-ttu-id="106ad-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="106ad-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="106ad-111">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="106ad-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="106ad-112">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="106ad-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="106ad-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="106ad-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="106ad-114">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="106ad-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="106ad-115">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="106ad-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="106ad-116">Det här exemplet liknar exempel 1, men använder ett resurs-ID för att referera till det virtuella WAN som krävs för att skapa det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="106ad-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="106ad-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="106ad-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="106ad-118">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="106ad-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="106ad-119">Det virtuella navet har adress utrymmet "10.0.1.0/24" och en väg tabell bifogad.</span><span class="sxs-lookup"><span data-stu-id="106ad-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="106ad-120">Det här exemplet liknar exempel 2 men kopplar också en väg tabell till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="106ad-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="106ad-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="106ad-121">PARAMETERS</span></span>

### <span data-ttu-id="106ad-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="106ad-122">-AddressPrefix</span></span>
<span data-ttu-id="106ad-123">Adress utrymmes strängen för det här virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="106ad-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="106ad-124">-AsJob</span></span>
<span data-ttu-id="106ad-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="106ad-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="106ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106ad-126">-DefaultProfile</span></span>
<span data-ttu-id="106ad-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="106ad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="106ad-128">-HubVnetConnection</span></span>
<span data-ttu-id="106ad-129">De virtuella hubb nätverks anslutningarna som är kopplade till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="106ad-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="106ad-130">-Location</span></span>
<span data-ttu-id="106ad-131">plats.</span><span class="sxs-lookup"><span data-stu-id="106ad-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="106ad-132">-Name</span></span>
<span data-ttu-id="106ad-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="106ad-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106ad-134">-ResourceGroupName</span></span>
<span data-ttu-id="106ad-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="106ad-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="106ad-136">-RouteTable</span></span>
<span data-ttu-id="106ad-137">Väg tabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="106ad-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="106ad-138">-Tag</span></span>
<span data-ttu-id="106ad-139">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="106ad-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="106ad-140">-VirtualWan</span></span>
<span data-ttu-id="106ad-141">Det virtuella WAN-objekt som navet är kopplat till.</span><span class="sxs-lookup"><span data-stu-id="106ad-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="106ad-142">-VirtualWanId</span></span>
<span data-ttu-id="106ad-143">ID för det virtuella WAN-objekt som navet är kopplat till.</span><span class="sxs-lookup"><span data-stu-id="106ad-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="106ad-144">-Confirm</span></span>
<span data-ttu-id="106ad-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="106ad-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106ad-146">-WhatIf</span></span>
<span data-ttu-id="106ad-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="106ad-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="106ad-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="106ad-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106ad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106ad-149">CommonParameters</span></span>
<span data-ttu-id="106ad-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106ad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106ad-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106ad-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106ad-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="106ad-152">INPUTS</span></span>

### <span data-ttu-id="106ad-153">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="106ad-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="106ad-154">System. String</span><span class="sxs-lookup"><span data-stu-id="106ad-154">System.String</span></span>

## <span data-ttu-id="106ad-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="106ad-155">OUTPUTS</span></span>

### <span data-ttu-id="106ad-156">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="106ad-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="106ad-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="106ad-157">NOTES</span></span>

## <span data-ttu-id="106ad-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="106ad-158">RELATED LINKS</span></span>
