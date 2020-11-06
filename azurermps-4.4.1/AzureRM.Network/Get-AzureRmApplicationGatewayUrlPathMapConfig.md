---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 4a15bf67906606735b47e48b62d3e35cbcc91914
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573636"
---
# <span data-ttu-id="4c0b9-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c0b9-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4c0b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0b9-103">Hämtar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c0b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c0b9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c0b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="4c0b9-106">Cmdleten **Get-AzureRmApplicationGatewayURLPathMapConfig** hämtar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4c0b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="4c0b9-108">Exempel 1: Hämta en konfiguration för URL-sökvägsvariabler</span><span class="sxs-lookup"><span data-stu-id="4c0b9-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="4c0b9-109">Det här kommandot hämtar konfigurationen för URL-sökvägsvariabler från backend-servern som finns på gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="4c0b9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c0b9-110">PARAMETERS</span></span>

### <span data-ttu-id="4c0b9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c0b9-111">-ApplicationGateway</span></span>
<span data-ttu-id="4c0b9-112">Anger den Programgateway till vilken denna cmdlet hämtar en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="4c0b9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c0b9-113">-Name</span></span>
<span data-ttu-id="4c0b9-114">Anger namnet på URL-sökvägen i den här cmdleten för att hämta Sök vägs karta.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-114">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="4c0b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0b9-115">-DefaultProfile</span></span>
<span data-ttu-id="4c0b9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c0b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0b9-117">CommonParameters</span></span>
<span data-ttu-id="4c0b9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0b9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0b9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0b9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c0b9-120">INPUTS</span></span>

### <span data-ttu-id="4c0b9-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c0b9-121">PSApplicationGateway</span></span>
<span data-ttu-id="4c0b9-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4c0b9-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4c0b9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c0b9-123">OUTPUTS</span></span>

### <span data-ttu-id="4c0b9-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="4c0b9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="4c0b9-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="4c0b9-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="4c0b9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c0b9-126">NOTES</span></span>

## <span data-ttu-id="4c0b9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c0b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c0b9-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c0b9-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c0b9-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c0b9-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c0b9-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c0b9-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c0b9-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c0b9-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


