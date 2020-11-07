---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ec85b643294f65aceefae2d4a52e9a5d48f15191
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922160"
---
# <span data-ttu-id="e83ac-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e83ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e83ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e83ac-103">Skapar en adresslisteregel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e83ac-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e83ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e83ac-104">SYNTAX</span></span>

### <span data-ttu-id="e83ac-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e83ac-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e83ac-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e83ac-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e83ac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e83ac-107">DESCRIPTION</span></span>
<span data-ttu-id="e83ac-108">Cmdleten **Add-AzApplicationGatewayRequestRoutingRule** skapar en regel för en anslutningsbegäran för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e83ac-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e83ac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e83ac-109">EXAMPLES</span></span>

### <span data-ttu-id="e83ac-110">Exempel 1: skapa en regel för en anslutningsbegäran för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="e83ac-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e83ac-111">Det här kommandot skapar en grundläggande Dirigerings regel med namnet Rule01 och lagrar resultatet i variabeln som heter $Rule.</span><span class="sxs-lookup"><span data-stu-id="e83ac-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="e83ac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e83ac-112">PARAMETERS</span></span>

### <span data-ttu-id="e83ac-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e83ac-113">-BackendAddressPool</span></span>
<span data-ttu-id="e83ac-114">Anger backend-adresspoolen som ett objekt för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="e83ac-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e83ac-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="e83ac-116">Anger backend-adressens adresspool-ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e83ac-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e83ac-117">-BackendHttpSettings</span></span>
<span data-ttu-id="e83ac-118">Anger backend-HTTP-inställningar, som ett objekt, för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="e83ac-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e83ac-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e83ac-120">Anger backend HTTP-inställningar ID för regeln för anslutningsbegäran som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e83ac-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83ac-121">-DefaultProfile</span></span>
<span data-ttu-id="e83ac-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e83ac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e83ac-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e83ac-123">-HttpListener</span></span>
<span data-ttu-id="e83ac-124">Anger den backend-HTTP-lyssnaren som regeln för anslutningsbegäran kan skapa.</span><span class="sxs-lookup"><span data-stu-id="e83ac-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e83ac-125">-HttpListenerId</span></span>
<span data-ttu-id="e83ac-126">Anger Server delens HTTP-lyssnar-ID för regeln för att skapa en begäran.</span><span class="sxs-lookup"><span data-stu-id="e83ac-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e83ac-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="e83ac-127">-Name</span></span>
<span data-ttu-id="e83ac-128">Anger namnet på regeln för anslutningsbegäran som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="e83ac-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e83ac-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83ac-129">-RedirectConfiguration</span></span>
<span data-ttu-id="e83ac-130">RedirectConfiguration för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e83ac-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e83ac-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e83ac-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="e83ac-132">ID för Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83ac-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e83ac-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e83ac-133">-RuleType</span></span>
<span data-ttu-id="e83ac-134">Anger typen för regeln för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="e83ac-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="e83ac-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e83ac-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="e83ac-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e83ac-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e83ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83ac-137">CommonParameters</span></span>
<span data-ttu-id="e83ac-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e83ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83ac-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83ac-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83ac-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e83ac-140">INPUTS</span></span>

### <span data-ttu-id="e83ac-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e83ac-141">System.String</span></span>

## <span data-ttu-id="e83ac-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e83ac-142">OUTPUTS</span></span>

### <span data-ttu-id="e83ac-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e83ac-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e83ac-144">NOTES</span></span>

## <span data-ttu-id="e83ac-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e83ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="e83ac-146">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-146">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e83ac-147">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-147">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e83ac-148">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-148">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e83ac-149">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e83ac-149">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


