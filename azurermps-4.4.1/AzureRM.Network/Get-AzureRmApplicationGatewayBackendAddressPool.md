---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ccef6b60dd33ebc584f782899134509a4e89f2be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755444"
---
# <span data-ttu-id="ed9c6-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ed9c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9c6-103">Hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed9c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed9c6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed9c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed9c6-105">DESCRIPTION</span></span>

## <span data-ttu-id="ed9c6-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed9c6-106">EXAMPLES</span></span>

### <span data-ttu-id="ed9c6-107">Exempel 1: Hämta en server med backend-servern</span><span class="sxs-lookup"><span data-stu-id="ed9c6-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ed9c6-108">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed9c6-109">Det andra kommandot får backend-adresspoolen som är kopplad till $AppGw namngivna Pool01 och lagrar den i $BackendPool-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="ed9c6-110">Exempel 2: Hämta en lista över backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="ed9c6-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="ed9c6-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed9c6-112">Det andra kommandot får en lista över de backend-adresspooler som är associerade med $AppGw och lagrar listan i $BackendPools-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="ed9c6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed9c6-113">PARAMETERS</span></span>

### <span data-ttu-id="ed9c6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed9c6-114">-ApplicationGateway</span></span>
<span data-ttu-id="ed9c6-115">Cmdleten **Get-AzureRmApplicationGatewayBackendAddressPool** hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="ed9c6-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed9c6-116">-Name</span></span>
<span data-ttu-id="ed9c6-117">Anger namnet på den backend-adresspool som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-117">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ed9c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9c6-118">-DefaultProfile</span></span>
<span data-ttu-id="ed9c6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9c6-120">CommonParameters</span></span>
<span data-ttu-id="ed9c6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9c6-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9c6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9c6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed9c6-123">INPUTS</span></span>

### <span data-ttu-id="ed9c6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ed9c6-124">System.String</span></span>

## <span data-ttu-id="ed9c6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed9c6-125">OUTPUTS</span></span>

### <span data-ttu-id="ed9c6-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ed9c6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed9c6-127">NOTES</span></span>

## <span data-ttu-id="ed9c6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed9c6-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed9c6-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ed9c6-130">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ed9c6-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ed9c6-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed9c6-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


