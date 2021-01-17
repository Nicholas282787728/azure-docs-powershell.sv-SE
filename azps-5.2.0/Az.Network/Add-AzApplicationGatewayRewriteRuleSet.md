---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412467"
---
# <span data-ttu-id="d8894-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="d8894-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8894-102">SYNOPSIS</span></span>
<span data-ttu-id="d8894-103">Lägger till en regel för att skriva en en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d8894-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="d8894-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8894-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8894-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8894-105">DESCRIPTION</span></span>
<span data-ttu-id="d8894-106">Cmdleten **Add-AzApplicationGatewayRewriteRuleSet** lägger till en regel uppsättning för att skriva på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d8894-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="d8894-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8894-107">EXAMPLES</span></span>

### <span data-ttu-id="d8894-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8894-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="d8894-109">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d8894-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d8894-110">Det andra kommandot lägger till regeln för ny skrivning för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d8894-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="d8894-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8894-111">PARAMETERS</span></span>

### <span data-ttu-id="d8894-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8894-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8894-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8894-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d8894-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8894-114">-DefaultProfile</span></span>
<span data-ttu-id="d8894-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8894-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8894-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8894-116">-Name</span></span>
<span data-ttu-id="d8894-117">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="d8894-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8894-118">-RewriteRule</span></span>
<span data-ttu-id="d8894-119">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="d8894-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="d8894-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8894-120">CommonParameters</span></span>
<span data-ttu-id="d8894-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8894-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8894-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8894-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8894-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8894-123">INPUTS</span></span>

### <span data-ttu-id="d8894-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8894-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8894-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8894-125">OUTPUTS</span></span>

### <span data-ttu-id="d8894-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8894-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8894-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8894-127">NOTES</span></span>

## <span data-ttu-id="d8894-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8894-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8894-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8894-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8894-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8894-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8894-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d8894-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8894-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d8894-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d8894-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d8894-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8894-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
