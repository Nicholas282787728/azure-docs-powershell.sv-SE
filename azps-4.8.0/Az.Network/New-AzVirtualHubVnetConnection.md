---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262087"
---
# <span data-ttu-id="97988-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97988-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="97988-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97988-102">SYNOPSIS</span></span>
<span data-ttu-id="97988-103">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="97988-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="97988-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97988-104">SYNTAX</span></span>

### <span data-ttu-id="97988-105">ByVirtualHubNameByRemoteVirtualNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="97988-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97988-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="97988-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97988-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="97988-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97988-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="97988-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97988-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="97988-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97988-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="97988-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97988-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97988-111">DESCRIPTION</span></span>
<span data-ttu-id="97988-112">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="97988-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="97988-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97988-113">EXAMPLES</span></span>

### <span data-ttu-id="97988-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97988-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="97988-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="97988-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="97988-116">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="97988-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="97988-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="97988-117">Example 2</span></span>

<span data-ttu-id="97988-118">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="97988-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="97988-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="97988-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="97988-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97988-120">PARAMETERS</span></span>

### <span data-ttu-id="97988-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97988-121">-AsJob</span></span>
<span data-ttu-id="97988-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97988-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97988-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97988-123">-DefaultProfile</span></span>
<span data-ttu-id="97988-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97988-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97988-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="97988-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="97988-126">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="97988-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="97988-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="97988-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="97988-128">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="97988-128">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="97988-129">-Name</span></span>
<span data-ttu-id="97988-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="97988-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="97988-131">-ParentObject</span></span>
<span data-ttu-id="97988-132">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="97988-132">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97988-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="97988-133">-ParentResourceId</span></span>
<span data-ttu-id="97988-134">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="97988-134">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97988-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="97988-135">-ParentResourceName</span></span>
<span data-ttu-id="97988-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="97988-136">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97988-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="97988-138">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="97988-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="97988-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="97988-140">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="97988-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97988-141">-ResourceGroupName</span></span>
<span data-ttu-id="97988-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="97988-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="97988-143">-RoutingConfiguration</span></span>
<span data-ttu-id="97988-144">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="97988-144">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97988-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97988-145">-Confirm</span></span>
<span data-ttu-id="97988-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97988-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97988-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97988-147">-WhatIf</span></span>
<span data-ttu-id="97988-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97988-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97988-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97988-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97988-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97988-150">CommonParameters</span></span>
<span data-ttu-id="97988-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97988-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97988-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97988-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97988-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97988-153">INPUTS</span></span>

### <span data-ttu-id="97988-154">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="97988-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="97988-155">System. String</span><span class="sxs-lookup"><span data-stu-id="97988-155">System.String</span></span>

## <span data-ttu-id="97988-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97988-156">OUTPUTS</span></span>

### <span data-ttu-id="97988-157">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="97988-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="97988-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97988-158">NOTES</span></span>

## <span data-ttu-id="97988-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97988-159">RELATED LINKS</span></span>

[<span data-ttu-id="97988-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97988-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="97988-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="97988-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="97988-162">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="97988-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
