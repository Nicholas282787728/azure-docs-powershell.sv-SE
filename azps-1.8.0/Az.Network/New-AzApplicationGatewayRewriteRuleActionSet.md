---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748114"
---
# <span data-ttu-id="79b4f-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="79b4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="79b4f-103">Skapar en actionset för att skriva om en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="79b4f-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="79b4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79b4f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79b4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="79b4f-106">Cmdleten **New-AzApplicationGatewayRewriteRuleActionSet** skapar en Rewrite Rule-actionset för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79b4f-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="79b4f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79b4f-107">EXAMPLES</span></span>

### <span data-ttu-id="79b4f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79b4f-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="79b4f-109">Det här kommandot skapar en actionset och lagrar resultatet i variabeln som heter $action.</span><span class="sxs-lookup"><span data-stu-id="79b4f-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="79b4f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79b4f-110">PARAMETERS</span></span>

### <span data-ttu-id="79b4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b4f-111">-DefaultProfile</span></span>
<span data-ttu-id="79b4f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79b4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b4f-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b4f-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="79b4f-114">Lista med konfigurationer för begärandehuvuden</span><span class="sxs-lookup"><span data-stu-id="79b4f-114">List of request header configurations</span></span>

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

### <span data-ttu-id="79b4f-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b4f-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="79b4f-116">Lista med konfigurationer för svarshuvuden</span><span class="sxs-lookup"><span data-stu-id="79b4f-116">List of response header configurations</span></span>

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

### <span data-ttu-id="79b4f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b4f-117">CommonParameters</span></span>
<span data-ttu-id="79b4f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b4f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b4f-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b4f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b4f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79b4f-120">INPUTS</span></span>

### <span data-ttu-id="79b4f-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="79b4f-121">None</span></span>

## <span data-ttu-id="79b4f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79b4f-122">OUTPUTS</span></span>

### <span data-ttu-id="79b4f-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="79b4f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79b4f-124">NOTES</span></span>

## <span data-ttu-id="79b4f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79b4f-125">RELATED LINKS</span></span>

[<span data-ttu-id="79b4f-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79b4f-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79b4f-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79b4f-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79b4f-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79b4f-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79b4f-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="79b4f-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="79b4f-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b4f-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
