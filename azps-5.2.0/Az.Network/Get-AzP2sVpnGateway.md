---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393371"
---
# <span data-ttu-id="808b1-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="808b1-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="808b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="808b1-102">SYNOPSIS</span></span>
<span data-ttu-id="808b1-103">Hämtar en befintlig P2SVpnGateway under VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="808b1-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="808b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="808b1-104">SYNTAX</span></span>

### <span data-ttu-id="808b1-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="808b1-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808b1-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808b1-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="808b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="808b1-107">DESCRIPTION</span></span>
<span data-ttu-id="808b1-108">Med cmdleten **Get-AzP2sVpnGateway** kan du hämta en befintlig P2SVpnGateway under VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="808b1-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="808b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="808b1-109">EXAMPLES</span></span>

### <span data-ttu-id="808b1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="808b1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
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
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="808b1-111">Med cmdleten **Get-AzP2sVpnGateway** kan du hämta en befintlig P2SVpnGateway under VirtualHub som används för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="808b1-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="808b1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="808b1-112">PARAMETERS</span></span>

### <span data-ttu-id="808b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808b1-113">-DefaultProfile</span></span>
<span data-ttu-id="808b1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="808b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808b1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="808b1-115">-Name</span></span>
<span data-ttu-id="808b1-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="808b1-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="808b1-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="808b1-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808b1-119">CommonParameters</span></span>
<span data-ttu-id="808b1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808b1-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808b1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808b1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="808b1-122">INPUTS</span></span>

### <span data-ttu-id="808b1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="808b1-123">None</span></span>

## <span data-ttu-id="808b1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="808b1-124">OUTPUTS</span></span>

### <span data-ttu-id="808b1-125">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="808b1-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="808b1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="808b1-126">NOTES</span></span>

## <span data-ttu-id="808b1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="808b1-127">RELATED LINKS</span></span>
