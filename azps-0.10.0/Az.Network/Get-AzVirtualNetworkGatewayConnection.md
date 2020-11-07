---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922205"
---
# <span data-ttu-id="ed569-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed569-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ed569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed569-102">SYNOPSIS</span></span>
<span data-ttu-id="ed569-103">Ansluter till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ed569-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="ed569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed569-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed569-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed569-105">DESCRIPTION</span></span>
<span data-ttu-id="ed569-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="ed569-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="ed569-107">Cmdleten **Get-AzVirtualNetworkGatewayConnection** returnerar anslutningen baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="ed569-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ed569-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed569-108">EXAMPLES</span></span>

### <span data-ttu-id="ed569-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ed569-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ed569-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="ed569-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ed569-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed569-111">PARAMETERS</span></span>

### <span data-ttu-id="ed569-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed569-112">-DefaultProfile</span></span>
<span data-ttu-id="ed569-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed569-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed569-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed569-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed569-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed569-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed569-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed569-116">CommonParameters</span></span>
<span data-ttu-id="ed569-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed569-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed569-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed569-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed569-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed569-119">INPUTS</span></span>

## <span data-ttu-id="ed569-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed569-120">OUTPUTS</span></span>

### <span data-ttu-id="ed569-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed569-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ed569-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed569-122">NOTES</span></span>

## <span data-ttu-id="ed569-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed569-123">RELATED LINKS</span></span>

