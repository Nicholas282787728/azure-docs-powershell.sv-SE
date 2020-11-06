---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 321c7272c02b4e5555f731d3a9dbaa7d806c0727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576918"
---
# <span data-ttu-id="72826-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="72826-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="72826-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72826-102">SYNOPSIS</span></span>
<span data-ttu-id="72826-103">Lägger till en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="72826-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72826-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72826-104">SYNTAX</span></span>

### <span data-ttu-id="72826-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72826-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72826-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72826-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72826-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72826-107">DESCRIPTION</span></span>
<span data-ttu-id="72826-108">Cmdleten **Add-AzureRmApplicationGatewayUrlPathMapConfig** lägger till en matris med URL-sökvägar till en adresspool Server.</span><span class="sxs-lookup"><span data-stu-id="72826-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="72826-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72826-109">EXAMPLES</span></span>

## <span data-ttu-id="72826-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72826-110">PARAMETERS</span></span>

### <span data-ttu-id="72826-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72826-111">-ApplicationGateway</span></span>
<span data-ttu-id="72826-112">Anger den Programgateway till vilken denna cmdlet lägger till en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="72826-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="72826-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72826-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="72826-114">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="72826-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="72826-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="72826-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="72826-116">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="72826-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="72826-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="72826-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="72826-118">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="72826-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="72826-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="72826-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="72826-120">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="72826-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="72826-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72826-121">-DefaultProfile</span></span>
<span data-ttu-id="72826-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72826-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72826-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="72826-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="72826-124">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="72826-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="72826-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="72826-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="72826-126">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="72826-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="72826-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="72826-127">-Name</span></span>
<span data-ttu-id="72826-128">Anger namnet på URL-sökvägen som denna cmdlet lägger till i Server delen.</span><span class="sxs-lookup"><span data-stu-id="72826-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="72826-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="72826-129">-PathRules</span></span>
<span data-ttu-id="72826-130">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="72826-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="72826-131">Sök vägs reglerna är ordnings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="72826-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72826-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72826-132">CommonParameters</span></span>
<span data-ttu-id="72826-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72826-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72826-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72826-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72826-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72826-135">INPUTS</span></span>

### <span data-ttu-id="72826-136">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72826-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="72826-137">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72826-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="72826-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72826-138">OUTPUTS</span></span>

### <span data-ttu-id="72826-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72826-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72826-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72826-140">NOTES</span></span>

## <span data-ttu-id="72826-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72826-141">RELATED LINKS</span></span>

[<span data-ttu-id="72826-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="72826-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="72826-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="72826-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="72826-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="72826-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="72826-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="72826-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


