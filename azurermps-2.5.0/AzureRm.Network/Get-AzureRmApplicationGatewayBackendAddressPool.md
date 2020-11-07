---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929829"
---
# <span data-ttu-id="d0258-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d0258-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0258-102">SYNOPSIS</span></span>
<span data-ttu-id="d0258-103">Hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d0258-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0258-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0258-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0258-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0258-105">DESCRIPTION</span></span>

## <span data-ttu-id="d0258-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0258-106">EXAMPLES</span></span>

### <span data-ttu-id="d0258-107">Exempel 1: Hämta en server med backend-servern</span><span class="sxs-lookup"><span data-stu-id="d0258-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d0258-108">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d0258-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0258-109">Det andra kommandot får backend-adresspoolen som är kopplad till $AppGw namngivna Pool01 och lagrar den i $BackendPool-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d0258-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="d0258-110">Exempel 2: Hämta en lista över backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="d0258-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="d0258-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d0258-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0258-112">Det andra kommandot får en lista över de backend-adresspooler som är associerade med $AppGw och lagrar listan i $BackendPools-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d0258-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="d0258-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0258-113">PARAMETERS</span></span>

### <span data-ttu-id="d0258-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0258-114">-ApplicationGateway</span></span>
<span data-ttu-id="d0258-115">Cmdleten **Get-AzureRmApplicationGatewayBackendAddressPool** hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d0258-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0258-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0258-116">-DefaultProfile</span></span>
<span data-ttu-id="d0258-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0258-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0258-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0258-118">-Name</span></span>
<span data-ttu-id="d0258-119">Anger namnet på den backend-adresspool som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d0258-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0258-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0258-120">CommonParameters</span></span>
<span data-ttu-id="d0258-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0258-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0258-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0258-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0258-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0258-123">INPUTS</span></span>

### <span data-ttu-id="d0258-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d0258-124">System.String</span></span>

## <span data-ttu-id="d0258-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0258-125">OUTPUTS</span></span>

### <span data-ttu-id="d0258-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d0258-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0258-127">NOTES</span></span>

## <span data-ttu-id="d0258-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0258-128">RELATED LINKS</span></span>

[<span data-ttu-id="d0258-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d0258-130">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d0258-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d0258-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0258-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


