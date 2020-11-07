---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922304"
---
# <span data-ttu-id="644fc-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="644fc-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="644fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="644fc-102">SYNOPSIS</span></span>
<span data-ttu-id="644fc-103">Hämtar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="644fc-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="644fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="644fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="644fc-105">DESCRIPTION</span></span>
<span data-ttu-id="644fc-106">Cmdleten **Get-AzApplicationGatewayURLPathMapConfig** hämtar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="644fc-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="644fc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="644fc-107">EXAMPLES</span></span>

### <span data-ttu-id="644fc-108">Exempel 1: Hämta en konfiguration för URL-sökvägsvariabler</span><span class="sxs-lookup"><span data-stu-id="644fc-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="644fc-109">Det här kommandot hämtar konfigurationen för URL-sökvägsvariabler från backend-servern som finns på gatewayen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="644fc-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="644fc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="644fc-110">PARAMETERS</span></span>

### <span data-ttu-id="644fc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="644fc-111">-ApplicationGateway</span></span>
<span data-ttu-id="644fc-112">Anger den Programgateway till vilken denna cmdlet hämtar en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="644fc-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="644fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644fc-113">-DefaultProfile</span></span>
<span data-ttu-id="644fc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="644fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="644fc-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="644fc-115">-Name</span></span>
<span data-ttu-id="644fc-116">Anger namnet på URL-sökvägen i den här cmdleten för att hämta Sök vägs karta.</span><span class="sxs-lookup"><span data-stu-id="644fc-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="644fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644fc-117">CommonParameters</span></span>
<span data-ttu-id="644fc-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="644fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644fc-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644fc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644fc-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="644fc-120">INPUTS</span></span>

### <span data-ttu-id="644fc-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="644fc-121">PSApplicationGateway</span></span>
<span data-ttu-id="644fc-122">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="644fc-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="644fc-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="644fc-123">OUTPUTS</span></span>

### <span data-ttu-id="644fc-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="644fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="644fc-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="644fc-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="644fc-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="644fc-126">NOTES</span></span>

## <span data-ttu-id="644fc-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="644fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="644fc-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="644fc-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="644fc-129">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="644fc-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="644fc-130">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="644fc-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="644fc-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="644fc-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


