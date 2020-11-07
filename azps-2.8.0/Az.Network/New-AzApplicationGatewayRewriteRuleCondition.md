---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918652"
---
# <span data-ttu-id="6e30e-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6e30e-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="6e30e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e30e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e30e-103">Lägger till ett villkor i RewriteRule för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6e30e-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="6e30e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e30e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e30e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e30e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e30e-106">**AzApplicationGatewayRewriteRuleCondition** -cmdleten skapar ett villkor för att skapa en regel för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6e30e-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="6e30e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e30e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e30e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e30e-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="6e30e-109">Det här kommandot skapar ett villkor i en återskrivning-regel och lagrar resultatet i variabeln som heter $condition.</span><span class="sxs-lookup"><span data-stu-id="6e30e-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="6e30e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e30e-110">PARAMETERS</span></span>

### <span data-ttu-id="6e30e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e30e-111">-DefaultProfile</span></span>
<span data-ttu-id="6e30e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e30e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e30e-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="6e30e-113">-IgnoreCase</span></span>
<span data-ttu-id="6e30e-114">Ställ in den här flaggan så att den ignoreras i mönstret</span><span class="sxs-lookup"><span data-stu-id="6e30e-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e30e-115">-Minus</span><span class="sxs-lookup"><span data-stu-id="6e30e-115">-Negate</span></span>
<span data-ttu-id="6e30e-116">Ställ in den här flaggan för att negera villkors verifieringen</span><span class="sxs-lookup"><span data-stu-id="6e30e-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e30e-117">-Mönster</span><span class="sxs-lookup"><span data-stu-id="6e30e-117">-Pattern</span></span>
<span data-ttu-id="6e30e-118">Mönster att leta efter i variabel huvudet</span><span class="sxs-lookup"><span data-stu-id="6e30e-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e30e-119">-Variabel</span><span class="sxs-lookup"><span data-stu-id="6e30e-119">-Variable</span></span>
<span data-ttu-id="6e30e-120">Rubrikens namn för att ange villkoret</span><span class="sxs-lookup"><span data-stu-id="6e30e-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e30e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e30e-121">CommonParameters</span></span>
<span data-ttu-id="6e30e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e30e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6e30e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e30e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e30e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e30e-124">INPUTS</span></span>

### <span data-ttu-id="6e30e-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="6e30e-125">None</span></span>

## <span data-ttu-id="6e30e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e30e-126">OUTPUTS</span></span>

### <span data-ttu-id="6e30e-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6e30e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="6e30e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e30e-128">NOTES</span></span>

## <span data-ttu-id="6e30e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e30e-129">RELATED LINKS</span></span>
[<span data-ttu-id="6e30e-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6e30e-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6e30e-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6e30e-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6e30e-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6e30e-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6e30e-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="6e30e-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6e30e-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
