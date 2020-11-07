---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748171"
---
# <span data-ttu-id="3d9e8-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3d9e8-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="3d9e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9e8-103">Hämtar en VpnGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="3d9e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d9e8-104">SYNTAX</span></span>

### <span data-ttu-id="3d9e8-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9e8-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9e8-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d9e8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d9e8-107">DESCRIPTION</span></span>
<span data-ttu-id="3d9e8-108">Hämtar en VpnGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="3d9e8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d9e8-109">EXAMPLES</span></span>

### <span data-ttu-id="3d9e8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d9e8-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="3d9e8-111">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3d9e8-112">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3d9e8-113">Då hämtas VpnGateway med dess resourceGroupName och gateway-namnet.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="3d9e8-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d9e8-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="3d9e8-115">Denna cmdlet tar emot alla gateways som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="3d9e8-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="3d9e8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d9e8-116">PARAMETERS</span></span>

### <span data-ttu-id="3d9e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9e8-117">-DefaultProfile</span></span>
<span data-ttu-id="3d9e8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d9e8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d9e8-119">-Name</span></span>
<span data-ttu-id="3d9e8-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3d9e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d9e8-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3d9e8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9e8-123">CommonParameters</span></span>
<span data-ttu-id="3d9e8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9e8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9e8-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d9e8-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9e8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d9e8-126">INPUTS</span></span>

### <span data-ttu-id="3d9e8-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d9e8-127">None</span></span>

## <span data-ttu-id="3d9e8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d9e8-128">OUTPUTS</span></span>

### <span data-ttu-id="3d9e8-129">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3d9e8-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="3d9e8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d9e8-130">NOTES</span></span>

## <span data-ttu-id="3d9e8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d9e8-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d9e8-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3d9e8-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="3d9e8-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3d9e8-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="3d9e8-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3d9e8-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)