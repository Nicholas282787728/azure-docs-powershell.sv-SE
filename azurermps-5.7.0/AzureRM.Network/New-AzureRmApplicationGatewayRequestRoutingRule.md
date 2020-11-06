---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ab053235c928f109321cdf9adf3429e589958ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578120"
---
# <span data-ttu-id="502f3-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="502f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="502f3-102">SYNOPSIS</span></span>
<span data-ttu-id="502f3-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="502f3-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="502f3-104">SYNTAX</span></span>

### <span data-ttu-id="502f3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="502f3-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="502f3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="502f3-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="502f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="502f3-107">DESCRIPTION</span></span>
<span data-ttu-id="502f3-108">Cmdleten **Add-AzureRmApplicationGatewayRequestRoutingRule** skapar en regel för en anslutningsbegäran för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="502f3-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="502f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="502f3-109">EXAMPLES</span></span>

### <span data-ttu-id="502f3-110">Exempel 1: skapa en regel för en anslutningsbegäran för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="502f3-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="502f3-111">Det här kommandot skapar en grundläggande Dirigerings regel med namnet Rule01 och lagrar resultatet i variabeln som heter $Rule.</span><span class="sxs-lookup"><span data-stu-id="502f3-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="502f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="502f3-112">PARAMETERS</span></span>

### <span data-ttu-id="502f3-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="502f3-113">-BackendAddressPool</span></span>
<span data-ttu-id="502f3-114">Anger backend-adresspoolen som ett objekt för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="502f3-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="502f3-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="502f3-116">Anger backend-adressens adresspool-ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="502f3-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="502f3-117">-BackendHttpSettings</span></span>
<span data-ttu-id="502f3-118">Anger backend-HTTP-inställningar, som ett objekt, för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="502f3-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="502f3-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="502f3-120">Anger backend HTTP-inställningar ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="502f3-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502f3-121">-DefaultProfile</span></span>
<span data-ttu-id="502f3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="502f3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="502f3-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="502f3-123">-HttpListener</span></span>
<span data-ttu-id="502f3-124">Anger den backend-HTTP-lyssnaren som regeln för anslutningsbegäran kan skapa.</span><span class="sxs-lookup"><span data-stu-id="502f3-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="502f3-125">-HttpListenerId</span></span>
<span data-ttu-id="502f3-126">Anger Server delens HTTP-lyssnar-ID för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="502f3-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="502f3-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="502f3-127">-Name</span></span>
<span data-ttu-id="502f3-128">Anger namnet på regeln för anslutningsbegäran som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="502f3-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="502f3-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="502f3-129">-RedirectConfiguration</span></span>
<span data-ttu-id="502f3-130">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="502f3-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="502f3-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="502f3-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="502f3-132">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="502f3-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="502f3-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="502f3-133">-RuleType</span></span>
<span data-ttu-id="502f3-134">Anger typen för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="502f3-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="502f3-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="502f3-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="502f3-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="502f3-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="502f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502f3-137">CommonParameters</span></span>
<span data-ttu-id="502f3-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502f3-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502f3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502f3-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="502f3-140">INPUTS</span></span>

### <span data-ttu-id="502f3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="502f3-141">System.String</span></span>

## <span data-ttu-id="502f3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="502f3-142">OUTPUTS</span></span>

### <span data-ttu-id="502f3-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="502f3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="502f3-144">NOTES</span></span>

## <span data-ttu-id="502f3-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="502f3-145">RELATED LINKS</span></span>

[<span data-ttu-id="502f3-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="502f3-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="502f3-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="502f3-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="502f3-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


