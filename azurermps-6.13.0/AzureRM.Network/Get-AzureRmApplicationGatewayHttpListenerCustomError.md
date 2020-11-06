---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576914"
---
# <span data-ttu-id="244c0-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="244c0-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="244c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="244c0-102">SYNOPSIS</span></span>
<span data-ttu-id="244c0-103">Hämtar anpassade fel från en http-lyssnare av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="244c0-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="244c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="244c0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="244c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="244c0-105">DESCRIPTION</span></span>
<span data-ttu-id="244c0-106">Cmdleten **Get-AzureRmApplicationGatewayCustomError** hämtar anpassade fel från en http-lyssnare av en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="244c0-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="244c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="244c0-107">EXAMPLES</span></span>

### <span data-ttu-id="244c0-108">Exempel 1: hämtar ett anpassat fel i en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="244c0-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="244c0-109">Det här kommandot hämtar och returnerar det anpassade felet hos HTTP-statuskod 502 från http-lyssnaren $listener 01.</span><span class="sxs-lookup"><span data-stu-id="244c0-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="244c0-110">Exempel 2: hämtar listan över alla anpassade fel i en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="244c0-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="244c0-111">Det här kommandot hämtar och returnerar listan över alla anpassade fel från http-lyssnaren $listener 01.</span><span class="sxs-lookup"><span data-stu-id="244c0-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="244c0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="244c0-112">PARAMETERS</span></span>

### <span data-ttu-id="244c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244c0-113">-DefaultProfile</span></span>
<span data-ttu-id="244c0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="244c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="244c0-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="244c0-115">-HttpListener</span></span>
<span data-ttu-id="244c0-116">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="244c0-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="244c0-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="244c0-117">-StatusCode</span></span>
<span data-ttu-id="244c0-118">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="244c0-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="244c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244c0-119">CommonParameters</span></span>
<span data-ttu-id="244c0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="244c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="244c0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="244c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244c0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="244c0-122">INPUTS</span></span>

### <span data-ttu-id="244c0-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="244c0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="244c0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="244c0-124">OUTPUTS</span></span>

### <span data-ttu-id="244c0-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="244c0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="244c0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="244c0-126">NOTES</span></span>

## <span data-ttu-id="244c0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="244c0-127">RELATED LINKS</span></span>
