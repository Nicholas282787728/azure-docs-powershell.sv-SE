---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918847"
---
# <span data-ttu-id="eb8fb-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="eb8fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8fb-103">Lägger till en regel för att skriva en en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="eb8fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb8fb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb8fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8fb-106">Cmdleten **Add-AzApplicationGatewayRewriteRuleSet** lägger till en regel uppsättning för att skriva på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="eb8fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb8fb-107">EXAMPLES</span></span>

### <span data-ttu-id="eb8fb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb8fb-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="eb8fb-109">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eb8fb-110">Det andra kommandot lägger till regeln för ny skrivning för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="eb8fb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb8fb-111">PARAMETERS</span></span>

### <span data-ttu-id="eb8fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb8fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="eb8fb-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb8fb-113">The applicationGateway</span></span>

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

### <span data-ttu-id="eb8fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8fb-114">-DefaultProfile</span></span>
<span data-ttu-id="eb8fb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb8fb-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb8fb-116">-Name</span></span>
<span data-ttu-id="eb8fb-117">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="eb8fb-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="eb8fb-118">-RewriteRule</span></span>
<span data-ttu-id="eb8fb-119">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="eb8fb-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="eb8fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8fb-120">CommonParameters</span></span>
<span data-ttu-id="eb8fb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8fb-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8fb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8fb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb8fb-123">INPUTS</span></span>

### <span data-ttu-id="eb8fb-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb8fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb8fb-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb8fb-125">OUTPUTS</span></span>

### <span data-ttu-id="eb8fb-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb8fb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb8fb-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb8fb-127">NOTES</span></span>

## <span data-ttu-id="eb8fb-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb8fb-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb8fb-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb8fb-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb8fb-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb8fb-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="eb8fb-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eb8fb-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="eb8fb-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eb8fb-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="eb8fb-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8fb-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
