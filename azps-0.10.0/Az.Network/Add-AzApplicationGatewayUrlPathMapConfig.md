---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922426"
---
# <span data-ttu-id="6efb9-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6efb9-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6efb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6efb9-102">SYNOPSIS</span></span>
<span data-ttu-id="6efb9-103">Lägger till en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="6efb9-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6efb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6efb9-104">SYNTAX</span></span>

### <span data-ttu-id="6efb9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6efb9-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6efb9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6efb9-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6efb9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6efb9-107">DESCRIPTION</span></span>
<span data-ttu-id="6efb9-108">Cmdleten **Add-AzApplicationGatewayUrlPathMapConfig** lägger till en matris med URL-sökvägar till en adresspool Server.</span><span class="sxs-lookup"><span data-stu-id="6efb9-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="6efb9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6efb9-109">EXAMPLES</span></span>

### <span data-ttu-id="6efb9-110">9.1</span><span class="sxs-lookup"><span data-stu-id="6efb9-110">1:</span></span>
```

```

## <span data-ttu-id="6efb9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6efb9-111">PARAMETERS</span></span>

### <span data-ttu-id="6efb9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6efb9-112">-ApplicationGateway</span></span>
<span data-ttu-id="6efb9-113">Anger den Programgateway till vilken denna cmdlet lägger till en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="6efb9-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="6efb9-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6efb9-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="6efb9-115">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="6efb9-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6efb9-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6efb9-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="6efb9-117">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="6efb9-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="6efb9-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6efb9-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="6efb9-119">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="6efb9-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6efb9-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6efb9-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="6efb9-121">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="6efb9-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="6efb9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efb9-122">-DefaultProfile</span></span>
<span data-ttu-id="6efb9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6efb9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6efb9-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6efb9-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="6efb9-125">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6efb9-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6efb9-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6efb9-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="6efb9-127">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6efb9-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6efb9-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="6efb9-128">-Name</span></span>
<span data-ttu-id="6efb9-129">Anger namnet på URL-sökvägen som denna cmdlet lägger till i Server delen.</span><span class="sxs-lookup"><span data-stu-id="6efb9-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="6efb9-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="6efb9-130">-PathRules</span></span>
<span data-ttu-id="6efb9-131">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="6efb9-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="6efb9-132">Sök vägs reglerna är ordnings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="6efb9-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="6efb9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efb9-133">CommonParameters</span></span>
<span data-ttu-id="6efb9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efb9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efb9-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efb9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efb9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6efb9-136">INPUTS</span></span>

### <span data-ttu-id="6efb9-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6efb9-137">PSApplicationGateway</span></span>
<span data-ttu-id="6efb9-138">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6efb9-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6efb9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6efb9-139">OUTPUTS</span></span>

### <span data-ttu-id="6efb9-140">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6efb9-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6efb9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6efb9-141">NOTES</span></span>

## <span data-ttu-id="6efb9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6efb9-142">RELATED LINKS</span></span>

[<span data-ttu-id="6efb9-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6efb9-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6efb9-144">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6efb9-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6efb9-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6efb9-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6efb9-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6efb9-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


