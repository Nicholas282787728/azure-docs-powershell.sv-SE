---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922158"
---
# <span data-ttu-id="47fae-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47fae-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="47fae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47fae-102">SYNOPSIS</span></span>
<span data-ttu-id="47fae-103">Skapar en konfiguration för omdirigering för en programport.</span><span class="sxs-lookup"><span data-stu-id="47fae-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="47fae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47fae-104">SYNTAX</span></span>

### <span data-ttu-id="47fae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47fae-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47fae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47fae-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47fae-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="47fae-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47fae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47fae-108">DESCRIPTION</span></span>
<span data-ttu-id="47fae-109">Cmdleten **New-AzApplicationGatewayRedirectConfiguration** skapar en konfiguration för omdirigering för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="47fae-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="47fae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47fae-110">EXAMPLES</span></span>

### <span data-ttu-id="47fae-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47fae-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="47fae-112">Det här kommandot skapar en Omdirigerad konfiguration med namnet Redirect01 och lagrar resultatet i variabeln som heter $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="47fae-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="47fae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47fae-113">PARAMETERS</span></span>

### <span data-ttu-id="47fae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fae-114">-DefaultProfile</span></span>
<span data-ttu-id="47fae-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47fae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47fae-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="47fae-116">-IncludePath</span></span>
<span data-ttu-id="47fae-117">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="47fae-117">Include path in the redirected url.</span></span>
<span data-ttu-id="47fae-118">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="47fae-118">Default is true.</span></span>

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

### <span data-ttu-id="47fae-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="47fae-119">-IncludeQueryString</span></span>
<span data-ttu-id="47fae-120">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="47fae-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="47fae-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="47fae-121">Default is true.</span></span>

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

### <span data-ttu-id="47fae-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="47fae-122">-Name</span></span>
<span data-ttu-id="47fae-123">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="47fae-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="47fae-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="47fae-124">-RedirectType</span></span>
<span data-ttu-id="47fae-125">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="47fae-125">The type of redirect</span></span>

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

### <span data-ttu-id="47fae-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="47fae-126">-TargetListener</span></span>
<span data-ttu-id="47fae-127">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="47fae-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="47fae-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="47fae-128">-TargetListenerID</span></span>
<span data-ttu-id="47fae-129">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="47fae-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="47fae-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="47fae-130">-TargetUrl</span></span>
<span data-ttu-id="47fae-131">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="47fae-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="47fae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fae-132">CommonParameters</span></span>
<span data-ttu-id="47fae-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47fae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fae-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47fae-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fae-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47fae-135">INPUTS</span></span>

### <span data-ttu-id="47fae-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="47fae-136">None</span></span>

## <span data-ttu-id="47fae-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47fae-137">OUTPUTS</span></span>

### <span data-ttu-id="47fae-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47fae-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="47fae-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47fae-139">NOTES</span></span>

## <span data-ttu-id="47fae-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47fae-140">RELATED LINKS</span></span>

