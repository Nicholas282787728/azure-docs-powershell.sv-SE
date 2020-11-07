---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918647"
---
# <span data-ttu-id="26caa-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="26caa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26caa-102">SYNOPSIS</span></span>
<span data-ttu-id="26caa-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="26caa-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="26caa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26caa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26caa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26caa-105">DESCRIPTION</span></span>
<span data-ttu-id="26caa-106">Cmdleten **New-AzApplicationGatewayRewriteRuleSet** skapar en regel uppsättning för att skriva om för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="26caa-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="26caa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26caa-107">EXAMPLES</span></span>

### <span data-ttu-id="26caa-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26caa-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="26caa-109">Det här kommandot skapar en regel uppsättning med namnet ruleset1 och lagrar resultatet i variabeln som heter $ruleset.</span><span class="sxs-lookup"><span data-stu-id="26caa-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="26caa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26caa-110">PARAMETERS</span></span>

### <span data-ttu-id="26caa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26caa-111">-DefaultProfile</span></span>
<span data-ttu-id="26caa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26caa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26caa-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="26caa-113">-Name</span></span>
<span data-ttu-id="26caa-114">Namnet på RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="26caa-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="26caa-115">-RewriteRule</span></span>
<span data-ttu-id="26caa-116">Lista över omskrivnings regler</span><span class="sxs-lookup"><span data-stu-id="26caa-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="26caa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26caa-117">CommonParameters</span></span>
<span data-ttu-id="26caa-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26caa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26caa-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26caa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26caa-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26caa-120">INPUTS</span></span>

### <span data-ttu-id="26caa-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="26caa-121">None</span></span>

## <span data-ttu-id="26caa-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26caa-122">OUTPUTS</span></span>

### <span data-ttu-id="26caa-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="26caa-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26caa-124">NOTES</span></span>

## <span data-ttu-id="26caa-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26caa-125">RELATED LINKS</span></span>

[<span data-ttu-id="26caa-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26caa-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26caa-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26caa-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26caa-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="26caa-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="26caa-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="26caa-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="26caa-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="26caa-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
