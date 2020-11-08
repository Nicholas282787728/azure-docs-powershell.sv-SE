---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271566"
---
# <span data-ttu-id="cac88-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cac88-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cac88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cac88-102">SYNOPSIS</span></span>
<span data-ttu-id="cac88-103">Ansluter till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="cac88-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="cac88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cac88-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cac88-105">DESCRIPTION</span></span>
<span data-ttu-id="cac88-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="cac88-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="cac88-107">Cmdleten **Get-AzVirtualNetworkGatewayConnection** returnerar anslutningen baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="cac88-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="cac88-108">Om cmdleten **Get-AzVirtualNetworkGatewayConnection** utfärdas utan att ange parametern-name visar utdata inte ConnectionStatus och SharedKey.</span><span class="sxs-lookup"><span data-stu-id="cac88-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="cac88-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cac88-109">EXAMPLES</span></span>

### <span data-ttu-id="cac88-110">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="cac88-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="cac88-111">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="cac88-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="cac88-112">2: Hämta alla anslutningar för virtuella nätverk med filter</span><span class="sxs-lookup"><span data-stu-id="cac88-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="cac88-113">Returnerar alla anslutningar för virtuell nätverksgateway som börjar med "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="cac88-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="cac88-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cac88-114">PARAMETERS</span></span>

### <span data-ttu-id="cac88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac88-115">-DefaultProfile</span></span>
<span data-ttu-id="cac88-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cac88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac88-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cac88-117">-Name</span></span>
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

### <span data-ttu-id="cac88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac88-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="cac88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac88-119">CommonParameters</span></span>
<span data-ttu-id="cac88-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac88-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cac88-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac88-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cac88-122">INPUTS</span></span>

### <span data-ttu-id="cac88-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cac88-123">System.String</span></span>

## <span data-ttu-id="cac88-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cac88-124">OUTPUTS</span></span>

### <span data-ttu-id="cac88-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cac88-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="cac88-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cac88-126">NOTES</span></span>

## <span data-ttu-id="cac88-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cac88-127">RELATED LINKS</span></span>

[<span data-ttu-id="cac88-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cac88-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cac88-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cac88-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="cac88-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cac88-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
