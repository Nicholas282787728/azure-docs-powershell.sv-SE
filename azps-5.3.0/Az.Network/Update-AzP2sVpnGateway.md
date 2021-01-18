---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 682f6bdb8eb0ce80d4b81dc12b9ed8d09de4713a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521808"
---
# <span data-ttu-id="4da4d-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4da4d-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="4da4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4da4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4da4d-103">Uppdatera en befintlig P2SVpnGateway under VirtualHub för webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="4da4d-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="4da4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4da4d-104">SYNTAX</span></span>

### <span data-ttu-id="4da4d-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="4da4d-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4da4d-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4da4d-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4da4d-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="4da4d-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4da4d-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4da4d-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="4da4d-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4da4d-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da4d-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="4da4d-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da4d-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4da4d-114">DESCRIPTION</span></span>
<span data-ttu-id="4da4d-115">Med cmdleten **Update-AzP2sVpnGateway** kan du uppdatera en befintlig P2SVpnGateway under VirtualHub med ny VpnClientAddressPool eller ny VpnServerConfiguration eller ändring av VpnGatewayScaleUnit.</span><span class="sxs-lookup"><span data-stu-id="4da4d-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="4da4d-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4da4d-116">EXAMPLES</span></span>

### <span data-ttu-id="4da4d-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4da4d-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,                                 
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="4da4d-118">Med cmdleten **Update-AzP2sVpnGateway** kan du uppdatera en befintlig P2SVpnGateway under VirtualHub med nya VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="4da4d-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="4da4d-119">När peka på webbplats klient ansluter med den här P2SVpnGateway tilldelas en av IP-adresserna från den här VpnClientAddressPool till klienten.</span><span class="sxs-lookup"><span data-stu-id="4da4d-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="4da4d-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4da4d-120">Example 2</span></span>

<span data-ttu-id="4da4d-121">Uppdatera en befintlig P2SVpnGateway under VirtualHub för webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="4da4d-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="4da4d-122">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="4da4d-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="4da4d-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4da4d-123">PARAMETERS</span></span>

### <span data-ttu-id="4da4d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4da4d-124">-AsJob</span></span>
<span data-ttu-id="4da4d-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4da4d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4da4d-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="4da4d-126">-CustomDnsServer</span></span>
<span data-ttu-id="4da4d-127">Listan med anpassade DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="4da4d-127">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da4d-128">-DefaultProfile</span></span>
<span data-ttu-id="4da4d-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4da4d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4da4d-130">-InputObject</span></span>
<span data-ttu-id="4da4d-131">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="4da4d-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="4da4d-132">-Name</span></span>
<span data-ttu-id="4da4d-133">P2S VPN gateway-namn.</span><span class="sxs-lookup"><span data-stu-id="4da4d-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da4d-134">-ResourceGroupName</span></span>
<span data-ttu-id="4da4d-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4da4d-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4da4d-136">-ResourceId</span></span>
<span data-ttu-id="4da4d-137">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="4da4d-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="4da4d-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="4da4d-139">Aktivera Internet säkerhets flaggan för dessa P2SVpnGateway-anslutningar</span><span class="sxs-lookup"><span data-stu-id="4da4d-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="4da4d-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="4da4d-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="4da4d-141">Inaktivera Internet säkerhets flaggan för dessa P2SVpnGateway-anslutningar</span><span class="sxs-lookup"><span data-stu-id="4da4d-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="4da4d-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da4d-142">-RoutingConfiguration</span></span>
<span data-ttu-id="4da4d-143">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="4da4d-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="4da4d-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4da4d-144">-Tag</span></span>
<span data-ttu-id="4da4d-145">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="4da4d-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4da4d-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="4da4d-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="4da4d-147">P2S VpnClient AddressPool för denna P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4da4d-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4da4d-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="4da4d-149">Skalan för denna P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4da4d-149">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da4d-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="4da4d-151">VpnServerConfiguration ska kopplas till denna P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4da4d-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4da4d-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="4da4d-153">ID för VPN-serverkonfigurationen denna P2SVpnGateway kommer att kopplas till.</span><span class="sxs-lookup"><span data-stu-id="4da4d-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da4d-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4da4d-154">-Confirm</span></span>
<span data-ttu-id="4da4d-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4da4d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da4d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da4d-156">-WhatIf</span></span>
<span data-ttu-id="4da4d-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4da4d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da4d-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4da4d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da4d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da4d-159">CommonParameters</span></span>
<span data-ttu-id="4da4d-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da4d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da4d-161">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da4d-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da4d-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4da4d-162">INPUTS</span></span>

### <span data-ttu-id="4da4d-163">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4da4d-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="4da4d-164">System. String Microsoft. Azure. commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da4d-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="4da4d-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4da4d-165">OUTPUTS</span></span>

### <span data-ttu-id="4da4d-166">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4da4d-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="4da4d-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4da4d-167">NOTES</span></span>

## <span data-ttu-id="4da4d-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4da4d-168">RELATED LINKS</span></span>

[<span data-ttu-id="4da4d-169">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4da4d-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
