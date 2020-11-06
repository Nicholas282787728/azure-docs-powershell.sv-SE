---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576216"
---
# <span data-ttu-id="86bfb-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86bfb-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="86bfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="86bfb-103">Hämtar en VpnGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="86bfb-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86bfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86bfb-104">SYNTAX</span></span>

### <span data-ttu-id="86bfb-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="86bfb-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86bfb-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86bfb-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86bfb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86bfb-107">DESCRIPTION</span></span>
<span data-ttu-id="86bfb-108">Hämtar en VpnGateway-resurs med ResourceGroupName och GatewayName eller visar alla gateways via ResourceGroupName eller SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="86bfb-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="86bfb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86bfb-109">EXAMPLES</span></span>

### <span data-ttu-id="86bfb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86bfb-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="86bfb-111">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="86bfb-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="86bfb-112">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="86bfb-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="86bfb-113">Då hämtas VpnGateway med dess resourceGroupName och gateway-namnet.</span><span class="sxs-lookup"><span data-stu-id="86bfb-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="86bfb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86bfb-114">PARAMETERS</span></span>

### <span data-ttu-id="86bfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86bfb-115">-DefaultProfile</span></span>
<span data-ttu-id="86bfb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86bfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86bfb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="86bfb-117">-Name</span></span>
<span data-ttu-id="86bfb-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="86bfb-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86bfb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86bfb-119">-ResourceGroupName</span></span>
<span data-ttu-id="86bfb-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="86bfb-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86bfb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86bfb-121">CommonParameters</span></span>
<span data-ttu-id="86bfb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86bfb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86bfb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86bfb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86bfb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86bfb-124">INPUTS</span></span>

### <span data-ttu-id="86bfb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="86bfb-125">System.String</span></span>

## <span data-ttu-id="86bfb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86bfb-126">OUTPUTS</span></span>

### <span data-ttu-id="86bfb-127">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="86bfb-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="86bfb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86bfb-128">NOTES</span></span>

## <span data-ttu-id="86bfb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86bfb-129">RELATED LINKS</span></span>
