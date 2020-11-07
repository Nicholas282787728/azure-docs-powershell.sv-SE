---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922337"
---
# <span data-ttu-id="de8e1-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="de8e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="de8e1-103">Hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="de8e1-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="de8e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de8e1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de8e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de8e1-105">DESCRIPTION</span></span>

## <span data-ttu-id="de8e1-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de8e1-106">EXAMPLES</span></span>

### <span data-ttu-id="de8e1-107">Exempel 1: Hämta en server med backend-servern</span><span class="sxs-lookup"><span data-stu-id="de8e1-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="de8e1-108">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="de8e1-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="de8e1-109">Det andra kommandot får backend-adresspoolen som är kopplad till $AppGw namngivna Pool01 och lagrar den i $BackendPool-variabeln.</span><span class="sxs-lookup"><span data-stu-id="de8e1-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="de8e1-110">Exempel 2: Hämta en lista över backend-serverpoolen</span><span class="sxs-lookup"><span data-stu-id="de8e1-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="de8e1-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="de8e1-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="de8e1-112">Det andra kommandot får en lista över de backend-adresspooler som är associerade med $AppGw och lagrar listan i $BackendPools-variabeln.</span><span class="sxs-lookup"><span data-stu-id="de8e1-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="de8e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de8e1-113">PARAMETERS</span></span>

### <span data-ttu-id="de8e1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de8e1-114">-ApplicationGateway</span></span>
<span data-ttu-id="de8e1-115">Cmdleten **Get-AzApplicationGatewayBackendAddressPool** hämtar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="de8e1-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="de8e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8e1-116">-DefaultProfile</span></span>
<span data-ttu-id="de8e1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de8e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de8e1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="de8e1-118">-Name</span></span>
<span data-ttu-id="de8e1-119">Anger namnet på den backend-adresspool som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="de8e1-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="de8e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8e1-120">CommonParameters</span></span>
<span data-ttu-id="de8e1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8e1-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8e1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8e1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de8e1-123">INPUTS</span></span>

### <span data-ttu-id="de8e1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="de8e1-124">System.String</span></span>

## <span data-ttu-id="de8e1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de8e1-125">OUTPUTS</span></span>

### <span data-ttu-id="de8e1-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="de8e1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de8e1-127">NOTES</span></span>

## <span data-ttu-id="de8e1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de8e1-128">RELATED LINKS</span></span>

[<span data-ttu-id="de8e1-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="de8e1-130">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="de8e1-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="de8e1-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de8e1-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


