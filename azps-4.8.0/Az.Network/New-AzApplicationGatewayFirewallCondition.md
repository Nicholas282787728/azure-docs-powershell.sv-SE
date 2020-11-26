---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260754"
---
# <span data-ttu-id="290f9-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="290f9-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="290f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="290f9-102">SYNOPSIS</span></span>
<span data-ttu-id="290f9-103">Skapar ett matchnings villkor för en anpassad regel</span><span class="sxs-lookup"><span data-stu-id="290f9-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="290f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="290f9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="290f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="290f9-105">DESCRIPTION</span></span>
<span data-ttu-id="290f9-106">**New-AzApplicationGatewayFirewallCondition** skapar ett matchnings villkor för den anpassade brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="290f9-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="290f9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="290f9-107">EXAMPLES</span></span>

### <span data-ttu-id="290f9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="290f9-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="290f9-109">Kommandot skapar ett nytt matchnings villkor med variabeln som definierats i $variable, operatorn är inställt och negation villkor är falskt, som kommer från inklusive gemener och trim, matchar svärdet ABC och CDE.</span><span class="sxs-lookup"><span data-stu-id="290f9-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="290f9-110">Det nya matchnings villkoret sparas i $condition.</span><span class="sxs-lookup"><span data-stu-id="290f9-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="290f9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="290f9-111">PARAMETERS</span></span>

### <span data-ttu-id="290f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="290f9-112">-DefaultProfile</span></span>
<span data-ttu-id="290f9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="290f9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="290f9-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="290f9-114">-MatchValue</span></span>
<span data-ttu-id="290f9-115">Match värde.</span><span class="sxs-lookup"><span data-stu-id="290f9-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290f9-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="290f9-116">-MatchVariable</span></span>
<span data-ttu-id="290f9-117">Lista över variabler som matchar.</span><span class="sxs-lookup"><span data-stu-id="290f9-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290f9-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="290f9-118">-NegationCondition</span></span>
<span data-ttu-id="290f9-119">Beskriver om det här är en negerad omständighet eller inte.</span><span class="sxs-lookup"><span data-stu-id="290f9-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290f9-120">-Operatör</span><span class="sxs-lookup"><span data-stu-id="290f9-120">-Operator</span></span>
<span data-ttu-id="290f9-121">Beskriver vilken operator som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="290f9-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290f9-122">-Omvandla</span><span class="sxs-lookup"><span data-stu-id="290f9-122">-Transform</span></span>
<span data-ttu-id="290f9-123">Lista över transformeringar.</span><span class="sxs-lookup"><span data-stu-id="290f9-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="290f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="290f9-124">CommonParameters</span></span>
<span data-ttu-id="290f9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="290f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="290f9-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="290f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="290f9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="290f9-127">INPUTS</span></span>

### <span data-ttu-id="290f9-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="290f9-128">None</span></span>

## <span data-ttu-id="290f9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="290f9-129">OUTPUTS</span></span>

### <span data-ttu-id="290f9-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="290f9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="290f9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="290f9-131">NOTES</span></span>

## <span data-ttu-id="290f9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="290f9-132">RELATED LINKS</span></span>