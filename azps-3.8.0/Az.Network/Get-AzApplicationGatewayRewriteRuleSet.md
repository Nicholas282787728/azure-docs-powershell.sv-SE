---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926777"
---
# <span data-ttu-id="61f33-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="61f33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61f33-102">SYNOPSIS</span></span>
<span data-ttu-id="61f33-103">Hämtar en regel uppsättning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="61f33-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="61f33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61f33-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f33-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61f33-105">DESCRIPTION</span></span>
<span data-ttu-id="61f33-106">Hämtar en regel uppsättning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="61f33-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="61f33-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61f33-107">EXAMPLES</span></span>

### <span data-ttu-id="61f33-108">Exempel 1: Hämta en specifik regel uppsättning för att skriva över</span><span class="sxs-lookup"><span data-stu-id="61f33-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="61f33-109">Med det första kommandot får programgatewayen namnet ApplicationGateway01 och lagras resultatet i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="61f33-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="61f33-110">Det andra kommandot hämtar regel uppsättningen för omskrivning som heter RuleSet01 från den Application Gateway som lagras i variabeln som heter $AppGW.</span><span class="sxs-lookup"><span data-stu-id="61f33-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="61f33-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61f33-111">PARAMETERS</span></span>

### <span data-ttu-id="61f33-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f33-112">-ApplicationGateway</span></span>
<span data-ttu-id="61f33-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f33-113">The applicationGateway</span></span>

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

### <span data-ttu-id="61f33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f33-114">-DefaultProfile</span></span>
<span data-ttu-id="61f33-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61f33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f33-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="61f33-116">-Name</span></span>
<span data-ttu-id="61f33-117">Namnet på Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="61f33-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f33-118">CommonParameters</span></span>
<span data-ttu-id="61f33-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f33-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f33-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61f33-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f33-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61f33-121">INPUTS</span></span>

### <span data-ttu-id="61f33-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f33-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61f33-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61f33-123">OUTPUTS</span></span>

### <span data-ttu-id="61f33-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="61f33-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61f33-125">NOTES</span></span>

## <span data-ttu-id="61f33-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61f33-126">RELATED LINKS</span></span>

[<span data-ttu-id="61f33-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="61f33-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="61f33-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="61f33-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61f33-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="61f33-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="61f33-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="61f33-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="61f33-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="61f33-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f33-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
