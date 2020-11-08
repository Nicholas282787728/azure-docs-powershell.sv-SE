---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088090"
---
# <span data-ttu-id="05d8e-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="05d8e-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="05d8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="05d8e-103">Hämtar hälso information om aggregared för webbplats anslutningar från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="05d8e-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="05d8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05d8e-104">SYNTAX</span></span>

### <span data-ttu-id="05d8e-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="05d8e-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d8e-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="05d8e-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05d8e-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="05d8e-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05d8e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05d8e-108">DESCRIPTION</span></span>
<span data-ttu-id="05d8e-109">Med cmdleten **Get-AzP2sVpnGatewayConnectionHealth** kan du hämta den aktuella aggregerade hälsan för Point to Site Connections från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="05d8e-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="05d8e-110">Aggregerad hälsa visar antalet peka på webbplats klienter som är anslutna till P2SVpnGateway, totalt inkommande och utgående byte via P2SVpnGateway och tilldelade IP-adresser för anslutna punkter till klient klienter.</span><span class="sxs-lookup"><span data-stu-id="05d8e-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="05d8e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05d8e-111">EXAMPLES</span></span>

### <span data-ttu-id="05d8e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05d8e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="05d8e-113">Med cmdleten **Get-AzP2sVpnGatewayConnectionHealth** kan du hämta den aktuella aggregerade hälsan för Point to Site Connections från P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="05d8e-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="05d8e-114">Ovan kommando Tillåt utmatnings status visar att antalet peka på plats klienter som är anslutna till P2SVpnGateway är 2.</span><span class="sxs-lookup"><span data-stu-id="05d8e-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="05d8e-115">Totalt antal inkommande och utgående byte som överförts via P2SVpnGateway är 100 respektive 200.</span><span class="sxs-lookup"><span data-stu-id="05d8e-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="05d8e-116">Tilldelade IP-adresser för anslutna plats klienter är "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="05d8e-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="05d8e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05d8e-117">PARAMETERS</span></span>

### <span data-ttu-id="05d8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d8e-118">-DefaultProfile</span></span>
<span data-ttu-id="05d8e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05d8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05d8e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05d8e-120">-InputObject</span></span>
<span data-ttu-id="05d8e-121">P2s VPN gateway-objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="05d8e-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="05d8e-122">-Name</span></span>
<span data-ttu-id="05d8e-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="05d8e-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="05d8e-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="05d8e-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05d8e-126">-ResourceId</span></span>
<span data-ttu-id="05d8e-127">Azure-resurs-ID för P2SVpnGateway som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="05d8e-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d8e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d8e-128">CommonParameters</span></span>
<span data-ttu-id="05d8e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d8e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d8e-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d8e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d8e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05d8e-131">INPUTS</span></span>

### <span data-ttu-id="05d8e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05d8e-132">System.String</span></span>
<span data-ttu-id="05d8e-133">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="05d8e-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="05d8e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05d8e-134">OUTPUTS</span></span>

### <span data-ttu-id="05d8e-135">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="05d8e-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="05d8e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05d8e-136">NOTES</span></span>

## <span data-ttu-id="05d8e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05d8e-137">RELATED LINKS</span></span>
