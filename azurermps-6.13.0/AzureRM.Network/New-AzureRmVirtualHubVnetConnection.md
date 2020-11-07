---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756378"
---
# <span data-ttu-id="0e7dc-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0e7dc-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="0e7dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7dc-103">New-AzureRmVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e7dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e7dc-104">SYNTAX</span></span>

### <span data-ttu-id="0e7dc-105">ByVirtualHubNameByRemoteVirtualNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="0e7dc-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="0e7dc-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="0e7dc-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e7dc-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7dc-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e7dc-111">DESCRIPTION</span></span>
<span data-ttu-id="0e7dc-112">New-AzureRmVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="0e7dc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e7dc-113">EXAMPLES</span></span>

### <span data-ttu-id="0e7dc-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e7dc-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="0e7dc-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="0e7dc-116">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="0e7dc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e7dc-117">PARAMETERS</span></span>

### <span data-ttu-id="0e7dc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e7dc-118">-AsJob</span></span>
<span data-ttu-id="0e7dc-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0e7dc-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e7dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7dc-120">-DefaultProfile</span></span>
<span data-ttu-id="0e7dc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7dc-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e7dc-122">-Name</span></span>
<span data-ttu-id="0e7dc-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0e7dc-124">-ParentObject</span></span>
<span data-ttu-id="0e7dc-125">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-126">-ParentResourceId</span></span>
<span data-ttu-id="0e7dc-127">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="0e7dc-128">-ParentResourceName</span></span>
<span data-ttu-id="0e7dc-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e7dc-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="0e7dc-131">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0e7dc-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0e7dc-133">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7dc-134">-ResourceGroupName</span></span>
<span data-ttu-id="0e7dc-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e7dc-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e7dc-136">-Confirm</span></span>
<span data-ttu-id="0e7dc-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7dc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7dc-138">-WhatIf</span></span>
<span data-ttu-id="0e7dc-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7dc-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7dc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7dc-141">CommonParameters</span></span>
<span data-ttu-id="0e7dc-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7dc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7dc-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7dc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7dc-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e7dc-144">INPUTS</span></span>

### <span data-ttu-id="0e7dc-145">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0e7dc-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="0e7dc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0e7dc-146">System.String</span></span>

## <span data-ttu-id="0e7dc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e7dc-147">OUTPUTS</span></span>

### <span data-ttu-id="0e7dc-148">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="0e7dc-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="0e7dc-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e7dc-149">NOTES</span></span>

## <span data-ttu-id="0e7dc-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e7dc-150">RELATED LINKS</span></span>
