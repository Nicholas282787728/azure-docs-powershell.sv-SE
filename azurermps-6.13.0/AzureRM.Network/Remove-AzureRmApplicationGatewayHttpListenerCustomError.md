---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574794"
---
# <span data-ttu-id="254bd-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="254bd-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="254bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="254bd-102">SYNOPSIS</span></span>
<span data-ttu-id="254bd-103">Tar bort ett anpassat fel från en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="254bd-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="254bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="254bd-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="254bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="254bd-105">DESCRIPTION</span></span>
<span data-ttu-id="254bd-106">Cmdleten **Remove-AzureRmApplicationGatewayCustomError** tar bort ett anpassat fel från en http-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="254bd-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="254bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="254bd-107">EXAMPLES</span></span>

### <span data-ttu-id="254bd-108">Exempel 1: tar bort det anpassade felet från en http-lyssnare</span><span class="sxs-lookup"><span data-stu-id="254bd-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="254bd-109">Det här kommandot tar bort det anpassade felet hos HTTP-statuskod 502 från http-lyssnaren $listener 01 och returnerar den uppdaterade lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="254bd-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="254bd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="254bd-110">PARAMETERS</span></span>

### <span data-ttu-id="254bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254bd-111">-DefaultProfile</span></span>
<span data-ttu-id="254bd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="254bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="254bd-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="254bd-113">-HttpListener</span></span>
<span data-ttu-id="254bd-114">Http-lyssnaren för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="254bd-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="254bd-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="254bd-115">-StatusCode</span></span>
<span data-ttu-id="254bd-116">Status kod för kund felet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="254bd-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="254bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254bd-117">CommonParameters</span></span>
<span data-ttu-id="254bd-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="254bd-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="254bd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254bd-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="254bd-120">INPUTS</span></span>

### <span data-ttu-id="254bd-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="254bd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="254bd-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="254bd-122">OUTPUTS</span></span>

### <span data-ttu-id="254bd-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="254bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="254bd-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="254bd-124">NOTES</span></span>

## <span data-ttu-id="254bd-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="254bd-125">RELATED LINKS</span></span>
