---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397936"
---
# <span data-ttu-id="a5cd6-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5cd6-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="a5cd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cd6-103">Skapar en URL-konfiguration för en en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="a5cd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5cd6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5cd6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cd6-106">**Med AzApplicationGatewayRewriteRuleUrlConfiguration** -cmdleten skapas en URL-konfiguration för omskrivning av regler för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a5cd6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="a5cd6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5cd6-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="a5cd6-109">Det här kommandot skapar en URL-konfiguration för en omskrivning av en regel och lagrar resultatet i variabeln som heter $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="a5cd6-110">Om du vill uppdatera en befintlig UrlConfiguration kan du göra det genom att skapa en ny UrlConfiguration och tilldela den nya UrlConfiguration till egenskapen UrlConfiguration för åtgärden Skriv om regel.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="a5cd6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5cd6-111">PARAMETERS</span></span>

### <span data-ttu-id="a5cd6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cd6-112">-DefaultProfile</span></span>
<span data-ttu-id="a5cd6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5cd6-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="a5cd6-114">-ModifiedPath</span></span>
<span data-ttu-id="a5cd6-115">Värde för URL-sökväg.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-115">Url path value.</span></span>

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

### <span data-ttu-id="a5cd6-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="a5cd6-116">-ModifiedQueryString</span></span>
<span data-ttu-id="a5cd6-117">URL-Frågesträngens värde.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-117">Url query string value.</span></span>

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

### <span data-ttu-id="a5cd6-118">-Omdirigera</span><span class="sxs-lookup"><span data-stu-id="a5cd6-118">-Reroute</span></span>
<span data-ttu-id="a5cd6-119">Flagga för att utvärdera URL-sökvägen som visas i sökväg baserat på routningsregler med den ändrade sökvägen.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="a5cd6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cd6-120">CommonParameters</span></span>
<span data-ttu-id="a5cd6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cd6-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cd6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5cd6-123">INPUTS</span></span>

### <span data-ttu-id="a5cd6-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5cd6-124">None</span></span>

## <span data-ttu-id="a5cd6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5cd6-125">OUTPUTS</span></span>

### <span data-ttu-id="a5cd6-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5cd6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="a5cd6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5cd6-127">NOTES</span></span>

## <span data-ttu-id="a5cd6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5cd6-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5cd6-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5cd6-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5cd6-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5cd6-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5cd6-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a5cd6-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a5cd6-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a5cd6-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a5cd6-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)