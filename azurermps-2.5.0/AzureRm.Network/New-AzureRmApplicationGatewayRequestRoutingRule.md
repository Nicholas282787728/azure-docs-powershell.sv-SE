---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930538"
---
# <span data-ttu-id="bd312-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bd312-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd312-102">SYNOPSIS</span></span>
<span data-ttu-id="bd312-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="bd312-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd312-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd312-104">SYNTAX</span></span>

### <span data-ttu-id="bd312-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd312-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd312-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bd312-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd312-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd312-107">DESCRIPTION</span></span>
<span data-ttu-id="bd312-108">Cmdleten **Add-AzureRmApplicationGatewayRequestRoutingRule** skapar en regel för en anslutningsbegäran för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd312-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="bd312-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd312-109">EXAMPLES</span></span>

### <span data-ttu-id="bd312-110">Exempel 1: skapa en regel för en anslutningsbegäran för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="bd312-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="bd312-111">Det här kommandot skapar en grundläggande Dirigerings regel med namnet Rule01 och lagrar resultatet i variabeln som heter $Rule.</span><span class="sxs-lookup"><span data-stu-id="bd312-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="bd312-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd312-112">PARAMETERS</span></span>

### <span data-ttu-id="bd312-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd312-113">-BackendAddressPool</span></span>
<span data-ttu-id="bd312-114">Anger backend-adresspoolen som ett objekt för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="bd312-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bd312-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="bd312-116">Anger backend-adressens adresspool-ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="bd312-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bd312-117">-BackendHttpSettings</span></span>
<span data-ttu-id="bd312-118">Anger backend-HTTP-inställningar, som ett objekt, för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="bd312-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bd312-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="bd312-120">Anger backend HTTP-inställningar ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="bd312-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd312-121">-DefaultProfile</span></span>
<span data-ttu-id="bd312-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd312-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd312-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bd312-123">-HttpListener</span></span>
<span data-ttu-id="bd312-124">Anger den backend-HTTP-lyssnaren som regeln för anslutningsbegäran kan skapa.</span><span class="sxs-lookup"><span data-stu-id="bd312-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="bd312-125">-HttpListenerId</span></span>
<span data-ttu-id="bd312-126">Anger Server delens HTTP-lyssnar-ID för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="bd312-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bd312-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd312-127">-Name</span></span>
<span data-ttu-id="bd312-128">Anger namnet på regeln för anslutningsbegäran som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="bd312-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bd312-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd312-129">-RedirectConfiguration</span></span>
<span data-ttu-id="bd312-130">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="bd312-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bd312-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bd312-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="bd312-132">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd312-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bd312-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bd312-133">-RuleType</span></span>
<span data-ttu-id="bd312-134">Anger typen för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="bd312-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="bd312-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="bd312-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="bd312-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="bd312-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="bd312-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd312-137">CommonParameters</span></span>
<span data-ttu-id="bd312-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd312-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd312-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd312-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd312-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd312-140">INPUTS</span></span>

### <span data-ttu-id="bd312-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bd312-141">System.String</span></span>

## <span data-ttu-id="bd312-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd312-142">OUTPUTS</span></span>

### <span data-ttu-id="bd312-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bd312-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd312-144">NOTES</span></span>

## <span data-ttu-id="bd312-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd312-145">RELATED LINKS</span></span>

[<span data-ttu-id="bd312-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bd312-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bd312-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bd312-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bd312-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


