---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409771"
---
# <span data-ttu-id="ff059-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ff059-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff059-102">SYNOPSIS</span></span>
<span data-ttu-id="ff059-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ff059-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="ff059-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff059-104">SYNTAX</span></span>

### <span data-ttu-id="ff059-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff059-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff059-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ff059-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff059-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff059-107">DESCRIPTION</span></span>
<span data-ttu-id="ff059-108">Cmdleten **Add-AzApplicationGatewayRequestRoutingRule** skapar en regel för en anslutningsbegäran för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff059-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="ff059-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff059-109">EXAMPLES</span></span>

### <span data-ttu-id="ff059-110">Exempel 1: skapa en regel för en anslutningsbegäran för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="ff059-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="ff059-111">Det här kommandot skapar en grundläggande Dirigerings regel med namnet Rule01 och lagrar resultatet i variabeln som heter $Rule.</span><span class="sxs-lookup"><span data-stu-id="ff059-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="ff059-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff059-112">PARAMETERS</span></span>

### <span data-ttu-id="ff059-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff059-113">-BackendAddressPool</span></span>
<span data-ttu-id="ff059-114">Anger backend-adresspoolen som ett objekt för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="ff059-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ff059-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="ff059-116">Anger backend-adressens adresspool-ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ff059-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ff059-117">-BackendHttpSettings</span></span>
<span data-ttu-id="ff059-118">Anger backend-HTTP-inställningar, som ett objekt, för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="ff059-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ff059-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="ff059-120">Anger backend HTTP-inställningar ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ff059-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff059-121">-DefaultProfile</span></span>
<span data-ttu-id="ff059-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff059-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff059-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ff059-123">-HttpListener</span></span>
<span data-ttu-id="ff059-124">Anger den backend-HTTP-lyssnaren som regeln för anslutningsbegäran kan skapa.</span><span class="sxs-lookup"><span data-stu-id="ff059-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="ff059-125">-HttpListenerId</span></span>
<span data-ttu-id="ff059-126">Anger Server delens HTTP-lyssnar-ID för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="ff059-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff059-127">-Name</span></span>
<span data-ttu-id="ff059-128">Anger namnet på regeln för anslutningsbegäran som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ff059-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ff059-129">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="ff059-129">-Priority</span></span>
<span data-ttu-id="ff059-130">Regelns prioritet</span><span class="sxs-lookup"><span data-stu-id="ff059-130">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff059-131">-RedirectConfiguration</span></span>
<span data-ttu-id="ff059-132">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ff059-132">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ff059-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="ff059-134">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff059-134">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff059-135">-RewriteRuleSet</span></span>
<span data-ttu-id="ff059-136">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ff059-136">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="ff059-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="ff059-138">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff059-138">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ff059-139">-RuleType</span></span>
<span data-ttu-id="ff059-140">Anger typen för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="ff059-140">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ff059-141">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="ff059-142">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff059-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff059-143">CommonParameters</span></span>
<span data-ttu-id="ff059-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff059-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff059-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff059-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff059-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff059-146">INPUTS</span></span>

### <span data-ttu-id="ff059-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff059-147">None</span></span>

## <span data-ttu-id="ff059-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff059-148">OUTPUTS</span></span>

### <span data-ttu-id="ff059-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ff059-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff059-150">NOTES</span></span>

## <span data-ttu-id="ff059-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff059-151">RELATED LINKS</span></span>

[<span data-ttu-id="ff059-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ff059-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ff059-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ff059-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff059-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


