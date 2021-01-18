---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522452"
---
# <span data-ttu-id="a4a26-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4a26-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a4a26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4a26-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a26-103">Hämtar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="a4a26-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a4a26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4a26-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4a26-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a26-106">Cmdleten **Get-AzApplicationGatewayURLPathMapConfig** hämtar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="a4a26-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a4a26-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4a26-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a26-108">Exempel 1: Hämta en konfiguration för URL-sökvägsvariabler</span><span class="sxs-lookup"><span data-stu-id="a4a26-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="a4a26-109">Det här kommandot hämtar konfigurationen för URL-sökvägsvariabler från backend-servern som finns på gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="a4a26-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="a4a26-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4a26-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a26-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4a26-111">-ApplicationGateway</span></span>
<span data-ttu-id="a4a26-112">Anger den Programgateway till vilken denna cmdlet hämtar en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="a4a26-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="a4a26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a26-113">-DefaultProfile</span></span>
<span data-ttu-id="a4a26-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4a26-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4a26-115">-Name</span></span>
<span data-ttu-id="a4a26-116">Anger namnet på URL-sökvägen i den här cmdleten för att hämta Sök vägs karta.</span><span class="sxs-lookup"><span data-stu-id="a4a26-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="a4a26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a26-117">CommonParameters</span></span>
<span data-ttu-id="a4a26-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a26-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4a26-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a26-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4a26-120">INPUTS</span></span>

### <span data-ttu-id="a4a26-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4a26-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4a26-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4a26-122">OUTPUTS</span></span>

### <span data-ttu-id="a4a26-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="a4a26-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="a4a26-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4a26-124">NOTES</span></span>

## <span data-ttu-id="a4a26-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4a26-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4a26-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4a26-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4a26-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4a26-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4a26-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4a26-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a4a26-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a4a26-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


