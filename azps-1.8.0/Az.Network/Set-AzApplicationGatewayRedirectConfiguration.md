---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747770"
---
# <span data-ttu-id="10e6b-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10e6b-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="10e6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="10e6b-103">Anger konfigurationen för omdirigering för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="10e6b-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="10e6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10e6b-104">SYNTAX</span></span>

### <span data-ttu-id="10e6b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10e6b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e6b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10e6b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e6b-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="10e6b-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10e6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10e6b-108">DESCRIPTION</span></span>
<span data-ttu-id="10e6b-109">Cmdleten **set-AzApplicationGatewayRequestRoutingRule** ändrar en konfiguration för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="10e6b-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="10e6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10e6b-110">EXAMPLES</span></span>

### <span data-ttu-id="10e6b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10e6b-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="10e6b-112">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="10e6b-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="10e6b-113">Det andra kommandot ändrar omdirigeringsinställningar för Application Gateway för att omdirigera typen permanent och använda en mål-URL.</span><span class="sxs-lookup"><span data-stu-id="10e6b-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="10e6b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-114">PARAMETERS</span></span>

### <span data-ttu-id="10e6b-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10e6b-115">-ApplicationGateway</span></span>
<span data-ttu-id="10e6b-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10e6b-116">The applicationGateway</span></span>

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

### <span data-ttu-id="10e6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e6b-117">-DefaultProfile</span></span>
<span data-ttu-id="10e6b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10e6b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e6b-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="10e6b-119">-IncludePath</span></span>
<span data-ttu-id="10e6b-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="10e6b-120">Include path in the redirected url.</span></span>
<span data-ttu-id="10e6b-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="10e6b-121">Default is true.</span></span>

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

### <span data-ttu-id="10e6b-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="10e6b-122">-IncludeQueryString</span></span>
<span data-ttu-id="10e6b-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="10e6b-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="10e6b-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="10e6b-124">Default is true.</span></span>

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

### <span data-ttu-id="10e6b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="10e6b-125">-Name</span></span>
<span data-ttu-id="10e6b-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="10e6b-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="10e6b-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="10e6b-127">-RedirectType</span></span>
<span data-ttu-id="10e6b-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="10e6b-128">The type of redirect</span></span>

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

### <span data-ttu-id="10e6b-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="10e6b-129">-TargetListener</span></span>
<span data-ttu-id="10e6b-130">HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="10e6b-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="10e6b-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="10e6b-131">-TargetListenerID</span></span>
<span data-ttu-id="10e6b-132">ID för HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="10e6b-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="10e6b-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="10e6b-133">-TargetUrl</span></span>
<span data-ttu-id="10e6b-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="10e6b-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="10e6b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e6b-135">CommonParameters</span></span>
<span data-ttu-id="10e6b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e6b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e6b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e6b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e6b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10e6b-138">INPUTS</span></span>

### <span data-ttu-id="10e6b-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10e6b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10e6b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10e6b-140">OUTPUTS</span></span>

### <span data-ttu-id="10e6b-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10e6b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10e6b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-142">NOTES</span></span>

## <span data-ttu-id="10e6b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-143">RELATED LINKS</span></span>

[<span data-ttu-id="10e6b-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10e6b-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="10e6b-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10e6b-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="10e6b-146">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10e6b-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="10e6b-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10e6b-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
