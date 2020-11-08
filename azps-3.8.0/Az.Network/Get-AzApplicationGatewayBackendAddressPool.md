---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091307"
---
# <span data-ttu-id="a2753-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a2753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2753-102">SYNOPSIS</span></span>
<span data-ttu-id="a2753-103">Hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a2753-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="a2753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2753-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2753-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2753-105">DESCRIPTION</span></span>
<span data-ttu-id="a2753-106">Cmdleten **Get-AzApplicationGatewayBackendAddressPool** hämtar en eller flera konfigurationer från Server delen av adresspoolen från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a2753-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="a2753-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2753-107">EXAMPLES</span></span>

### <span data-ttu-id="a2753-108">Exempel 1: Hämta en server med backend-servern</span><span class="sxs-lookup"><span data-stu-id="a2753-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a2753-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a2753-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a2753-110">Det andra kommandot får backend-adresspoolen som är kopplad till $AppGw namngivna Pool01 och lagrar den i $BackendPool-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a2753-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="a2753-111">Exempel 2: Hämta en lista över backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="a2753-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="a2753-112">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a2753-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a2753-113">Det andra kommandot får en lista över de backend-adresspooler som är associerade med $AppGw och lagrar listan i $BackendPools-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a2753-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="a2753-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2753-114">PARAMETERS</span></span>

### <span data-ttu-id="a2753-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2753-115">-ApplicationGateway</span></span>
<span data-ttu-id="a2753-116">Cmdleten **Get-AzApplicationGatewayBackendAddressPool** hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a2753-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2753-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2753-117">-DefaultProfile</span></span>
<span data-ttu-id="a2753-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2753-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2753-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2753-119">-Name</span></span>
<span data-ttu-id="a2753-120">Anger namnet på den backend-adresspool som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a2753-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2753-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2753-121">CommonParameters</span></span>
<span data-ttu-id="a2753-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2753-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2753-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2753-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2753-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2753-124">INPUTS</span></span>

### <span data-ttu-id="a2753-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2753-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a2753-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2753-126">OUTPUTS</span></span>

### <span data-ttu-id="a2753-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a2753-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2753-128">NOTES</span></span>

## <span data-ttu-id="a2753-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2753-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2753-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a2753-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a2753-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a2753-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2753-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


