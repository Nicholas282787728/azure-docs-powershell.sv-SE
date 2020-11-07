---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929045"
---
# <span data-ttu-id="a8c79-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c79-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a8c79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8c79-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c79-103">Hämtar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="a8c79-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8c79-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8c79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8c79-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c79-106">Cmdleten **Get-AzureRmApplicationGatewayURLPathMapConfig** hämtar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="a8c79-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a8c79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8c79-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c79-108">Exempel 1: Hämta en konfiguration för URL-sökvägsvariabler</span><span class="sxs-lookup"><span data-stu-id="a8c79-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="a8c79-109">Det här kommandot hämtar konfigurationen för URL-sökvägsvariabler från backend-servern som finns på gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8c79-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="a8c79-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8c79-110">PARAMETERS</span></span>

### <span data-ttu-id="a8c79-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8c79-111">-ApplicationGateway</span></span>
<span data-ttu-id="a8c79-112">Anger den Programgateway till vilken denna cmdlet hämtar en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="a8c79-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="a8c79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c79-113">-DefaultProfile</span></span>
<span data-ttu-id="a8c79-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c79-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c79-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8c79-115">-Name</span></span>
<span data-ttu-id="a8c79-116">Anger namnet på URL-sökvägen i den här cmdleten för att hämta Sök vägs karta.</span><span class="sxs-lookup"><span data-stu-id="a8c79-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="a8c79-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c79-117">CommonParameters</span></span>
<span data-ttu-id="a8c79-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c79-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c79-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c79-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c79-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8c79-120">INPUTS</span></span>

### <span data-ttu-id="a8c79-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8c79-121">PSApplicationGateway</span></span>
<span data-ttu-id="a8c79-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a8c79-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a8c79-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8c79-123">OUTPUTS</span></span>

### <span data-ttu-id="a8c79-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="a8c79-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="a8c79-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="a8c79-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="a8c79-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8c79-126">NOTES</span></span>

## <span data-ttu-id="a8c79-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8c79-127">RELATED LINKS</span></span>

[<span data-ttu-id="a8c79-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c79-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c79-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c79-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c79-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c79-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c79-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c79-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


