---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926797"
---
# <span data-ttu-id="06d4a-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="06d4a-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="06d4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="06d4a-103">Få identitet tilldelad till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="06d4a-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="06d4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06d4a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="06d4a-106">Cmdleten **Get-AzApplicationGatewayIdentity** får identiteten tilldelad till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="06d4a-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="06d4a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="06d4a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06d4a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="06d4a-109">I det här exemplet visas hur du får en Programgateway-identitet från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="06d4a-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="06d4a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="06d4a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06d4a-111">-ApplicationGateway</span></span>
<span data-ttu-id="06d4a-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06d4a-112">The applicationGateway</span></span>

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

### <span data-ttu-id="06d4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d4a-113">-DefaultProfile</span></span>
<span data-ttu-id="06d4a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06d4a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d4a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d4a-115">CommonParameters</span></span>
<span data-ttu-id="06d4a-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d4a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d4a-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d4a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d4a-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06d4a-118">INPUTS</span></span>

### <span data-ttu-id="06d4a-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06d4a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06d4a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06d4a-120">OUTPUTS</span></span>

### <span data-ttu-id="06d4a-121">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="06d4a-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="06d4a-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06d4a-122">NOTES</span></span>

## <span data-ttu-id="06d4a-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06d4a-123">RELATED LINKS</span></span>
