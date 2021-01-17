---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389454"
---
# <span data-ttu-id="ab8be-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ab8be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab8be-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8be-103">Hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ab8be-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="ab8be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab8be-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab8be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab8be-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8be-106">Cmdleten **Get-AzApplicationGatewayCustomError** hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ab8be-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="ab8be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab8be-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8be-108">Exempel 1: hämtar ett anpassat fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="ab8be-109">Det här kommandot hämtar och returnerar det anpassade felet hos HTTP-statuskod 502 från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="ab8be-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="ab8be-110">Exempel 2: hämtar listan över alla anpassade fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="ab8be-111">Det här kommandot hämtar och returnerar listan över alla anpassade fel från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="ab8be-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="ab8be-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab8be-112">PARAMETERS</span></span>

### <span data-ttu-id="ab8be-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-113">-ApplicationGateway</span></span>
<span data-ttu-id="ab8be-114">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-114">The Application Gateway</span></span>

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

### <span data-ttu-id="ab8be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8be-115">-DefaultProfile</span></span>
<span data-ttu-id="ab8be-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8be-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ab8be-117">-StatusCode</span></span>
<span data-ttu-id="ab8be-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab8be-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ab8be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8be-119">CommonParameters</span></span>
<span data-ttu-id="ab8be-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8be-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab8be-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8be-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab8be-122">INPUTS</span></span>

### <span data-ttu-id="ab8be-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab8be-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab8be-124">OUTPUTS</span></span>

### <span data-ttu-id="ab8be-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ab8be-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab8be-126">NOTES</span></span>

## <span data-ttu-id="ab8be-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab8be-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab8be-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab8be-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab8be-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab8be-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab8be-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
