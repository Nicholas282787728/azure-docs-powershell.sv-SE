---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918663"
---
# <span data-ttu-id="c3dcf-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c3dcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dcf-103">Skapar en konfiguration för omdirigering för en programport.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="c3dcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3dcf-104">SYNTAX</span></span>

### <span data-ttu-id="c3dcf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3dcf-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3dcf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c3dcf-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3dcf-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="c3dcf-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3dcf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3dcf-108">DESCRIPTION</span></span>
<span data-ttu-id="c3dcf-109">Cmdleten **New-AzApplicationGatewayRedirectConfiguration** skapar en konfiguration för omdirigering för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="c3dcf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3dcf-110">EXAMPLES</span></span>

### <span data-ttu-id="c3dcf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3dcf-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="c3dcf-112">Det här kommandot skapar en Omdirigerad konfiguration med namnet Redirect01 och lagrar resultatet i variabeln som heter $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="c3dcf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3dcf-113">PARAMETERS</span></span>

### <span data-ttu-id="c3dcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dcf-114">-DefaultProfile</span></span>
<span data-ttu-id="c3dcf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3dcf-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="c3dcf-116">-IncludePath</span></span>
<span data-ttu-id="c3dcf-117">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-117">Include path in the redirected url.</span></span>
<span data-ttu-id="c3dcf-118">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-118">Default is true.</span></span>

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

### <span data-ttu-id="c3dcf-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="c3dcf-119">-IncludeQueryString</span></span>
<span data-ttu-id="c3dcf-120">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="c3dcf-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-121">Default is true.</span></span>

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

### <span data-ttu-id="c3dcf-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3dcf-122">-Name</span></span>
<span data-ttu-id="c3dcf-123">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c3dcf-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="c3dcf-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c3dcf-124">-RedirectType</span></span>
<span data-ttu-id="c3dcf-125">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="c3dcf-125">The type of redirect</span></span>

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

### <span data-ttu-id="c3dcf-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="c3dcf-126">-TargetListener</span></span>
<span data-ttu-id="c3dcf-127">HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="c3dcf-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="c3dcf-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="c3dcf-128">-TargetListenerID</span></span>
<span data-ttu-id="c3dcf-129">ID för HTTP-lyssning för att dirigera om begäran till</span><span class="sxs-lookup"><span data-stu-id="c3dcf-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="c3dcf-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="c3dcf-130">-TargetUrl</span></span>
<span data-ttu-id="c3dcf-131">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="c3dcf-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="c3dcf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dcf-132">CommonParameters</span></span>
<span data-ttu-id="c3dcf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dcf-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3dcf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dcf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3dcf-135">INPUTS</span></span>

### <span data-ttu-id="c3dcf-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="c3dcf-136">None</span></span>

## <span data-ttu-id="c3dcf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3dcf-137">OUTPUTS</span></span>

### <span data-ttu-id="c3dcf-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c3dcf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3dcf-139">NOTES</span></span>

## <span data-ttu-id="c3dcf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3dcf-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3dcf-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c3dcf-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c3dcf-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c3dcf-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3dcf-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
