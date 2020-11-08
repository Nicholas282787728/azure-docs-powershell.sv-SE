---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102109"
---
# <span data-ttu-id="110fb-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="110fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="110fb-102">SYNOPSIS</span></span>
<span data-ttu-id="110fb-103">Tar bort en regel uppsättning för en omskrivning från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="110fb-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="110fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="110fb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="110fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="110fb-105">DESCRIPTION</span></span>
<span data-ttu-id="110fb-106">Cmdleten **Remove-AzApplicationGatewayRewriteRuleSet** tar bort en regel uppsättning för en omarbetning från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="110fb-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="110fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="110fb-107">EXAMPLES</span></span>

### <span data-ttu-id="110fb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="110fb-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="110fb-109">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="110fb-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="110fb-110">Det andra kommandot tar bort den omskrivnings regel uppsättning som heter RuleSet02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="110fb-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="110fb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="110fb-111">PARAMETERS</span></span>

### <span data-ttu-id="110fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="110fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="110fb-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="110fb-113">The applicationGateway</span></span>

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

### <span data-ttu-id="110fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110fb-114">-DefaultProfile</span></span>
<span data-ttu-id="110fb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="110fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110fb-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="110fb-116">-Name</span></span>
<span data-ttu-id="110fb-117">Namnet på Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="110fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110fb-118">CommonParameters</span></span>
<span data-ttu-id="110fb-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110fb-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="110fb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110fb-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="110fb-121">INPUTS</span></span>

### <span data-ttu-id="110fb-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="110fb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="110fb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="110fb-123">OUTPUTS</span></span>

### <span data-ttu-id="110fb-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="110fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="110fb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="110fb-125">NOTES</span></span>

## <span data-ttu-id="110fb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="110fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="110fb-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="110fb-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="110fb-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="110fb-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110fb-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="110fb-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="110fb-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="110fb-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="110fb-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="110fb-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="110fb-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
