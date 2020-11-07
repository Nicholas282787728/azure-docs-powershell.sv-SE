---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922434"
---
# <span data-ttu-id="919c4-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="919c4-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="919c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="919c4-102">SYNOPSIS</span></span>
<span data-ttu-id="919c4-103">Lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="919c4-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="919c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="919c4-104">SYNTAX</span></span>

### <span data-ttu-id="919c4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="919c4-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="919c4-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="919c4-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="919c4-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="919c4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="919c4-108">DESCRIPTION</span></span>
<span data-ttu-id="919c4-109">Cmdleten **Add-AzApplicationGatewayRedirectConfiguration** lägger till en konfiguration för omdirigering till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="919c4-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="919c4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="919c4-110">EXAMPLES</span></span>

### <span data-ttu-id="919c4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="919c4-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="919c4-112">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="919c4-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="919c4-113">Det andra kommandot lägger till omdirigeringsvariabler i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="919c4-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="919c4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="919c4-114">PARAMETERS</span></span>

### <span data-ttu-id="919c4-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="919c4-115">-ApplicationGateway</span></span>
<span data-ttu-id="919c4-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="919c4-116">The applicationGateway</span></span>

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

### <span data-ttu-id="919c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919c4-117">-DefaultProfile</span></span>
<span data-ttu-id="919c4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="919c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="919c4-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="919c4-119">-IncludePath</span></span>
<span data-ttu-id="919c4-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="919c4-120">Include path in the redirected url.</span></span>
<span data-ttu-id="919c4-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="919c4-121">Default is true.</span></span>

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

### <span data-ttu-id="919c4-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="919c4-122">-IncludeQueryString</span></span>
<span data-ttu-id="919c4-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="919c4-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="919c4-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="919c4-124">Default is true.</span></span>

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

### <span data-ttu-id="919c4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="919c4-125">-Name</span></span>
<span data-ttu-id="919c4-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="919c4-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="919c4-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="919c4-127">-RedirectType</span></span>
<span data-ttu-id="919c4-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="919c4-128">The type of redirect</span></span>

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

### <span data-ttu-id="919c4-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="919c4-129">-TargetListener</span></span>
<span data-ttu-id="919c4-130">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="919c4-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="919c4-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="919c4-131">-TargetListenerID</span></span>
<span data-ttu-id="919c4-132">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="919c4-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="919c4-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="919c4-133">-TargetUrl</span></span>
<span data-ttu-id="919c4-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="919c4-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="919c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919c4-135">CommonParameters</span></span>
<span data-ttu-id="919c4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919c4-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919c4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919c4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="919c4-138">INPUTS</span></span>

### <span data-ttu-id="919c4-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="919c4-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="919c4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="919c4-140">OUTPUTS</span></span>

### <span data-ttu-id="919c4-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="919c4-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="919c4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="919c4-142">NOTES</span></span>

## <span data-ttu-id="919c4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="919c4-143">RELATED LINKS</span></span>

