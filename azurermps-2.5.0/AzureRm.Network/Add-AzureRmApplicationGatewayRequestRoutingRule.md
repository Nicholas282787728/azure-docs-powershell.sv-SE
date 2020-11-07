---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: fdbbb28d69d5094b52d8ac7340839fa570bce55d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929053"
---
# <span data-ttu-id="36241-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36241-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="36241-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36241-102">SYNOPSIS</span></span>
<span data-ttu-id="36241-103">Lägger till en adresslisteregel till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="36241-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36241-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36241-104">SYNTAX</span></span>

### <span data-ttu-id="36241-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36241-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36241-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="36241-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36241-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36241-107">DESCRIPTION</span></span>
<span data-ttu-id="36241-108">Cmdleten **Add-AzureRmApplicationGatewayRequestRoutingRule** lägger till en regel för anslutningsbegäran till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="36241-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="36241-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36241-109">EXAMPLES</span></span>

### <span data-ttu-id="36241-110">Exempel 1: lägga till en operationsföljdslänkkod i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="36241-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="36241-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="36241-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="36241-112">Med det andra kommandot läggs regeln för anslutningsbegäran till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="36241-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="36241-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36241-113">PARAMETERS</span></span>

### <span data-ttu-id="36241-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36241-114">-ApplicationGateway</span></span>
<span data-ttu-id="36241-115">Anger en Programgateway som denna cmdlet lägger till en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="36241-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36241-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="36241-116">-BackendAddressPool</span></span>
<span data-ttu-id="36241-117">Anger ett objekt för en Programgateway-backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="36241-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="36241-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="36241-119">Anger en Programgateway-adresspool-ID.</span><span class="sxs-lookup"><span data-stu-id="36241-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="36241-120">-BackendHttpSettings</span></span>
<span data-ttu-id="36241-121">Anger ett backend-objekt med HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="36241-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="36241-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="36241-123">Anger ett ID för HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="36241-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36241-124">-DefaultProfile</span></span>
<span data-ttu-id="36241-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36241-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="36241-126">-HttpListener</span></span>
<span data-ttu-id="36241-127">Anger HTTP Listener-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="36241-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="36241-128">-HttpListenerId</span></span>
<span data-ttu-id="36241-129">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="36241-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="36241-130">-Name</span></span>
<span data-ttu-id="36241-131">Anger namnet på regeln för routningsregler denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="36241-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="36241-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="36241-132">-RedirectConfiguration</span></span>
<span data-ttu-id="36241-133">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="36241-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="36241-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="36241-135">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="36241-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="36241-136">-RuleType</span></span>
<span data-ttu-id="36241-137">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="36241-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="36241-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="36241-139">-UrlPathMapId</span></span>
<span data-ttu-id="36241-140">Anger URL-sökvägen för kart regeln.</span><span class="sxs-lookup"><span data-stu-id="36241-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36241-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36241-141">CommonParameters</span></span>
<span data-ttu-id="36241-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36241-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36241-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36241-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36241-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36241-144">INPUTS</span></span>

### <span data-ttu-id="36241-145">System. String</span><span class="sxs-lookup"><span data-stu-id="36241-145">System.String</span></span>

## <span data-ttu-id="36241-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36241-146">OUTPUTS</span></span>

### <span data-ttu-id="36241-147">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36241-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36241-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36241-148">NOTES</span></span>

## <span data-ttu-id="36241-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36241-149">RELATED LINKS</span></span>

[<span data-ttu-id="36241-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36241-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="36241-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36241-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="36241-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36241-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="36241-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="36241-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


