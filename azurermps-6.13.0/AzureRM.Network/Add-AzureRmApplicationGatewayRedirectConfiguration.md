---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 01f7daf47fa62e346dc7323ee5978f81f5797e29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758176"
---
# <span data-ttu-id="8a66b-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a66b-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8a66b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a66b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a66b-103">Lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a66b-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a66b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a66b-104">SYNTAX</span></span>

### <span data-ttu-id="8a66b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a66b-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a66b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8a66b-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a66b-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="8a66b-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a66b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a66b-108">DESCRIPTION</span></span>
<span data-ttu-id="8a66b-109">Cmdleten **Add-AzureRmApplicationGatewayRedirectConfiguration** lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a66b-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="8a66b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a66b-110">EXAMPLES</span></span>

### <span data-ttu-id="8a66b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a66b-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="8a66b-112">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="8a66b-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8a66b-113">Det andra kommandot lägger till omdirigeringsvariabler i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="8a66b-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="8a66b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a66b-114">PARAMETERS</span></span>

### <span data-ttu-id="8a66b-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a66b-115">-ApplicationGateway</span></span>
<span data-ttu-id="8a66b-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a66b-116">The applicationGateway</span></span>

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

### <span data-ttu-id="8a66b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a66b-117">-DefaultProfile</span></span>
<span data-ttu-id="8a66b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a66b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a66b-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="8a66b-119">-IncludePath</span></span>
<span data-ttu-id="8a66b-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="8a66b-120">Include path in the redirected url.</span></span>
<span data-ttu-id="8a66b-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="8a66b-121">Default is true.</span></span>

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

### <span data-ttu-id="8a66b-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="8a66b-122">-IncludeQueryString</span></span>
<span data-ttu-id="8a66b-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="8a66b-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="8a66b-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="8a66b-124">Default is true.</span></span>

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

### <span data-ttu-id="8a66b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a66b-125">-Name</span></span>
<span data-ttu-id="8a66b-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8a66b-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="8a66b-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="8a66b-127">-RedirectType</span></span>
<span data-ttu-id="8a66b-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="8a66b-128">The type of redirect</span></span>

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

### <span data-ttu-id="8a66b-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="8a66b-129">-TargetListener</span></span>
<span data-ttu-id="8a66b-130">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="8a66b-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="8a66b-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="8a66b-131">-TargetListenerID</span></span>
<span data-ttu-id="8a66b-132">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="8a66b-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="8a66b-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="8a66b-133">-TargetUrl</span></span>
<span data-ttu-id="8a66b-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="8a66b-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="8a66b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a66b-135">CommonParameters</span></span>
<span data-ttu-id="8a66b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a66b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a66b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a66b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a66b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a66b-138">INPUTS</span></span>

### <span data-ttu-id="8a66b-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a66b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8a66b-140">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a66b-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8a66b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a66b-141">OUTPUTS</span></span>

### <span data-ttu-id="8a66b-142">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a66b-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a66b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a66b-143">NOTES</span></span>

## <span data-ttu-id="8a66b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a66b-144">RELATED LINKS</span></span>
