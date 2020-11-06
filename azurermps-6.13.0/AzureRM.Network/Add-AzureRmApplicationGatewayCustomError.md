---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574821"
---
# <span data-ttu-id="d9c15-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d9c15-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d9c15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9c15-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c15-103">Lägger till ett anpassat fel i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d9c15-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9c15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9c15-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9c15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9c15-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c15-106">Cmdleten **Add-AzureRmApplicationGatewayCustomError** lägger till ett anpassat fel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d9c15-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="d9c15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9c15-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c15-108">Exempel 1: lägger till ett anpassat fel till en Application Gateway-nivå</span><span class="sxs-lookup"><span data-stu-id="d9c15-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="d9c15-109">Det här kommandot lägger till ett anpassat fel med HTTP-statuskod 502 till Programgateway $appgw och returnerar den uppdaterade gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d9c15-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="d9c15-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9c15-110">PARAMETERS</span></span>

### <span data-ttu-id="d9c15-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9c15-111">-ApplicationGateway</span></span>
<span data-ttu-id="d9c15-112">Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d9c15-112">The Application Gateway</span></span>

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

### <span data-ttu-id="d9c15-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="d9c15-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="d9c15-114">Felsida URL för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9c15-114">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c15-115">-DefaultProfile</span></span>
<span data-ttu-id="d9c15-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c15-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d9c15-117">-StatusCode</span></span>
<span data-ttu-id="d9c15-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9c15-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c15-119">CommonParameters</span></span>
<span data-ttu-id="d9c15-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c15-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c15-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c15-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9c15-122">INPUTS</span></span>

### <span data-ttu-id="d9c15-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9c15-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9c15-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9c15-124">OUTPUTS</span></span>

### <span data-ttu-id="d9c15-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9c15-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9c15-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9c15-126">NOTES</span></span>

## <span data-ttu-id="d9c15-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9c15-127">RELATED LINKS</span></span>
