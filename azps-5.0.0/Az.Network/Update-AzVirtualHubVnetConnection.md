---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325127"
---
# <span data-ttu-id="6db5d-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6db5d-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="6db5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6db5d-102">SYNOPSIS</span></span>
<span data-ttu-id="6db5d-103">Uppdaterar en befintlig HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="6db5d-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="6db5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6db5d-104">SYNTAX</span></span>

### <span data-ttu-id="6db5d-105">ByHubVirtualNetworkConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="6db5d-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6db5d-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6db5d-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6db5d-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="6db5d-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db5d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6db5d-108">DESCRIPTION</span></span>
<span data-ttu-id="6db5d-109">Uppdaterar en befintlig HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="6db5d-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="6db5d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6db5d-110">EXAMPLES</span></span>

### <span data-ttu-id="6db5d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6db5d-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="6db5d-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="6db5d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="6db5d-113">En virtuell nätverks anslutning skapas också som är peer det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="6db5d-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="6db5d-114">Den här virtuella nätverks anslutningen uppdateras sedan för att aktivera Internet säkerhet.</span><span class="sxs-lookup"><span data-stu-id="6db5d-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="6db5d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6db5d-115">PARAMETERS</span></span>

### <span data-ttu-id="6db5d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6db5d-116">-AsJob</span></span>
<span data-ttu-id="6db5d-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6db5d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6db5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db5d-118">-DefaultProfile</span></span>
<span data-ttu-id="6db5d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6db5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6db5d-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="6db5d-121">Aktivera Internet säkerhet för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="6db5d-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="6db5d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db5d-122">-InputObject</span></span>
<span data-ttu-id="6db5d-123">Hubvirtualnetworkconnection-resursen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="6db5d-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6db5d-124">-Name</span></span>
<span data-ttu-id="6db5d-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="6db5d-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6db5d-126">-ParentResourceName</span></span>
<span data-ttu-id="6db5d-127">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="6db5d-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="6db5d-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6db5d-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db5d-130">-ResourceId</span></span>
<span data-ttu-id="6db5d-131">Resurs-ID för den hubvirtualnetworkconnection-resurs som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="6db5d-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6db5d-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6db5d-132">-RoutingConfiguration</span></span>
<span data-ttu-id="6db5d-133">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="6db5d-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="6db5d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6db5d-134">-Confirm</span></span>
<span data-ttu-id="6db5d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6db5d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db5d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db5d-136">-WhatIf</span></span>
<span data-ttu-id="6db5d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6db5d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db5d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6db5d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db5d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db5d-139">CommonParameters</span></span>
<span data-ttu-id="6db5d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db5d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db5d-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db5d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db5d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6db5d-142">INPUTS</span></span>

### <span data-ttu-id="6db5d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6db5d-143">System.String</span></span>

### <span data-ttu-id="6db5d-144">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="6db5d-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="6db5d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6db5d-145">OUTPUTS</span></span>

### <span data-ttu-id="6db5d-146">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="6db5d-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="6db5d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6db5d-147">NOTES</span></span>

## <span data-ttu-id="6db5d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6db5d-148">RELATED LINKS</span></span>

[<span data-ttu-id="6db5d-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6db5d-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
