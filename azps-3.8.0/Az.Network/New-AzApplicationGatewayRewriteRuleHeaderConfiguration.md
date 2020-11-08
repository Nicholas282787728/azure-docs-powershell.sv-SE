---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092509"
---
# <span data-ttu-id="89e32-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="89e32-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="89e32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89e32-102">SYNOPSIS</span></span>
<span data-ttu-id="89e32-103">Skapar en omskrivnings huvud konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="89e32-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="89e32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89e32-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89e32-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89e32-105">DESCRIPTION</span></span>
<span data-ttu-id="89e32-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration** -cmdleten skapar en åtgärd för att skriva om en regel för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="89e32-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="89e32-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89e32-107">EXAMPLES</span></span>

### <span data-ttu-id="89e32-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89e32-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="89e32-109">Det här kommandot skapar en rapport huvud konfiguration och lagrar resultatet i variabeln som heter $hc.</span><span class="sxs-lookup"><span data-stu-id="89e32-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="89e32-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89e32-110">PARAMETERS</span></span>

### <span data-ttu-id="89e32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e32-111">-DefaultProfile</span></span>
<span data-ttu-id="89e32-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89e32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89e32-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="89e32-113">-HeaderName</span></span>
<span data-ttu-id="89e32-114">Namn på den rubrik som ska skrivas om</span><span class="sxs-lookup"><span data-stu-id="89e32-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="89e32-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="89e32-115">-HeaderValue</span></span>
<span data-ttu-id="89e32-116">Rubrik värde till angivet rubrik namn.</span><span class="sxs-lookup"><span data-stu-id="89e32-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="89e32-117">Huvudet tas bort om det utelämnas</span><span class="sxs-lookup"><span data-stu-id="89e32-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="89e32-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e32-118">CommonParameters</span></span>
<span data-ttu-id="89e32-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e32-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e32-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e32-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e32-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89e32-121">INPUTS</span></span>

### <span data-ttu-id="89e32-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="89e32-122">None</span></span>

## <span data-ttu-id="89e32-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89e32-123">OUTPUTS</span></span>

### <span data-ttu-id="89e32-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="89e32-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="89e32-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89e32-125">NOTES</span></span>

## <span data-ttu-id="89e32-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89e32-126">RELATED LINKS</span></span>

[<span data-ttu-id="89e32-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="89e32-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="89e32-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="89e32-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="89e32-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="89e32-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="89e32-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="89e32-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="89e32-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="89e32-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="89e32-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="89e32-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="89e32-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="89e32-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
