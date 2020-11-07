---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: 2359459688dbae2c718e4a5d5f65bf68b2c8c5ea
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931322"
---
# <span data-ttu-id="53361-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53361-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="53361-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53361-102">SYNOPSIS</span></span>
<span data-ttu-id="53361-103">Hämtar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53361-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53361-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53361-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53361-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53361-105">DESCRIPTION</span></span>
<span data-ttu-id="53361-106">Cmdleten **Get-AzureRmApplicationGatewaySku** hämtar lager behållnings enheten (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53361-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="53361-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53361-107">EXAMPLES</span></span>

### <span data-ttu-id="53361-108">Exempel 1: skaffa en Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="53361-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="53361-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="53361-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="53361-110">Det andra kommandot får SKU för en Programgateway som heter ApplicationGateway01 och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="53361-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="53361-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53361-111">PARAMETERS</span></span>

### <span data-ttu-id="53361-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53361-112">-ApplicationGateway</span></span>
<span data-ttu-id="53361-113">Anger Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="53361-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="53361-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53361-114">-DefaultProfile</span></span>
<span data-ttu-id="53361-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53361-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53361-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53361-116">CommonParameters</span></span>
<span data-ttu-id="53361-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53361-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53361-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53361-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53361-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53361-119">INPUTS</span></span>

### <span data-ttu-id="53361-120">System. String</span><span class="sxs-lookup"><span data-stu-id="53361-120">System.String</span></span>

## <span data-ttu-id="53361-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53361-121">OUTPUTS</span></span>

### <span data-ttu-id="53361-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53361-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="53361-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53361-123">NOTES</span></span>

## <span data-ttu-id="53361-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53361-124">RELATED LINKS</span></span>

[<span data-ttu-id="53361-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53361-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="53361-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="53361-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


