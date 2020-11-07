---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748369"
---
# <span data-ttu-id="1ded3-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1ded3-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1ded3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ded3-102">SYNOPSIS</span></span>
<span data-ttu-id="1ded3-103">Få identitet tilldelad till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="1ded3-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="1ded3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ded3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ded3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ded3-105">DESCRIPTION</span></span>
<span data-ttu-id="1ded3-106">Cmdleten **Get-AzApplicationGatewayIdentity** får identiteten tilldelad till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="1ded3-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="1ded3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ded3-107">EXAMPLES</span></span>

### <span data-ttu-id="1ded3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ded3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="1ded3-109">I det här exemplet visas hur du får en Programgateway-identitet från Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1ded3-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="1ded3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ded3-110">PARAMETERS</span></span>

### <span data-ttu-id="1ded3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded3-111">-ApplicationGateway</span></span>
<span data-ttu-id="1ded3-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded3-112">The applicationGateway</span></span>

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

### <span data-ttu-id="1ded3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ded3-113">-DefaultProfile</span></span>
<span data-ttu-id="1ded3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ded3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ded3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ded3-115">CommonParameters</span></span>
<span data-ttu-id="1ded3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ded3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ded3-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ded3-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ded3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ded3-118">INPUTS</span></span>

### <span data-ttu-id="1ded3-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ded3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ded3-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ded3-120">OUTPUTS</span></span>

### <span data-ttu-id="1ded3-121">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1ded3-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="1ded3-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ded3-122">NOTES</span></span>

## <span data-ttu-id="1ded3-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ded3-123">RELATED LINKS</span></span>
