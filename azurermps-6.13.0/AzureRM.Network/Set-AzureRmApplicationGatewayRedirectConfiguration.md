---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fe6c2ce03c238dadb53e8e0df88e4402d8f614d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573960"
---
# <span data-ttu-id="7f7a9-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f7a9-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7f7a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7a9-103">Anger konfigurationen för omdirigering för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f7a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f7a9-104">SYNTAX</span></span>

### <span data-ttu-id="7f7a9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7a9-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f7a9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f7a9-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f7a9-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="7f7a9-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7a9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f7a9-108">DESCRIPTION</span></span>
<span data-ttu-id="7f7a9-109">Cmdleten **set-AzureRmApplicationGatewayRequestRoutingRule** ändrar en konfiguration för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="7f7a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f7a9-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7a9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f7a9-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="7f7a9-112">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f7a9-113">Det andra kommandot ändrar omdirigeringsinställningar för Application Gateway för att omdirigera typen permanent och använda en mål-URL.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="7f7a9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f7a9-114">PARAMETERS</span></span>

### <span data-ttu-id="7f7a9-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f7a9-115">-ApplicationGateway</span></span>
<span data-ttu-id="7f7a9-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f7a9-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7f7a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7a9-117">-DefaultProfile</span></span>
<span data-ttu-id="7f7a9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f7a9-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="7f7a9-119">-IncludePath</span></span>
<span data-ttu-id="7f7a9-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-120">Include path in the redirected url.</span></span>
<span data-ttu-id="7f7a9-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-121">Default is true.</span></span>

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

### <span data-ttu-id="7f7a9-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="7f7a9-122">-IncludeQueryString</span></span>
<span data-ttu-id="7f7a9-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="7f7a9-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-124">Default is true.</span></span>

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

### <span data-ttu-id="7f7a9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f7a9-125">-Name</span></span>
<span data-ttu-id="7f7a9-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="7f7a9-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="7f7a9-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="7f7a9-127">-RedirectType</span></span>
<span data-ttu-id="7f7a9-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="7f7a9-128">The type of redirect</span></span>

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

### <span data-ttu-id="7f7a9-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="7f7a9-129">-TargetListener</span></span>
<span data-ttu-id="7f7a9-130">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="7f7a9-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="7f7a9-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="7f7a9-131">-TargetListenerID</span></span>
<span data-ttu-id="7f7a9-132">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="7f7a9-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="7f7a9-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="7f7a9-133">-TargetUrl</span></span>
<span data-ttu-id="7f7a9-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="7f7a9-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="7f7a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7a9-135">CommonParameters</span></span>
<span data-ttu-id="7f7a9-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7a9-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7a9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7a9-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f7a9-138">INPUTS</span></span>

### <span data-ttu-id="7f7a9-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f7a9-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7f7a9-140">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f7a9-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7f7a9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f7a9-141">OUTPUTS</span></span>

### <span data-ttu-id="7f7a9-142">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f7a9-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f7a9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f7a9-143">NOTES</span></span>

## <span data-ttu-id="7f7a9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f7a9-144">RELATED LINKS</span></span>
