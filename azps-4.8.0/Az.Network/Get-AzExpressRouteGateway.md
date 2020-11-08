---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261880"
---
# <span data-ttu-id="04228-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="04228-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="04228-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04228-102">SYNOPSIS</span></span>
<span data-ttu-id="04228-103">Hämtar en ExpressRouteGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="04228-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="04228-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04228-104">SYNTAX</span></span>

### <span data-ttu-id="04228-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="04228-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04228-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04228-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04228-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="04228-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04228-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04228-108">DESCRIPTION</span></span>
<span data-ttu-id="04228-109">Hämtar en ExpressRouteGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="04228-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="04228-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04228-110">EXAMPLES</span></span>

### <span data-ttu-id="04228-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04228-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="04228-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra centrala USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="04228-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="04228-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="04228-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="04228-114">Då hämtas ExpressRouteGateway med dess resourceGroupName och gateway-namnet.</span><span class="sxs-lookup"><span data-stu-id="04228-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="04228-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="04228-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="04228-116">Det här kommandot får alla ExpressRouteGateways som börjar med "test"</span><span class="sxs-lookup"><span data-stu-id="04228-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="04228-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04228-117">PARAMETERS</span></span>

### <span data-ttu-id="04228-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04228-118">-DefaultProfile</span></span>
<span data-ttu-id="04228-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04228-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04228-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="04228-120">-Name</span></span>
<span data-ttu-id="04228-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="04228-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="04228-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04228-122">-ResourceGroupName</span></span>
<span data-ttu-id="04228-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="04228-123">The resource group name.</span></span>

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

### <span data-ttu-id="04228-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04228-124">-ResourceId</span></span>
<span data-ttu-id="04228-125">Azure Resource ID för expressRouteGateway ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="04228-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04228-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04228-126">CommonParameters</span></span>
<span data-ttu-id="04228-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04228-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04228-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04228-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04228-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04228-129">INPUTS</span></span>

### <span data-ttu-id="04228-130">System. String</span><span class="sxs-lookup"><span data-stu-id="04228-130">System.String</span></span>

## <span data-ttu-id="04228-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04228-131">OUTPUTS</span></span>

### <span data-ttu-id="04228-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="04228-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="04228-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04228-133">NOTES</span></span>

## <span data-ttu-id="04228-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04228-134">RELATED LINKS</span></span>
