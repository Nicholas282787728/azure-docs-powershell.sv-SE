---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269451"
---
# <span data-ttu-id="56f84-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56f84-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="56f84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56f84-102">SYNOPSIS</span></span>
<span data-ttu-id="56f84-103">Får en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="56f84-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="56f84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56f84-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56f84-105">DESCRIPTION</span></span>
<span data-ttu-id="56f84-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="56f84-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="56f84-107">Cmdleten **Get-AzLocalNetworkGateway** returnerar det objekt som representerar din lokala-gateway baserat på namn och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="56f84-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="56f84-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56f84-108">EXAMPLES</span></span>

### <span data-ttu-id="56f84-109">Exempel 1: skaffa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="56f84-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="56f84-110">Returnerar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW1" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="56f84-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="56f84-111">Exempel 2: skaffa lokala nätverks-gateways med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="56f84-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="56f84-112">Returnerar objektet för den lokala Nätverksgatewayen med namn som börjar med "myLocalGW" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="56f84-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="56f84-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56f84-113">PARAMETERS</span></span>

### <span data-ttu-id="56f84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f84-114">-DefaultProfile</span></span>
<span data-ttu-id="56f84-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56f84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f84-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="56f84-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="56f84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f84-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="56f84-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f84-118">CommonParameters</span></span>
<span data-ttu-id="56f84-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f84-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f84-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56f84-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f84-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56f84-121">INPUTS</span></span>

### <span data-ttu-id="56f84-122">System. String</span><span class="sxs-lookup"><span data-stu-id="56f84-122">System.String</span></span>

## <span data-ttu-id="56f84-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56f84-123">OUTPUTS</span></span>

### <span data-ttu-id="56f84-124">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56f84-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="56f84-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56f84-125">NOTES</span></span>

## <span data-ttu-id="56f84-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56f84-126">RELATED LINKS</span></span>

[<span data-ttu-id="56f84-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56f84-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="56f84-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56f84-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="56f84-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="56f84-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)