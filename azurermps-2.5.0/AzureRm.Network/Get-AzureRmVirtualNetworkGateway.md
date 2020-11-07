---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929785"
---
# <span data-ttu-id="2c89b-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c89b-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="2c89b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c89b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c89b-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2c89b-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c89b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c89b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c89b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c89b-105">DESCRIPTION</span></span>
<span data-ttu-id="2c89b-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="2c89b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="2c89b-107">Cmdleten **Get-AzureRmVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="2c89b-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2c89b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c89b-108">EXAMPLES</span></span>

### <span data-ttu-id="2c89b-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2c89b-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="2c89b-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="2c89b-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="2c89b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c89b-111">PARAMETERS</span></span>

### <span data-ttu-id="2c89b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c89b-112">-DefaultProfile</span></span>
<span data-ttu-id="2c89b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c89b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c89b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c89b-114">-Name</span></span>
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

### <span data-ttu-id="2c89b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c89b-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2c89b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c89b-116">CommonParameters</span></span>
<span data-ttu-id="2c89b-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c89b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c89b-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c89b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c89b-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c89b-119">INPUTS</span></span>

## <span data-ttu-id="2c89b-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c89b-120">OUTPUTS</span></span>

### <span data-ttu-id="2c89b-121">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c89b-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2c89b-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c89b-122">NOTES</span></span>

## <span data-ttu-id="2c89b-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c89b-123">RELATED LINKS</span></span>

