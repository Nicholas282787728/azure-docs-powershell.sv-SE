---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409763"
---
# <span data-ttu-id="b4e03-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="b4e03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4e03-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e03-103">Skapar en åtgärd för att skriva om en regel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b4e03-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="b4e03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4e03-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4e03-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e03-106">Cmdleten **New-AzApplicationGatewayRewriteRuleActionSet** skapar en åtgärd för att skriva om en regel för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4e03-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="b4e03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4e03-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e03-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4e03-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="b4e03-109">Det här kommandot skapar en instruktion för att skriva om en regel och lagrar resultatet i variabeln som heter $action.</span><span class="sxs-lookup"><span data-stu-id="b4e03-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="b4e03-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4e03-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e03-111">-DefaultProfile</span></span>
<span data-ttu-id="b4e03-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e03-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e03-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="b4e03-114">Lista med konfigurationer för begärandehuvuden</span><span class="sxs-lookup"><span data-stu-id="b4e03-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e03-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e03-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="b4e03-116">Lista med konfigurationer för svarshuvuden</span><span class="sxs-lookup"><span data-stu-id="b4e03-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e03-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e03-117">-UrlConfiguration</span></span>
<span data-ttu-id="b4e03-118">URL-konfiguration för åtgärds uppsättning</span><span class="sxs-lookup"><span data-stu-id="b4e03-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e03-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e03-119">CommonParameters</span></span>
<span data-ttu-id="b4e03-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e03-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e03-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e03-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e03-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4e03-122">INPUTS</span></span>

### <span data-ttu-id="b4e03-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4e03-123">None</span></span>

## <span data-ttu-id="b4e03-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4e03-124">OUTPUTS</span></span>

### <span data-ttu-id="b4e03-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="b4e03-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4e03-126">NOTES</span></span>

## <span data-ttu-id="b4e03-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4e03-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4e03-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4e03-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4e03-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4e03-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4e03-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4e03-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b4e03-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b4e03-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b4e03-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e03-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="b4e03-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e03-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)