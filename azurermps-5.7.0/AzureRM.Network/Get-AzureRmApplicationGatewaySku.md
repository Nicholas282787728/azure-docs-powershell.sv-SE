---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 425955dd9b39b78c599262f7681c97dd15c93fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574274"
---
# <span data-ttu-id="5fc75-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5fc75-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="5fc75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fc75-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc75-103">Hämtar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5fc75-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fc75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fc75-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc75-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fc75-105">DESCRIPTION</span></span>
<span data-ttu-id="5fc75-106">Cmdleten **Get-AzureRmApplicationGatewaySku** hämtar lager behållnings enheten (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="5fc75-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="5fc75-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fc75-107">EXAMPLES</span></span>

### <span data-ttu-id="5fc75-108">Exempel 1: skaffa en Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="5fc75-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="5fc75-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5fc75-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5fc75-110">Det andra kommandot får SKU för en Programgateway som heter ApplicationGateway01 och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="5fc75-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="5fc75-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fc75-111">PARAMETERS</span></span>

### <span data-ttu-id="5fc75-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fc75-112">-ApplicationGateway</span></span>
<span data-ttu-id="5fc75-113">Anger Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="5fc75-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="5fc75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc75-114">-DefaultProfile</span></span>
<span data-ttu-id="5fc75-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc75-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc75-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc75-116">CommonParameters</span></span>
<span data-ttu-id="5fc75-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc75-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc75-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc75-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc75-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fc75-119">INPUTS</span></span>

### <span data-ttu-id="5fc75-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5fc75-120">System.String</span></span>

## <span data-ttu-id="5fc75-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fc75-121">OUTPUTS</span></span>

### <span data-ttu-id="5fc75-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5fc75-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="5fc75-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fc75-123">NOTES</span></span>

## <span data-ttu-id="5fc75-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fc75-124">RELATED LINKS</span></span>

[<span data-ttu-id="5fc75-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5fc75-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="5fc75-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5fc75-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


