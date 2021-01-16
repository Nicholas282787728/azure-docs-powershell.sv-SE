---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523417"
---
# <span data-ttu-id="4a773-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="4a773-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a773-102">SYNOPSIS</span></span>
<span data-ttu-id="4a773-103">Lägger till en regel för att skriva en en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4a773-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="4a773-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a773-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a773-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a773-105">DESCRIPTION</span></span>
<span data-ttu-id="4a773-106">Cmdleten **Add-AzApplicationGatewayRewriteRuleSet** lägger till en regel uppsättning för att skriva på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4a773-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="4a773-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a773-107">EXAMPLES</span></span>

### <span data-ttu-id="4a773-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a773-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="4a773-109">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4a773-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4a773-110">Det andra kommandot lägger till regeln för ny skrivning för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4a773-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="4a773-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a773-111">PARAMETERS</span></span>

### <span data-ttu-id="4a773-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a773-112">-ApplicationGateway</span></span>
<span data-ttu-id="4a773-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a773-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4a773-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a773-114">-DefaultProfile</span></span>
<span data-ttu-id="4a773-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a773-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a773-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a773-116">-Name</span></span>
<span data-ttu-id="4a773-117">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="4a773-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="4a773-118">-RewriteRule</span></span>
<span data-ttu-id="4a773-119">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="4a773-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a773-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a773-120">CommonParameters</span></span>
<span data-ttu-id="4a773-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a773-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a773-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a773-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a773-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a773-123">INPUTS</span></span>

### <span data-ttu-id="4a773-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a773-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a773-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a773-125">OUTPUTS</span></span>

### <span data-ttu-id="4a773-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a773-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a773-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a773-127">NOTES</span></span>

## <span data-ttu-id="4a773-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a773-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a773-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a773-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a773-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a773-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a773-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a773-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4a773-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="4a773-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4a773-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="4a773-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a773-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
