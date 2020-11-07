---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: c0599f599770467c3528cff902d2d60434c335e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929782"
---
# <span data-ttu-id="008d5-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="008d5-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="008d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="008d5-102">SYNOPSIS</span></span>
<span data-ttu-id="008d5-103">Ansluter till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="008d5-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="008d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="008d5-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="008d5-105">DESCRIPTION</span></span>
<span data-ttu-id="008d5-106">Anslutningen för virtuell nätverksgateway är det objekt som representerar IPsec-tunneln (plats-till-plats eller VNet som är ansluten till din virtuella nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="008d5-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="008d5-107">Cmdleten **Get-AzureRmVirtualNetworkGatewayConnection** returnerar anslutningen baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="008d5-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="008d5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="008d5-108">EXAMPLES</span></span>

### <span data-ttu-id="008d5-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="008d5-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="008d5-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "tunnel" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="008d5-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="008d5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="008d5-111">PARAMETERS</span></span>

### <span data-ttu-id="008d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008d5-112">-DefaultProfile</span></span>
<span data-ttu-id="008d5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="008d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008d5-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="008d5-114">-Name</span></span>
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

### <span data-ttu-id="008d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008d5-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="008d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008d5-116">CommonParameters</span></span>
<span data-ttu-id="008d5-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008d5-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008d5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008d5-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="008d5-119">INPUTS</span></span>

## <span data-ttu-id="008d5-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="008d5-120">OUTPUTS</span></span>

### <span data-ttu-id="008d5-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="008d5-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="008d5-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="008d5-122">NOTES</span></span>

## <span data-ttu-id="008d5-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="008d5-123">RELATED LINKS</span></span>

