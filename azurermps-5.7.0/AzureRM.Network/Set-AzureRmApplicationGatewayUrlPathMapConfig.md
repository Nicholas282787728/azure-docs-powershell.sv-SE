---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 949de1a2016ffbecb96a8f10a34435cedd284ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583631"
---
# <span data-ttu-id="f668f-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f668f-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f668f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f668f-102">SYNOPSIS</span></span>
<span data-ttu-id="f668f-103">Anger konfiguration för en matris med URL-sökvägar till backend-server.</span><span class="sxs-lookup"><span data-stu-id="f668f-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f668f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f668f-104">SYNTAX</span></span>

### <span data-ttu-id="f668f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f668f-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f668f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f668f-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f668f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f668f-107">DESCRIPTION</span></span>
<span data-ttu-id="f668f-108">Cmdleten **set-AzureRmApplicationGatewayUrlPathMapConfig** anger konfiguration för en matris med URL-sökvägar till en Server grupp.</span><span class="sxs-lookup"><span data-stu-id="f668f-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f668f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f668f-109">EXAMPLES</span></span>

## <span data-ttu-id="f668f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f668f-110">PARAMETERS</span></span>

### <span data-ttu-id="f668f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f668f-111">-ApplicationGateway</span></span>
<span data-ttu-id="f668f-112">Anger den Programgateway till vilken denna cmdlet ställer in en konfiguration för URL-sökvägar.</span><span class="sxs-lookup"><span data-stu-id="f668f-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="f668f-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f668f-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="f668f-114">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="f668f-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f668f-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f668f-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="f668f-116">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="f668f-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="f668f-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f668f-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="f668f-118">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="f668f-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f668f-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f668f-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="f668f-120">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="f668f-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="f668f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f668f-121">-DefaultProfile</span></span>
<span data-ttu-id="f668f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f668f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f668f-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f668f-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="f668f-124">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f668f-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f668f-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f668f-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="f668f-126">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f668f-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f668f-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f668f-127">-Name</span></span>
<span data-ttu-id="f668f-128">Anger namnet på den URL-sökväg där cmdlet ställer in konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="f668f-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="f668f-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="f668f-129">-PathRules</span></span>
<span data-ttu-id="f668f-130">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="f668f-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="f668f-131">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="f668f-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="f668f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f668f-132">CommonParameters</span></span>
<span data-ttu-id="f668f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f668f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f668f-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f668f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f668f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f668f-135">INPUTS</span></span>

### <span data-ttu-id="f668f-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f668f-136">PSApplicationGateway</span></span>
<span data-ttu-id="f668f-137">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f668f-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f668f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f668f-138">OUTPUTS</span></span>

### <span data-ttu-id="f668f-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f668f-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f668f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f668f-140">NOTES</span></span>

## <span data-ttu-id="f668f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f668f-141">RELATED LINKS</span></span>

[<span data-ttu-id="f668f-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f668f-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f668f-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f668f-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f668f-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f668f-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f668f-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f668f-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

