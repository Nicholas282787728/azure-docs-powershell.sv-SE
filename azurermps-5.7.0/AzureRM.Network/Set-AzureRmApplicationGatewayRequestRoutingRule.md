---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: fb171429e6b704964e0bbff68d301cc5f712c185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574251"
---
# <span data-ttu-id="c0e70-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0e70-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c0e70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0e70-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e70-103">Ändrar regeln för en anslutningsbegäran för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c0e70-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0e70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0e70-104">SYNTAX</span></span>

### <span data-ttu-id="c0e70-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e70-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0e70-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c0e70-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0e70-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0e70-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e70-108">Cmdleten **set-AzureRmApplicationGatewayRequestRoutingRule** ändrar en regel för en anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="c0e70-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="c0e70-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0e70-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e70-110">Exempel 1: uppdatera en regel för en anslutningsbegäran</span><span class="sxs-lookup"><span data-stu-id="c0e70-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c0e70-111">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="c0e70-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c0e70-112">Det andra kommandot ändrar regeln för anslutningsbegäran för Application Gateway för användning av backend-HTTP-inställningar som anges i $Setting variabel, en HTTP-lyssnare som anges i $Listener-variabeln och en backend-adresspool som angetts i $Pool variabeln.</span><span class="sxs-lookup"><span data-stu-id="c0e70-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="c0e70-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0e70-113">PARAMETERS</span></span>

### <span data-ttu-id="c0e70-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0e70-114">-ApplicationGateway</span></span>
<span data-ttu-id="c0e70-115">Anger det Application Gateway-objekt som denna cmdlet associerar en anslutningsbegäran för.</span><span class="sxs-lookup"><span data-stu-id="c0e70-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="c0e70-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c0e70-116">-BackendAddressPool</span></span>
<span data-ttu-id="c0e70-117">Anger backend-adresspoolen för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c0e70-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="c0e70-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c0e70-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c0e70-119">Anger programgatewayens backend-ID.</span><span class="sxs-lookup"><span data-stu-id="c0e70-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="c0e70-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c0e70-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c0e70-121">Anger Server delen för Programgateway-HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="c0e70-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="c0e70-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c0e70-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c0e70-123">Anger backend-ID för HTTP-inställningar för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c0e70-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="c0e70-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e70-124">-DefaultProfile</span></span>
<span data-ttu-id="c0e70-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e70-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e70-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c0e70-126">-HttpListener</span></span>
<span data-ttu-id="c0e70-127">Anger HTTP-lyssnaren för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c0e70-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="c0e70-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c0e70-128">-HttpListenerId</span></span>
<span data-ttu-id="c0e70-129">Anger HTTP-lyssnar-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c0e70-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="c0e70-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0e70-130">-Name</span></span>
<span data-ttu-id="c0e70-131">Anger namnet på regeln för anslutningsbegäran som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c0e70-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c0e70-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0e70-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c0e70-133">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c0e70-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c0e70-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c0e70-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c0e70-135">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0e70-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c0e70-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c0e70-136">-RuleType</span></span>
<span data-ttu-id="c0e70-137">Anger typen för routningsregler för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="c0e70-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="c0e70-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c0e70-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="c0e70-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c0e70-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="c0e70-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e70-140">CommonParameters</span></span>
<span data-ttu-id="c0e70-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e70-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e70-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e70-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e70-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0e70-143">INPUTS</span></span>

### <span data-ttu-id="c0e70-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e70-144">System.String</span></span>

## <span data-ttu-id="c0e70-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0e70-145">OUTPUTS</span></span>

### <span data-ttu-id="c0e70-146">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0e70-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0e70-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0e70-147">NOTES</span></span>

## <span data-ttu-id="c0e70-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0e70-148">RELATED LINKS</span></span>

[<span data-ttu-id="c0e70-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0e70-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c0e70-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0e70-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c0e70-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0e70-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c0e70-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0e70-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


