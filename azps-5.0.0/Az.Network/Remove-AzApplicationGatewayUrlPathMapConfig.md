---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269192"
---
# <span data-ttu-id="49703-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="49703-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="49703-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49703-102">SYNOPSIS</span></span>
<span data-ttu-id="49703-103">Tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="49703-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="49703-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49703-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49703-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49703-105">DESCRIPTION</span></span>
<span data-ttu-id="49703-106">Cmdleten **Remove-AzApplicationGatewayUrlPathMapConfig** tar bort URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="49703-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="49703-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49703-107">EXAMPLES</span></span>

### <span data-ttu-id="49703-108">Exempel 1: ta bort en URL-mappsökväg från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="49703-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="49703-109">Med det första kommandot får programgatewayen namnet appGwName och lagras resultatet i $appgw variabel.</span><span class="sxs-lookup"><span data-stu-id="49703-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="49703-110">Det andra kommandot tar bort URL-sökvägen som heter map01 från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="49703-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="49703-111">Det tredje kommandot uppdaterar programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="49703-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="49703-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49703-112">PARAMETERS</span></span>

### <span data-ttu-id="49703-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49703-113">-ApplicationGateway</span></span>
<span data-ttu-id="49703-114">Anger den Programgateway till vilken denna cmdlet tar bort URL Path Map-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="49703-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="49703-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49703-115">-DefaultProfile</span></span>
<span data-ttu-id="49703-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49703-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49703-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="49703-117">-Name</span></span>
<span data-ttu-id="49703-118">Anger namnet på URL-sökvägen som den här cmdleten tar bort från backend-servern.</span><span class="sxs-lookup"><span data-stu-id="49703-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="49703-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49703-119">CommonParameters</span></span>
<span data-ttu-id="49703-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49703-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49703-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49703-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49703-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49703-122">INPUTS</span></span>

### <span data-ttu-id="49703-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49703-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49703-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49703-124">OUTPUTS</span></span>

### <span data-ttu-id="49703-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49703-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49703-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49703-126">NOTES</span></span>

## <span data-ttu-id="49703-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49703-127">RELATED LINKS</span></span>

[<span data-ttu-id="49703-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="49703-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="49703-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="49703-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="49703-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="49703-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="49703-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="49703-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


