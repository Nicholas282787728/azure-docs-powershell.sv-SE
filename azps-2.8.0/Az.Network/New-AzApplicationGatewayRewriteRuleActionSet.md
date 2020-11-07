---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918655"
---
# <span data-ttu-id="af781-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af781-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="af781-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af781-102">SYNOPSIS</span></span>
<span data-ttu-id="af781-103">Skapar en åtgärd för att skriva om en regel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="af781-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="af781-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af781-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af781-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af781-105">DESCRIPTION</span></span>
<span data-ttu-id="af781-106">Cmdleten **New-AzApplicationGatewayRewriteRuleActionSet** skapar en åtgärd för att skriva om en regel för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="af781-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="af781-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af781-107">EXAMPLES</span></span>

### <span data-ttu-id="af781-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af781-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="af781-109">Det här kommandot skapar en instruktion för att skriva om en regel och lagrar resultatet i variabeln som heter $action.</span><span class="sxs-lookup"><span data-stu-id="af781-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="af781-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af781-110">PARAMETERS</span></span>

### <span data-ttu-id="af781-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af781-111">-DefaultProfile</span></span>
<span data-ttu-id="af781-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af781-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af781-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af781-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="af781-114">Lista med konfigurationer för begärandehuvuden</span><span class="sxs-lookup"><span data-stu-id="af781-114">List of request header configurations</span></span>

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

### <span data-ttu-id="af781-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af781-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="af781-116">Lista med konfigurationer för svarshuvuden</span><span class="sxs-lookup"><span data-stu-id="af781-116">List of response header configurations</span></span>

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

### <span data-ttu-id="af781-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af781-117">CommonParameters</span></span>
<span data-ttu-id="af781-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af781-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af781-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af781-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af781-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af781-120">INPUTS</span></span>

### <span data-ttu-id="af781-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="af781-121">None</span></span>

## <span data-ttu-id="af781-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af781-122">OUTPUTS</span></span>

### <span data-ttu-id="af781-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af781-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="af781-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af781-124">NOTES</span></span>

## <span data-ttu-id="af781-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af781-125">RELATED LINKS</span></span>

[<span data-ttu-id="af781-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af781-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af781-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af781-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af781-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af781-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af781-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af781-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af781-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af781-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="af781-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="af781-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="af781-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af781-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
