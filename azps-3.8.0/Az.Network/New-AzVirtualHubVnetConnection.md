---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090963"
---
# <span data-ttu-id="4603a-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4603a-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4603a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4603a-102">SYNOPSIS</span></span>
<span data-ttu-id="4603a-103">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="4603a-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4603a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4603a-104">SYNTAX</span></span>

### <span data-ttu-id="4603a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4603a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4603a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4603a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4603a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4603a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4603a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4603a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4603a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4603a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4603a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4603a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4603a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4603a-111">DESCRIPTION</span></span>
<span data-ttu-id="4603a-112">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="4603a-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4603a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4603a-113">EXAMPLES</span></span>

### <span data-ttu-id="4603a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4603a-114">Example 1</span></span>

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
```

<span data-ttu-id="4603a-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="4603a-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4603a-116">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="4603a-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="4603a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4603a-117">PARAMETERS</span></span>

### <span data-ttu-id="4603a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4603a-118">-AsJob</span></span>
<span data-ttu-id="4603a-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4603a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4603a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4603a-120">-DefaultProfile</span></span>
<span data-ttu-id="4603a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4603a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4603a-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="4603a-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="4603a-123">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="4603a-123">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="4603a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4603a-124">-Name</span></span>
<span data-ttu-id="4603a-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4603a-125">The resource name.</span></span>

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

### <span data-ttu-id="4603a-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4603a-126">-ParentObject</span></span>
<span data-ttu-id="4603a-127">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="4603a-127">The parent resource.</span></span>

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

### <span data-ttu-id="4603a-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4603a-128">-ParentResourceId</span></span>
<span data-ttu-id="4603a-129">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="4603a-129">The parent resource.</span></span>

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

### <span data-ttu-id="4603a-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4603a-130">-ParentResourceName</span></span>
<span data-ttu-id="4603a-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4603a-131">The resource group name.</span></span>

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

### <span data-ttu-id="4603a-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4603a-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="4603a-133">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="4603a-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="4603a-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4603a-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="4603a-135">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="4603a-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="4603a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4603a-136">-ResourceGroupName</span></span>
<span data-ttu-id="4603a-137">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4603a-137">The resource group name.</span></span>

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

### <span data-ttu-id="4603a-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4603a-138">-Confirm</span></span>
<span data-ttu-id="4603a-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4603a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4603a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4603a-140">-WhatIf</span></span>
<span data-ttu-id="4603a-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4603a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4603a-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4603a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4603a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4603a-143">CommonParameters</span></span>
<span data-ttu-id="4603a-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4603a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4603a-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4603a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4603a-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4603a-146">INPUTS</span></span>

### <span data-ttu-id="4603a-147">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4603a-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4603a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4603a-148">System.String</span></span>

## <span data-ttu-id="4603a-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4603a-149">OUTPUTS</span></span>

### <span data-ttu-id="4603a-150">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4603a-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4603a-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4603a-151">NOTES</span></span>

## <span data-ttu-id="4603a-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4603a-152">RELATED LINKS</span></span>

[<span data-ttu-id="4603a-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4603a-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4603a-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4603a-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
