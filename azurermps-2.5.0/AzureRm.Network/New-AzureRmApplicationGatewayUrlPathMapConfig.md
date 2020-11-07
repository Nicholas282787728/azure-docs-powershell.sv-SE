---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: e43d5277566311fe77ee239d88e55f658aca8b40
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929002"
---
# <span data-ttu-id="d03eb-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d03eb-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d03eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d03eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d03eb-103">Skapar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="d03eb-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d03eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d03eb-104">SYNTAX</span></span>

### <span data-ttu-id="d03eb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d03eb-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d03eb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d03eb-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d03eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d03eb-107">DESCRIPTION</span></span>
<span data-ttu-id="d03eb-108">Cmdleten **New-AzureRmApplicationGatewayUrlPathMapConfig** skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="d03eb-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d03eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d03eb-109">EXAMPLES</span></span>

### <span data-ttu-id="d03eb-110">Exempel 1: skapa en matris med URL-sökvägar till en backend-server</span><span class="sxs-lookup"><span data-stu-id="d03eb-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="d03eb-111">Det här kommandot skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="d03eb-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d03eb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d03eb-112">PARAMETERS</span></span>

### <span data-ttu-id="d03eb-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d03eb-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d03eb-114">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="d03eb-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d03eb-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d03eb-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d03eb-116">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="d03eb-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d03eb-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d03eb-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d03eb-118">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="d03eb-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d03eb-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d03eb-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d03eb-120">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="d03eb-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d03eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03eb-121">-DefaultProfile</span></span>
<span data-ttu-id="d03eb-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d03eb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d03eb-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d03eb-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d03eb-124">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d03eb-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d03eb-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d03eb-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d03eb-126">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d03eb-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d03eb-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d03eb-127">-Name</span></span>
<span data-ttu-id="d03eb-128">Anger namnet på URL-sökvägen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="d03eb-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d03eb-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d03eb-129">-PathRules</span></span>
<span data-ttu-id="d03eb-130">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="d03eb-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="d03eb-131">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="d03eb-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d03eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03eb-132">CommonParameters</span></span>
<span data-ttu-id="d03eb-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d03eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03eb-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03eb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03eb-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d03eb-135">INPUTS</span></span>

## <span data-ttu-id="d03eb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d03eb-136">OUTPUTS</span></span>

### <span data-ttu-id="d03eb-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d03eb-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="d03eb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d03eb-138">NOTES</span></span>

## <span data-ttu-id="d03eb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d03eb-139">RELATED LINKS</span></span>

[<span data-ttu-id="d03eb-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d03eb-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d03eb-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d03eb-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d03eb-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d03eb-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d03eb-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d03eb-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


