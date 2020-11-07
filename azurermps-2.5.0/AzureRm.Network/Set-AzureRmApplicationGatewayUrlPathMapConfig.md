---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930525"
---
# <span data-ttu-id="11ff6-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11ff6-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="11ff6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="11ff6-103">Anger konfiguration för en matris med URL-sökvägar till backend-server.</span><span class="sxs-lookup"><span data-stu-id="11ff6-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ff6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11ff6-104">SYNTAX</span></span>

### <span data-ttu-id="11ff6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11ff6-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ff6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11ff6-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11ff6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="11ff6-108">Cmdleten **set-AzureRmApplicationGatewayUrlPathMapConfig** anger konfiguration för en matris med URL-sökvägar till en Server grupp.</span><span class="sxs-lookup"><span data-stu-id="11ff6-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="11ff6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="11ff6-110">9.1</span><span class="sxs-lookup"><span data-stu-id="11ff6-110">1:</span></span>
```

```

## <span data-ttu-id="11ff6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11ff6-111">PARAMETERS</span></span>

### <span data-ttu-id="11ff6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11ff6-112">-ApplicationGateway</span></span>
<span data-ttu-id="11ff6-113">Anger den Programgateway till vilken denna cmdlet ställer in en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="11ff6-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="11ff6-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11ff6-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="11ff6-115">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="11ff6-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="11ff6-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="11ff6-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="11ff6-117">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="11ff6-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="11ff6-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="11ff6-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="11ff6-119">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="11ff6-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="11ff6-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="11ff6-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="11ff6-121">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="11ff6-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="11ff6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ff6-122">-DefaultProfile</span></span>
<span data-ttu-id="11ff6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11ff6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11ff6-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11ff6-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="11ff6-125">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="11ff6-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="11ff6-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="11ff6-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="11ff6-127">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11ff6-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="11ff6-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="11ff6-128">-Name</span></span>
<span data-ttu-id="11ff6-129">Anger namnet på den URL-sökväg där cmdlet ställer in konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="11ff6-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="11ff6-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="11ff6-130">-PathRules</span></span>
<span data-ttu-id="11ff6-131">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="11ff6-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="11ff6-132">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="11ff6-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="11ff6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ff6-133">CommonParameters</span></span>
<span data-ttu-id="11ff6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ff6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ff6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ff6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ff6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11ff6-136">INPUTS</span></span>

### <span data-ttu-id="11ff6-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11ff6-137">PSApplicationGateway</span></span>
<span data-ttu-id="11ff6-138">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11ff6-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="11ff6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11ff6-139">OUTPUTS</span></span>

### <span data-ttu-id="11ff6-140">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11ff6-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11ff6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11ff6-141">NOTES</span></span>

## <span data-ttu-id="11ff6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11ff6-142">RELATED LINKS</span></span>

[<span data-ttu-id="11ff6-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11ff6-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11ff6-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11ff6-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11ff6-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11ff6-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11ff6-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11ff6-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


