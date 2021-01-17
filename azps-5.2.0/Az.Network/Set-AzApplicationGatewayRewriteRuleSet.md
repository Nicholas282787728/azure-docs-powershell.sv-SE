---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417728"
---
# <span data-ttu-id="bfee9-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="bfee9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfee9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfee9-103">Ändrar en regel uppsättning för en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bfee9-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="bfee9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfee9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfee9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfee9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfee9-106">Cmdleten **set-AzApplicationGatewayRewriteRuleSet** ändrar en regel för en anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="bfee9-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="bfee9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfee9-107">EXAMPLES</span></span>

### <span data-ttu-id="bfee9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bfee9-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="bfee9-109">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="bfee9-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bfee9-110">Med det andra kommandot ändras regel för ny skrivning för Application Gateway för användning av omskrivnings regler som anges i variabeln $rule.</span><span class="sxs-lookup"><span data-stu-id="bfee9-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="bfee9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfee9-111">PARAMETERS</span></span>

### <span data-ttu-id="bfee9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfee9-112">-ApplicationGateway</span></span>
<span data-ttu-id="bfee9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfee9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bfee9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfee9-114">-DefaultProfile</span></span>
<span data-ttu-id="bfee9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfee9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfee9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bfee9-116">-Name</span></span>
<span data-ttu-id="bfee9-117">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="bfee9-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="bfee9-118">-RewriteRule</span></span>
<span data-ttu-id="bfee9-119">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="bfee9-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="bfee9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfee9-120">CommonParameters</span></span>
<span data-ttu-id="bfee9-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfee9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfee9-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfee9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfee9-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfee9-123">INPUTS</span></span>

### <span data-ttu-id="bfee9-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfee9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfee9-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfee9-125">OUTPUTS</span></span>

### <span data-ttu-id="bfee9-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfee9-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfee9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfee9-127">NOTES</span></span>

## <span data-ttu-id="bfee9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfee9-128">RELATED LINKS</span></span>

[<span data-ttu-id="bfee9-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bfee9-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bfee9-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bfee9-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bfee9-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bfee9-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="bfee9-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bfee9-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="bfee9-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfee9-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
