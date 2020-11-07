---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b4a6ae7db1221a2dee8a0bd5343ad78ed88a0abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755962"
---
# <span data-ttu-id="1331c-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1331c-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1331c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1331c-102">SYNOPSIS</span></span>
<span data-ttu-id="1331c-103">Ansluter till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="1331c-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1331c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1331c-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1331c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1331c-105">DESCRIPTION</span></span>
<span data-ttu-id="1331c-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="1331c-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="1331c-107">Cmdleten **Get-AzureRmVirtualNetworkGatewayConnection** returnerar anslutningen baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="1331c-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1331c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1331c-108">EXAMPLES</span></span>

### <span data-ttu-id="1331c-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="1331c-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="1331c-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="1331c-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="1331c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1331c-111">PARAMETERS</span></span>

### <span data-ttu-id="1331c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1331c-112">-DefaultProfile</span></span>
<span data-ttu-id="1331c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1331c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1331c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="1331c-114">-Name</span></span>
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

### <span data-ttu-id="1331c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1331c-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1331c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1331c-116">CommonParameters</span></span>
<span data-ttu-id="1331c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1331c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1331c-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1331c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1331c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1331c-119">INPUTS</span></span>

### <span data-ttu-id="1331c-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="1331c-120">None</span></span>
<span data-ttu-id="1331c-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1331c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1331c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1331c-122">OUTPUTS</span></span>

### <span data-ttu-id="1331c-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1331c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1331c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1331c-124">NOTES</span></span>

## <span data-ttu-id="1331c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1331c-125">RELATED LINKS</span></span>

