---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929845"
---
# <span data-ttu-id="6d7be-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d7be-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6d7be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d7be-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7be-103">Lägger till en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="6d7be-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d7be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d7be-104">SYNTAX</span></span>

### <span data-ttu-id="6d7be-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d7be-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7be-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6d7be-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d7be-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d7be-107">DESCRIPTION</span></span>
<span data-ttu-id="6d7be-108">Cmdleten **Add-AzureRmApplicationGatewayUrlPathMapConfig** lägger till en matris med URL-sökvägar till en adresspool Server.</span><span class="sxs-lookup"><span data-stu-id="6d7be-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="6d7be-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d7be-109">EXAMPLES</span></span>

### <span data-ttu-id="6d7be-110">9.1</span><span class="sxs-lookup"><span data-stu-id="6d7be-110">1:</span></span>
```

```

## <span data-ttu-id="6d7be-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d7be-111">PARAMETERS</span></span>

### <span data-ttu-id="6d7be-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d7be-112">-ApplicationGateway</span></span>
<span data-ttu-id="6d7be-113">Anger den Programgateway till vilken denna cmdlet lägger till en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="6d7be-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="6d7be-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6d7be-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="6d7be-115">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="6d7be-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6d7be-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6d7be-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="6d7be-117">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="6d7be-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="6d7be-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6d7be-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="6d7be-119">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="6d7be-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6d7be-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6d7be-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="6d7be-121">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="6d7be-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="6d7be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7be-122">-DefaultProfile</span></span>
<span data-ttu-id="6d7be-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7be-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d7be-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d7be-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="6d7be-125">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6d7be-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6d7be-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6d7be-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="6d7be-127">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d7be-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6d7be-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d7be-128">-Name</span></span>
<span data-ttu-id="6d7be-129">Anger namnet på URL-sökvägen som denna cmdlet lägger till i Server delen.</span><span class="sxs-lookup"><span data-stu-id="6d7be-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="6d7be-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="6d7be-130">-PathRules</span></span>
<span data-ttu-id="6d7be-131">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="6d7be-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="6d7be-132">Sök vägs reglerna är ordnings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="6d7be-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="6d7be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7be-133">CommonParameters</span></span>
<span data-ttu-id="6d7be-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7be-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7be-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7be-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d7be-136">INPUTS</span></span>

### <span data-ttu-id="6d7be-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d7be-137">PSApplicationGateway</span></span>
<span data-ttu-id="6d7be-138">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6d7be-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6d7be-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d7be-139">OUTPUTS</span></span>

### <span data-ttu-id="6d7be-140">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d7be-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d7be-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d7be-141">NOTES</span></span>

## <span data-ttu-id="6d7be-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d7be-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d7be-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d7be-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6d7be-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d7be-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6d7be-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d7be-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6d7be-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d7be-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


