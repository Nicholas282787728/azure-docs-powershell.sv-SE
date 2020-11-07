---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922145"
---
# <span data-ttu-id="ab47f-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab47f-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ab47f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab47f-103">Skapar en matris med URL-sökvägar till en server del.</span><span class="sxs-lookup"><span data-stu-id="ab47f-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ab47f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab47f-104">SYNTAX</span></span>

### <span data-ttu-id="ab47f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab47f-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab47f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ab47f-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab47f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab47f-107">DESCRIPTION</span></span>
<span data-ttu-id="ab47f-108">Cmdleten **New-AzApplicationGatewayUrlPathMapConfig** skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="ab47f-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ab47f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab47f-109">EXAMPLES</span></span>

### <span data-ttu-id="ab47f-110">Exempel 1: skapa en matris med URL-sökvägar till en backend-server</span><span class="sxs-lookup"><span data-stu-id="ab47f-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="ab47f-111">Det här kommandot skapar en matris med URL-sökvägar till en backend-server.</span><span class="sxs-lookup"><span data-stu-id="ab47f-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ab47f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab47f-112">PARAMETERS</span></span>

### <span data-ttu-id="ab47f-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ab47f-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="ab47f-114">Anger den standardinställda adresspoolen för routning i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="ab47f-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ab47f-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ab47f-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="ab47f-116">Anger standardpool-ID för Server dels adress.</span><span class="sxs-lookup"><span data-stu-id="ab47f-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="ab47f-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ab47f-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="ab47f-118">Anger den server dels HTTP-inställningar som ska användas i händelse av att ingen av reglerna som anges i *pathRules* parameter matchar.</span><span class="sxs-lookup"><span data-stu-id="ab47f-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ab47f-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ab47f-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="ab47f-120">Anger standard server delen för HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="ab47f-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="ab47f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab47f-121">-DefaultProfile</span></span>
<span data-ttu-id="ab47f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab47f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab47f-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab47f-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="ab47f-124">Standard RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ab47f-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ab47f-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ab47f-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="ab47f-126">ID för Application Gateway standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab47f-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ab47f-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab47f-127">-Name</span></span>
<span data-ttu-id="ab47f-128">Anger namnet på URL-sökvägen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="ab47f-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ab47f-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="ab47f-129">-PathRules</span></span>
<span data-ttu-id="ab47f-130">Anger en lista med Sök vägs regler.</span><span class="sxs-lookup"><span data-stu-id="ab47f-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="ab47f-131">Observera att Sök vägs reglerna är sorterings känsliga, de används i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="ab47f-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="ab47f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab47f-132">CommonParameters</span></span>
<span data-ttu-id="ab47f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab47f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab47f-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab47f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab47f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab47f-135">INPUTS</span></span>

## <span data-ttu-id="ab47f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab47f-136">OUTPUTS</span></span>

### <span data-ttu-id="ab47f-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ab47f-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="ab47f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab47f-138">NOTES</span></span>

## <span data-ttu-id="ab47f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab47f-139">RELATED LINKS</span></span>

[<span data-ttu-id="ab47f-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab47f-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ab47f-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab47f-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ab47f-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab47f-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ab47f-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab47f-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


