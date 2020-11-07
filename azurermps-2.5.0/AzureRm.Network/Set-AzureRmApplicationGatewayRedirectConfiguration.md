---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: c851e075c4963477d8b8f6b18440780735c74f32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930522"
---
# <span data-ttu-id="6d894-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d894-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6d894-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d894-102">SYNOPSIS</span></span>
<span data-ttu-id="6d894-103">Anger konfigurationen för omdirigering för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="6d894-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d894-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d894-104">SYNTAX</span></span>

### <span data-ttu-id="6d894-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d894-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d894-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6d894-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d894-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="6d894-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d894-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d894-108">DESCRIPTION</span></span>
<span data-ttu-id="6d894-109">Cmdleten **set-AzureRmApplicationGatewayRequestRoutingRule** ändrar en konfiguration för omdirigering.</span><span class="sxs-lookup"><span data-stu-id="6d894-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="6d894-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d894-110">EXAMPLES</span></span>

### <span data-ttu-id="6d894-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d894-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="6d894-112">Det första kommandot får programgatewayen som heter ApplicationGateway01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="6d894-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6d894-113">Det andra kommandot ändrar omdirigeringsinställningar för Application Gateway för att omdirigera typen permanent och använda en mål-URL.</span><span class="sxs-lookup"><span data-stu-id="6d894-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="6d894-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d894-114">PARAMETERS</span></span>

### <span data-ttu-id="6d894-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d894-115">-ApplicationGateway</span></span>
<span data-ttu-id="6d894-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d894-116">The applicationGateway</span></span>

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

### <span data-ttu-id="6d894-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d894-117">-DefaultProfile</span></span>
<span data-ttu-id="6d894-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d894-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d894-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="6d894-119">-IncludePath</span></span>
<span data-ttu-id="6d894-120">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="6d894-120">Include path in the redirected url.</span></span>
<span data-ttu-id="6d894-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="6d894-121">Default is true.</span></span>

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

### <span data-ttu-id="6d894-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="6d894-122">-IncludeQueryString</span></span>
<span data-ttu-id="6d894-123">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="6d894-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="6d894-124">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="6d894-124">Default is true.</span></span>

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

### <span data-ttu-id="6d894-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d894-125">-Name</span></span>
<span data-ttu-id="6d894-126">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6d894-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="6d894-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="6d894-127">-RedirectType</span></span>
<span data-ttu-id="6d894-128">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="6d894-128">The type of redirect</span></span>

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

### <span data-ttu-id="6d894-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="6d894-129">-TargetListener</span></span>
<span data-ttu-id="6d894-130">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="6d894-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="6d894-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="6d894-131">-TargetListenerID</span></span>
<span data-ttu-id="6d894-132">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="6d894-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="6d894-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="6d894-133">-TargetUrl</span></span>
<span data-ttu-id="6d894-134">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="6d894-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="6d894-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d894-135">CommonParameters</span></span>
<span data-ttu-id="6d894-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d894-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d894-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d894-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d894-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d894-138">INPUTS</span></span>

### <span data-ttu-id="6d894-139">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d894-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d894-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d894-140">OUTPUTS</span></span>

### <span data-ttu-id="6d894-141">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d894-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d894-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d894-142">NOTES</span></span>

## <span data-ttu-id="6d894-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d894-143">RELATED LINKS</span></span>

