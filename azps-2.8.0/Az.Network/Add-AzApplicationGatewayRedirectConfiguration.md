---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 6db510e79d2c1796cf62a1fd00e55e7860164af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918850"
---
# <span data-ttu-id="d45dd-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45dd-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d45dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d45dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d45dd-103">Lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d45dd-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="d45dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d45dd-104">SYNTAX</span></span>

### <span data-ttu-id="d45dd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d45dd-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d45dd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d45dd-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d45dd-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="d45dd-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d45dd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d45dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d45dd-109">Cmdleten **Add-AzApplicationGatewayRedirectConfiguration** lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d45dd-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="d45dd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d45dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d45dd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d45dd-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="d45dd-112">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d45dd-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d45dd-113">Det andra kommandot lägger till omdirigeringsvariabler i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d45dd-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="d45dd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d45dd-114">PARAMETERS</span></span>

### <span data-ttu-id="d45dd-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45dd-115">-ApplicationGateway</span></span>
<span data-ttu-id="d45dd-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45dd-116">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45dd-117">-DefaultProfile</span></span>
<span data-ttu-id="d45dd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d45dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="d45dd-119">-IncludePath</span></span>
<span data-ttu-id="d45dd-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d45dd-120">Include path in the redirected url.</span></span>
<span data-ttu-id="d45dd-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="d45dd-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="d45dd-122">-IncludeQueryString</span></span>
<span data-ttu-id="d45dd-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d45dd-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="d45dd-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="d45dd-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d45dd-125">-Name</span></span>
<span data-ttu-id="d45dd-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d45dd-126">The name of the Redirect Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="d45dd-127">-RedirectType</span></span>
<span data-ttu-id="d45dd-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="d45dd-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="d45dd-129">-TargetListener</span></span>
<span data-ttu-id="d45dd-130">HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="d45dd-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="d45dd-131">-TargetListenerID</span></span>
<span data-ttu-id="d45dd-132">ID för HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="d45dd-132">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="d45dd-133">-TargetUrl</span></span>
<span data-ttu-id="d45dd-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="d45dd-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45dd-135">CommonParameters</span></span>
<span data-ttu-id="d45dd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45dd-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45dd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45dd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d45dd-138">INPUTS</span></span>

### <span data-ttu-id="d45dd-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45dd-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45dd-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d45dd-140">OUTPUTS</span></span>

### <span data-ttu-id="d45dd-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45dd-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45dd-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d45dd-142">NOTES</span></span>

## <span data-ttu-id="d45dd-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d45dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="d45dd-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45dd-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d45dd-145">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45dd-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d45dd-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45dd-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d45dd-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d45dd-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
