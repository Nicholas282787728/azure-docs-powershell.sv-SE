---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918953"
---
# <span data-ttu-id="7bd5e-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7bd5e-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7bd5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd5e-103">Ändrar regeln för en anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="7bd5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bd5e-104">SYNTAX</span></span>

### <span data-ttu-id="7bd5e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd5e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7bd5e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd5e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bd5e-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd5e-108">Cmdleten **set-AzApplicationGatewayRequestRoutingRule** ändrar en regel för en anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="7bd5e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bd5e-109">EXAMPLES</span></span>

### <span data-ttu-id="7bd5e-110">Exempel 1: uppdatera en regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="7bd5e-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="7bd5e-111">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7bd5e-112">Det andra kommandot ändrar regeln för anslutningsbegäran för Application Gateway för användning av backend-HTTP-inställningar som anges i $Setting variabel, en HTTP-lyssnare som anges i $Listener-variabeln och en backend-adresspool som angetts i $Pool variabeln.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="7bd5e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bd5e-113">PARAMETERS</span></span>

### <span data-ttu-id="7bd5e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bd5e-114">-ApplicationGateway</span></span>
<span data-ttu-id="7bd5e-115">Anger det Application Gateway-objekt som denna cmdlet associerar en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd5e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7bd5e-116">-BackendAddressPool</span></span>
<span data-ttu-id="7bd5e-117">Anger backend-adresspoolen för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="7bd5e-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="7bd5e-119">Anger programgatewayens backend-ID.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="7bd5e-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7bd5e-120">-BackendHttpSettings</span></span>
<span data-ttu-id="7bd5e-121">Anger Server delen för Programgateway-HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="7bd5e-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="7bd5e-123">Anger backend-ID för HTTP-inställningar för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="7bd5e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd5e-124">-DefaultProfile</span></span>
<span data-ttu-id="7bd5e-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bd5e-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7bd5e-126">-HttpListener</span></span>
<span data-ttu-id="7bd5e-127">Anger HTTP-lyssnaren för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="7bd5e-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-128">-HttpListenerId</span></span>
<span data-ttu-id="7bd5e-129">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="7bd5e-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bd5e-130">-Name</span></span>
<span data-ttu-id="7bd5e-131">Anger namnet på regeln för anslutningsbegäran som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7bd5e-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bd5e-132">-RedirectConfiguration</span></span>
<span data-ttu-id="7bd5e-133">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7bd5e-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7bd5e-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="7bd5e-135">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bd5e-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7bd5e-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7bd5e-136">-RewriteRuleSet</span></span>
<span data-ttu-id="7bd5e-137">RewriteRuleSet för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7bd5e-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="7bd5e-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="7bd5e-139">ID för Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7bd5e-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="7bd5e-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="7bd5e-140">-RuleType</span></span>
<span data-ttu-id="7bd5e-141">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="7bd5e-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7bd5e-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="7bd5e-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="7bd5e-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="7bd5e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd5e-144">CommonParameters</span></span>
<span data-ttu-id="7bd5e-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd5e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd5e-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd5e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd5e-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bd5e-147">INPUTS</span></span>

### <span data-ttu-id="7bd5e-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bd5e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7bd5e-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bd5e-149">OUTPUTS</span></span>

### <span data-ttu-id="7bd5e-150">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bd5e-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7bd5e-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bd5e-151">NOTES</span></span>

## <span data-ttu-id="7bd5e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bd5e-152">RELATED LINKS</span></span>

[<span data-ttu-id="7bd5e-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7bd5e-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7bd5e-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7bd5e-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7bd5e-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7bd5e-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7bd5e-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7bd5e-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


