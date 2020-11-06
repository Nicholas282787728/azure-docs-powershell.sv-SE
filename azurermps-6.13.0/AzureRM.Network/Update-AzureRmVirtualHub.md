---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
ms.openlocfilehash: 188d449e47155739b4bc532c12b0e9193781c7c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578839"
---
# <span data-ttu-id="8a4c1-101">Update-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8a4c1-101">Update-AzureRmVirtualHub</span></span>

## <span data-ttu-id="8a4c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4c1-103">Uppdaterar ett virtuellt nav till ett avsett mål tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-103">Updates a Virtual Hub to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a4c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a4c1-104">SYNTAX</span></span>

### <span data-ttu-id="8a4c1-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="8a4c1-105">ByVirtualHubName (Default)</span></span>
```
Update-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4c1-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4c1-106">ByVirtualHubResourceId</span></span>
```
Update-AzureRmVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4c1-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8a4c1-107">ByVirtualHubObject</span></span>
```
Update-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a4c1-108">DESCRIPTION</span></span>
<span data-ttu-id="8a4c1-109">Uppdaterar ett virtuellt nav till ett avsett mål tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-109">Updates a Virtual Hub to an intended goal state.</span></span>

## <span data-ttu-id="8a4c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a4c1-110">EXAMPLES</span></span>

### <span data-ttu-id="8a4c1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a4c1-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="8a4c1-112">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="8a4c1-113">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="8a4c1-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="8a4c1-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8a4c1-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="8a4c1-115">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="8a4c1-116">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="8a4c1-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="8a4c1-117">Det här exemplet liknar exempel 1 men bifogar en routningstabell till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="8a4c1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a4c1-118">PARAMETERS</span></span>

### <span data-ttu-id="8a4c1-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8a4c1-119">-AddressPrefix</span></span>
<span data-ttu-id="8a4c1-120">Adress utrymmes strängen för det här virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a4c1-121">-AsJob</span></span>
<span data-ttu-id="8a4c1-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8a4c1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a4c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4c1-123">-DefaultProfile</span></span>
<span data-ttu-id="8a4c1-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4c1-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8a4c1-125">-HubVnetConnection</span></span>
<span data-ttu-id="8a4c1-126">De virtuella hubb nätverks anslutningarna som är kopplade till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="8a4c1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4c1-127">-InputObject</span></span>
<span data-ttu-id="8a4c1-128">Det virtuella nav-objekt som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c1-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a4c1-129">-Name</span></span>
<span data-ttu-id="8a4c1-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4c1-131">-ResourceGroupName</span></span>
<span data-ttu-id="8a4c1-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4c1-133">-ResourceId</span></span>
<span data-ttu-id="8a4c1-134">Resurs-ID för det virtuella nav som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c1-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8a4c1-135">-RouteTable</span></span>
<span data-ttu-id="8a4c1-136">Väg tabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="8a4c1-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8a4c1-137">-Tag</span></span>
<span data-ttu-id="8a4c1-138">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8a4c1-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a4c1-139">-Confirm</span></span>
<span data-ttu-id="8a4c1-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4c1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4c1-141">-WhatIf</span></span>
<span data-ttu-id="8a4c1-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4c1-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4c1-144">CommonParameters</span></span>
<span data-ttu-id="8a4c1-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4c1-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4c1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4c1-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a4c1-147">INPUTS</span></span>

### <span data-ttu-id="8a4c1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4c1-148">System.String</span></span>

### <span data-ttu-id="8a4c1-149">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8a4c1-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8a4c1-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a4c1-150">OUTPUTS</span></span>

### <span data-ttu-id="8a4c1-151">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8a4c1-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8a4c1-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a4c1-152">NOTES</span></span>

## <span data-ttu-id="8a4c1-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a4c1-153">RELATED LINKS</span></span>
