---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521892"
---
# <span data-ttu-id="94ade-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="94ade-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94ade-102">SYNOPSIS</span></span>
<span data-ttu-id="94ade-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="94ade-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="94ade-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94ade-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94ade-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94ade-105">DESCRIPTION</span></span>
<span data-ttu-id="94ade-106">Cmdleten **New-AzApplicationGatewayRewriteRuleSet** skapar en regel uppsättning för att skriva om för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="94ade-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="94ade-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94ade-107">EXAMPLES</span></span>

### <span data-ttu-id="94ade-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94ade-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="94ade-109">Det här kommandot skapar en regel uppsättning med namnet ruleset1 och lagrar resultatet i variabeln som heter $ruleset.</span><span class="sxs-lookup"><span data-stu-id="94ade-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="94ade-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94ade-110">PARAMETERS</span></span>

### <span data-ttu-id="94ade-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ade-111">-DefaultProfile</span></span>
<span data-ttu-id="94ade-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94ade-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ade-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="94ade-113">-Name</span></span>
<span data-ttu-id="94ade-114">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="94ade-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="94ade-115">-RewriteRule</span></span>
<span data-ttu-id="94ade-116">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="94ade-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="94ade-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ade-117">CommonParameters</span></span>
<span data-ttu-id="94ade-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ade-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ade-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ade-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ade-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94ade-120">INPUTS</span></span>

### <span data-ttu-id="94ade-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="94ade-121">None</span></span>

## <span data-ttu-id="94ade-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94ade-122">OUTPUTS</span></span>

### <span data-ttu-id="94ade-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="94ade-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94ade-124">NOTES</span></span>

## <span data-ttu-id="94ade-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94ade-125">RELATED LINKS</span></span>

[<span data-ttu-id="94ade-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="94ade-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="94ade-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="94ade-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94ade-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="94ade-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="94ade-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="94ade-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="94ade-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="94ade-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="94ade-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
