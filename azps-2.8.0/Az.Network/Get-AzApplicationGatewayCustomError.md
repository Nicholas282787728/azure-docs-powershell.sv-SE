---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918798"
---
# <span data-ttu-id="06d26-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="06d26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06d26-102">SYNOPSIS</span></span>
<span data-ttu-id="06d26-103">Hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="06d26-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="06d26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06d26-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06d26-105">DESCRIPTION</span></span>
<span data-ttu-id="06d26-106">Cmdleten **Get-AzApplicationGatewayCustomError** hämtar anpassade fel från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="06d26-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="06d26-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06d26-107">EXAMPLES</span></span>

### <span data-ttu-id="06d26-108">Exempel 1: hämtar ett anpassat fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="06d26-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="06d26-109">Det här kommandot hämtar och returnerar det anpassade felet hos HTTP-statuskod 502 från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="06d26-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="06d26-110">Exempel 2: hämtar listan över alla anpassade fel i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="06d26-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="06d26-111">Det här kommandot hämtar och returnerar listan över alla anpassade fel från Application Gateway $appgw.</span><span class="sxs-lookup"><span data-stu-id="06d26-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="06d26-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06d26-112">PARAMETERS</span></span>

### <span data-ttu-id="06d26-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06d26-113">-ApplicationGateway</span></span>
<span data-ttu-id="06d26-114">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="06d26-114">The Application Gateway</span></span>

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

### <span data-ttu-id="06d26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d26-115">-DefaultProfile</span></span>
<span data-ttu-id="06d26-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06d26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d26-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="06d26-117">-StatusCode</span></span>
<span data-ttu-id="06d26-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="06d26-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="06d26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d26-119">CommonParameters</span></span>
<span data-ttu-id="06d26-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d26-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d26-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d26-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06d26-122">INPUTS</span></span>

### <span data-ttu-id="06d26-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06d26-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06d26-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06d26-124">OUTPUTS</span></span>

### <span data-ttu-id="06d26-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="06d26-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06d26-126">NOTES</span></span>

## <span data-ttu-id="06d26-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06d26-127">RELATED LINKS</span></span>

[<span data-ttu-id="06d26-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06d26-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06d26-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="06d26-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="06d26-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)