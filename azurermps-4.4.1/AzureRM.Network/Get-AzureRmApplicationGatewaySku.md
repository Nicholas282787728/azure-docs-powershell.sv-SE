---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 09639badc9ac96525456b7a9556c8e2afa7ebf2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576717"
---
# <span data-ttu-id="07c37-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07c37-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="07c37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07c37-102">SYNOPSIS</span></span>
<span data-ttu-id="07c37-103">Hämtar SKU för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="07c37-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07c37-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07c37-105">DESCRIPTION</span></span>
<span data-ttu-id="07c37-106">Cmdleten **Get-AzureRmApplicationGatewaySku** hämtar lager behållnings enheten (SKU) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="07c37-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="07c37-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07c37-107">EXAMPLES</span></span>

### <span data-ttu-id="07c37-108">Exempel 1: skaffa en Application Gateway SKU</span><span class="sxs-lookup"><span data-stu-id="07c37-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="07c37-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="07c37-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="07c37-110">Det andra kommandot får SKU för en Programgateway som heter ApplicationGateway01 och lagrar resultatet i variabeln som heter $SKU.</span><span class="sxs-lookup"><span data-stu-id="07c37-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="07c37-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07c37-111">PARAMETERS</span></span>

### <span data-ttu-id="07c37-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07c37-112">-ApplicationGateway</span></span>
<span data-ttu-id="07c37-113">Anger Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="07c37-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="07c37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c37-114">-DefaultProfile</span></span>
<span data-ttu-id="07c37-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07c37-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c37-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c37-116">CommonParameters</span></span>
<span data-ttu-id="07c37-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c37-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c37-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c37-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c37-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07c37-119">INPUTS</span></span>

### <span data-ttu-id="07c37-120">System. String</span><span class="sxs-lookup"><span data-stu-id="07c37-120">System.String</span></span>

## <span data-ttu-id="07c37-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07c37-121">OUTPUTS</span></span>

### <span data-ttu-id="07c37-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07c37-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="07c37-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07c37-123">NOTES</span></span>

## <span data-ttu-id="07c37-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07c37-124">RELATED LINKS</span></span>

[<span data-ttu-id="07c37-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07c37-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="07c37-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07c37-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)

