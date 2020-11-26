---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324671"
---
# <span data-ttu-id="cc217-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc217-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="cc217-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc217-102">SYNOPSIS</span></span>
<span data-ttu-id="cc217-103">Skapar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="cc217-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cc217-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc217-104">SYNTAX</span></span>

### <span data-ttu-id="cc217-105">BackendSetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="cc217-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc217-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc217-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc217-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="cc217-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc217-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc217-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc217-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc217-109">DESCRIPTION</span></span>
<span data-ttu-id="cc217-110">Cmdleten **New-AzApplicationGatewayUrlPathMapConfig** skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="cc217-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cc217-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc217-111">EXAMPLES</span></span>

### <span data-ttu-id="cc217-112">Exempel 1: skapa en matris med URL-sökvägar till en backend-server</span><span class="sxs-lookup"><span data-stu-id="cc217-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="cc217-113">Det här kommandot skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="cc217-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cc217-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc217-114">PARAMETERS</span></span>

### <span data-ttu-id="cc217-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cc217-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="cc217-116">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="cc217-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cc217-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="cc217-118">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="cc217-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cc217-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="cc217-120">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="cc217-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="cc217-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="cc217-122">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="cc217-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc217-123">-DefaultProfile</span></span>
<span data-ttu-id="cc217-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc217-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc217-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc217-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="cc217-126">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cc217-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cc217-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="cc217-128">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc217-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc217-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="cc217-130">Standard regel uppsättning för Programgateway</span><span class="sxs-lookup"><span data-stu-id="cc217-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="cc217-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="cc217-132">ID för Application Gateway standard regel för omskrivning</span><span class="sxs-lookup"><span data-stu-id="cc217-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc217-133">-Name</span></span>
<span data-ttu-id="cc217-134">Anger namnet på URL-sökvägen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="cc217-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cc217-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="cc217-135">-PathRules</span></span>
<span data-ttu-id="cc217-136">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="cc217-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="cc217-137">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="cc217-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc217-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc217-138">CommonParameters</span></span>
<span data-ttu-id="cc217-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc217-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc217-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc217-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc217-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc217-141">INPUTS</span></span>

### <span data-ttu-id="cc217-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="cc217-142">None</span></span>

## <span data-ttu-id="cc217-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc217-143">OUTPUTS</span></span>

### <span data-ttu-id="cc217-144">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="cc217-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="cc217-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc217-145">NOTES</span></span>

## <span data-ttu-id="cc217-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc217-146">RELATED LINKS</span></span>

[<span data-ttu-id="cc217-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc217-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc217-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc217-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc217-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc217-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cc217-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cc217-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

