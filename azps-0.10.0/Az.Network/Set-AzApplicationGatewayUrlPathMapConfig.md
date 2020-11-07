---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924238"
---
# <span data-ttu-id="b4cae-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4cae-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b4cae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4cae-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cae-103">Anger konfiguration för en matris med URL-sökvägar till backend-server.</span><span class="sxs-lookup"><span data-stu-id="b4cae-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b4cae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4cae-104">SYNTAX</span></span>

### <span data-ttu-id="b4cae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4cae-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4cae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4cae-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4cae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4cae-107">DESCRIPTION</span></span>
<span data-ttu-id="b4cae-108">Cmdleten **set-AzApplicationGatewayUrlPathMapConfig** anger konfiguration för en matris med URL-sökvägar till en Server grupp.</span><span class="sxs-lookup"><span data-stu-id="b4cae-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b4cae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4cae-109">EXAMPLES</span></span>

### <span data-ttu-id="b4cae-110">9.1</span><span class="sxs-lookup"><span data-stu-id="b4cae-110">1:</span></span>
```

```

## <span data-ttu-id="b4cae-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4cae-111">PARAMETERS</span></span>

### <span data-ttu-id="b4cae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4cae-112">-ApplicationGateway</span></span>
<span data-ttu-id="b4cae-113">Anger den Programgateway till vilken denna cmdlet ställer in en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="b4cae-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="b4cae-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4cae-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="b4cae-115">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="b4cae-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b4cae-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b4cae-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="b4cae-117">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="b4cae-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="b4cae-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b4cae-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="b4cae-119">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="b4cae-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b4cae-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b4cae-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="b4cae-121">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="b4cae-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="b4cae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cae-122">-DefaultProfile</span></span>
<span data-ttu-id="b4cae-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4cae-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4cae-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4cae-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="b4cae-125">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b4cae-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b4cae-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4cae-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="b4cae-127">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4cae-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b4cae-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4cae-128">-Name</span></span>
<span data-ttu-id="b4cae-129">Anger namnet på den URL-sökväg där cmdlet ställer in konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="b4cae-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="b4cae-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="b4cae-130">-PathRules</span></span>
<span data-ttu-id="b4cae-131">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="b4cae-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="b4cae-132">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="b4cae-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="b4cae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cae-133">CommonParameters</span></span>
<span data-ttu-id="b4cae-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4cae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cae-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4cae-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cae-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4cae-136">INPUTS</span></span>

### <span data-ttu-id="b4cae-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4cae-137">PSApplicationGateway</span></span>
<span data-ttu-id="b4cae-138">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b4cae-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b4cae-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4cae-139">OUTPUTS</span></span>

### <span data-ttu-id="b4cae-140">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4cae-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4cae-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4cae-141">NOTES</span></span>

## <span data-ttu-id="b4cae-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4cae-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4cae-143">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4cae-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b4cae-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4cae-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b4cae-145">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4cae-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b4cae-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b4cae-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


