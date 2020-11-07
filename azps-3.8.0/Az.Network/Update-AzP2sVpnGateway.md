---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 39fb3223b1a80b831874bbd833d6d0c97aace53f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925790"
---
# <span data-ttu-id="05cfb-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="05cfb-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="05cfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="05cfb-103">Uppdatera en befintlig P2SVpnGateway under VirtualHub för webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="05cfb-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="05cfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05cfb-104">SYNTAX</span></span>

### <span data-ttu-id="05cfb-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="05cfb-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="05cfb-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="05cfb-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="05cfb-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="05cfb-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="05cfb-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="05cfb-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05cfb-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="05cfb-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cfb-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="05cfb-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05cfb-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05cfb-114">DESCRIPTION</span></span>
<span data-ttu-id="05cfb-115">Med cmdleten **Update-AzP2sVpnGateway** kan du uppdatera en befintlig P2SVpnGateway under VirtualHub med ny VpnClientAddressPool eller ny VpnServerConfiguration eller ändring av VpnGatewayScaleUnit.</span><span class="sxs-lookup"><span data-stu-id="05cfb-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="05cfb-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05cfb-116">EXAMPLES</span></span>

### <span data-ttu-id="05cfb-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05cfb-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces                                    

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="05cfb-118">Med cmdleten **Update-AzP2sVpnGateway** kan du uppdatera en befintlig P2SVpnGateway under VirtualHub med nya VpnClientAddressPool.</span><span class="sxs-lookup"><span data-stu-id="05cfb-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="05cfb-119">När peka på webbplats klient ansluter med den här P2SVpnGateway tilldelas en av IP-adresserna från den här VpnClientAddressPool till klienten.</span><span class="sxs-lookup"><span data-stu-id="05cfb-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

## <span data-ttu-id="05cfb-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05cfb-120">PARAMETERS</span></span>

### <span data-ttu-id="05cfb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05cfb-121">-AsJob</span></span>
<span data-ttu-id="05cfb-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="05cfb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05cfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cfb-123">-DefaultProfile</span></span>
<span data-ttu-id="05cfb-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05cfb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05cfb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05cfb-125">-InputObject</span></span>
<span data-ttu-id="05cfb-126">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="05cfb-126">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="05cfb-127">-Name</span></span>
<span data-ttu-id="05cfb-128">P2S VPN gateway-namn.</span><span class="sxs-lookup"><span data-stu-id="05cfb-128">The P2S vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cfb-129">-ResourceGroupName</span></span>
<span data-ttu-id="05cfb-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="05cfb-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05cfb-131">-ResourceId</span></span>
<span data-ttu-id="05cfb-132">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="05cfb-132">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="05cfb-133">-Tag</span></span>
<span data-ttu-id="05cfb-134">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="05cfb-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="05cfb-135">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="05cfb-135">-VpnClientAddressPool</span></span>
<span data-ttu-id="05cfb-136">P2S VpnClient AddressPool för denna P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="05cfb-136">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-137">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="05cfb-137">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="05cfb-138">Skalan för denna P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="05cfb-138">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-139">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="05cfb-139">-VpnServerConfiguration</span></span>
<span data-ttu-id="05cfb-140">VpnServerConfiguration ska kopplas till denna P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="05cfb-140">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-141">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="05cfb-141">-VpnServerConfigurationId</span></span>
<span data-ttu-id="05cfb-142">ID för VPN-serverkonfigurationen denna P2SVpnGateway kommer att kopplas till.</span><span class="sxs-lookup"><span data-stu-id="05cfb-142">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cfb-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05cfb-143">-Confirm</span></span>
<span data-ttu-id="05cfb-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05cfb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cfb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cfb-145">-WhatIf</span></span>
<span data-ttu-id="05cfb-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05cfb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05cfb-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05cfb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cfb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cfb-148">CommonParameters</span></span>
<span data-ttu-id="05cfb-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cfb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cfb-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05cfb-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cfb-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05cfb-151">INPUTS</span></span>

### <span data-ttu-id="05cfb-152">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="05cfb-152">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="05cfb-153">System. String Microsoft. Azure. commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="05cfb-153">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="05cfb-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05cfb-154">OUTPUTS</span></span>

### <span data-ttu-id="05cfb-155">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="05cfb-155">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="05cfb-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05cfb-156">NOTES</span></span>

## <span data-ttu-id="05cfb-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05cfb-157">RELATED LINKS</span></span>
