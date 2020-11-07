---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757574"
---
# <span data-ttu-id="0331a-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0331a-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0331a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0331a-102">SYNOPSIS</span></span>
<span data-ttu-id="0331a-103">Hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0331a-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0331a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0331a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0331a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0331a-105">DESCRIPTION</span></span>
<span data-ttu-id="0331a-106">Cmdleten **Get-AzureRmApplicationGatewayCustomError** hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0331a-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="0331a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0331a-107">EXAMPLES</span></span>

### <span data-ttu-id="0331a-108">Exempel 1: hämtar ett anpassat fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="0331a-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="0331a-109">Det här kommandot hämtar och returnerar det anpassade felet hos HTTP-statuskod 502 från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="0331a-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="0331a-110">Exempel 2: hämtar listan över alla anpassade fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="0331a-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="0331a-111">Det här kommandot hämtar och returnerar listan över alla anpassade fel från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="0331a-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="0331a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0331a-112">PARAMETERS</span></span>

### <span data-ttu-id="0331a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0331a-113">-ApplicationGateway</span></span>
<span data-ttu-id="0331a-114">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0331a-114">The Application Gateway</span></span>

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

### <span data-ttu-id="0331a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0331a-115">-DefaultProfile</span></span>
<span data-ttu-id="0331a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0331a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0331a-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0331a-117">-StatusCode</span></span>
<span data-ttu-id="0331a-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0331a-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0331a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0331a-119">CommonParameters</span></span>
<span data-ttu-id="0331a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0331a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0331a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0331a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0331a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0331a-122">INPUTS</span></span>

### <span data-ttu-id="0331a-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0331a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0331a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0331a-124">OUTPUTS</span></span>

### <span data-ttu-id="0331a-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0331a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0331a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0331a-126">NOTES</span></span>

## <span data-ttu-id="0331a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0331a-127">RELATED LINKS</span></span>
