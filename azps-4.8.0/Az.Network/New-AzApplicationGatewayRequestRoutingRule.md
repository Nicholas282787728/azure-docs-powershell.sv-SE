---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 8fc8f6785e9b6eda55615fb1e2ececbaf9ab0349
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262596"
---
# <span data-ttu-id="85c76-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="85c76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85c76-102">SYNOPSIS</span></span>
<span data-ttu-id="85c76-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="85c76-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="85c76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85c76-104">SYNTAX</span></span>

### <span data-ttu-id="85c76-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85c76-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85c76-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85c76-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c76-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85c76-107">DESCRIPTION</span></span>
<span data-ttu-id="85c76-108">Cmdleten **Add-AzApplicationGatewayRequestRoutingRule** skapar en regel för en anslutningsbegäran för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="85c76-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="85c76-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85c76-109">EXAMPLES</span></span>

### <span data-ttu-id="85c76-110">Exempel 1: skapa en regel för en anslutningsbegäran för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="85c76-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="85c76-111">Det här kommandot skapar en grundläggande Dirigerings regel med namnet Rule01 och lagrar resultatet i variabeln som heter $Rule.</span><span class="sxs-lookup"><span data-stu-id="85c76-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="85c76-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85c76-112">PARAMETERS</span></span>

### <span data-ttu-id="85c76-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85c76-113">-BackendAddressPool</span></span>
<span data-ttu-id="85c76-114">Anger backend-adresspoolen som ett objekt för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="85c76-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="85c76-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="85c76-116">Anger backend-adressens adresspool-ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="85c76-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="85c76-117">-BackendHttpSettings</span></span>
<span data-ttu-id="85c76-118">Anger backend-HTTP-inställningar, som ett objekt, för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="85c76-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="85c76-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="85c76-120">Anger backend HTTP-inställningar ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="85c76-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c76-121">-DefaultProfile</span></span>
<span data-ttu-id="85c76-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85c76-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c76-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="85c76-123">-HttpListener</span></span>
<span data-ttu-id="85c76-124">Anger den backend-HTTP-lyssnaren som regeln för anslutningsbegäran kan skapa.</span><span class="sxs-lookup"><span data-stu-id="85c76-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="85c76-125">-HttpListenerId</span></span>
<span data-ttu-id="85c76-126">Anger Server delens HTTP-lyssnar-ID för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="85c76-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="85c76-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="85c76-127">-Name</span></span>
<span data-ttu-id="85c76-128">Anger namnet på regeln för anslutningsbegäran som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="85c76-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="85c76-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="85c76-129">-RedirectConfiguration</span></span>
<span data-ttu-id="85c76-130">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="85c76-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="85c76-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="85c76-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="85c76-132">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="85c76-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="85c76-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c76-133">-RewriteRuleSet</span></span>
<span data-ttu-id="85c76-134">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="85c76-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="85c76-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="85c76-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="85c76-136">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85c76-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="85c76-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="85c76-137">-RuleType</span></span>
<span data-ttu-id="85c76-138">Anger typen för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="85c76-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="85c76-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="85c76-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="85c76-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="85c76-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="85c76-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c76-141">CommonParameters</span></span>
<span data-ttu-id="85c76-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c76-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c76-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c76-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c76-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85c76-144">INPUTS</span></span>

### <span data-ttu-id="85c76-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="85c76-145">None</span></span>

## <span data-ttu-id="85c76-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85c76-146">OUTPUTS</span></span>

### <span data-ttu-id="85c76-147">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="85c76-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85c76-148">NOTES</span></span>

## <span data-ttu-id="85c76-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85c76-149">RELATED LINKS</span></span>

[<span data-ttu-id="85c76-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="85c76-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="85c76-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="85c76-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85c76-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


