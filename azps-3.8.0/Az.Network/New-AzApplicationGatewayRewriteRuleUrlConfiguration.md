---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092498"
---
# <span data-ttu-id="7f16e-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f16e-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="7f16e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f16e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f16e-103">Skapar en URL-konfiguration för en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7f16e-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="7f16e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f16e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f16e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f16e-105">DESCRIPTION</span></span>
<span data-ttu-id="7f16e-106">**Med AzApplicationGatewayRewriteRuleUrlConfiguration** -cmdleten skapas en URL-konfiguration för omskrivning av regler för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f16e-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="7f16e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f16e-107">EXAMPLES</span></span>

### <span data-ttu-id="7f16e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f16e-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="7f16e-109">Det här kommandot skapar en URL-konfiguration för en omskrivning av en regel och lagrar resultatet i variabeln som heter $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f16e-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="7f16e-110">Om du vill uppdatera en befintlig UrlConfiguration kan du göra det genom att skapa en ny UrlConfiguration och tilldela den nya UrlConfiguration till egenskapen UrlConfiguration för åtgärden Skriv om regel.</span><span class="sxs-lookup"><span data-stu-id="7f16e-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="7f16e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f16e-111">PARAMETERS</span></span>

### <span data-ttu-id="7f16e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f16e-112">-DefaultProfile</span></span>
<span data-ttu-id="7f16e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f16e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f16e-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="7f16e-114">-ModifiedPath</span></span>
<span data-ttu-id="7f16e-115">Värde för URL-sökväg.</span><span class="sxs-lookup"><span data-stu-id="7f16e-115">Url path value.</span></span>

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

### <span data-ttu-id="7f16e-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="7f16e-116">-ModifiedQueryString</span></span>
<span data-ttu-id="7f16e-117">URL-Frågesträngens värde.</span><span class="sxs-lookup"><span data-stu-id="7f16e-117">Url query string value.</span></span>

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

### <span data-ttu-id="7f16e-118">-Omdirigera</span><span class="sxs-lookup"><span data-stu-id="7f16e-118">-Reroute</span></span>
<span data-ttu-id="7f16e-119">Flagga för att utvärdera URL-sökvägen som visas i sökväg baserat på routningsregler med den ändrade sökvägen.</span><span class="sxs-lookup"><span data-stu-id="7f16e-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f16e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f16e-120">CommonParameters</span></span>
<span data-ttu-id="7f16e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f16e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f16e-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f16e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f16e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f16e-123">INPUTS</span></span>

### <span data-ttu-id="7f16e-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="7f16e-124">None</span></span>

## <span data-ttu-id="7f16e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f16e-125">OUTPUTS</span></span>

### <span data-ttu-id="7f16e-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f16e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="7f16e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f16e-127">NOTES</span></span>

## <span data-ttu-id="7f16e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f16e-128">RELATED LINKS</span></span>

[<span data-ttu-id="7f16e-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f16e-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f16e-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f16e-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f16e-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f16e-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7f16e-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7f16e-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7f16e-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)