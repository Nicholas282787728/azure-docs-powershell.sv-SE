---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 73d60d86110893005e72152c08e82d4152b1c482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574279"
---
# <span data-ttu-id="fdb5e-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdb5e-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fdb5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb5e-103">Lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdb5e-104">SYNTAX</span></span>

### <span data-ttu-id="fdb5e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb5e-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb5e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fdb5e-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb5e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="fdb5e-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdb5e-108">DESCRIPTION</span></span>
<span data-ttu-id="fdb5e-109">Cmdleten **Add-AzureRmApplicationGatewayRedirectConfiguration** lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="fdb5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdb5e-110">EXAMPLES</span></span>

### <span data-ttu-id="fdb5e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fdb5e-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="fdb5e-112">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fdb5e-113">Det andra kommandot lägger till omdirigeringsvariabler i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="fdb5e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdb5e-114">PARAMETERS</span></span>

### <span data-ttu-id="fdb5e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdb5e-115">-ApplicationGateway</span></span>
<span data-ttu-id="fdb5e-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdb5e-116">The applicationGateway</span></span>

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

### <span data-ttu-id="fdb5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb5e-117">-DefaultProfile</span></span>
<span data-ttu-id="fdb5e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb5e-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="fdb5e-119">-IncludePath</span></span>
<span data-ttu-id="fdb5e-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-120">Include path in the redirected url.</span></span>
<span data-ttu-id="fdb5e-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb5e-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="fdb5e-122">-IncludeQueryString</span></span>
<span data-ttu-id="fdb5e-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="fdb5e-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb5e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdb5e-125">-Name</span></span>
<span data-ttu-id="fdb5e-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="fdb5e-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="fdb5e-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="fdb5e-127">-RedirectType</span></span>
<span data-ttu-id="fdb5e-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="fdb5e-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb5e-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="fdb5e-129">-TargetListener</span></span>
<span data-ttu-id="fdb5e-130">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="fdb5e-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="fdb5e-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="fdb5e-131">-TargetListenerID</span></span>
<span data-ttu-id="fdb5e-132">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="fdb5e-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="fdb5e-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="fdb5e-133">-TargetUrl</span></span>
<span data-ttu-id="fdb5e-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="fdb5e-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb5e-135">CommonParameters</span></span>
<span data-ttu-id="fdb5e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb5e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb5e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb5e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdb5e-138">INPUTS</span></span>

### <span data-ttu-id="fdb5e-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdb5e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fdb5e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdb5e-140">OUTPUTS</span></span>

### <span data-ttu-id="fdb5e-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fdb5e-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fdb5e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdb5e-142">NOTES</span></span>

## <span data-ttu-id="fdb5e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdb5e-143">RELATED LINKS</span></span>

