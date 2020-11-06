---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583244"
---
# <span data-ttu-id="37326-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37326-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="37326-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37326-102">SYNOPSIS</span></span>
<span data-ttu-id="37326-103">Skapar en konfiguration för omdirigering för en programport.</span><span class="sxs-lookup"><span data-stu-id="37326-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37326-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37326-104">SYNTAX</span></span>

### <span data-ttu-id="37326-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="37326-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37326-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="37326-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37326-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="37326-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37326-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37326-108">DESCRIPTION</span></span>
<span data-ttu-id="37326-109">Cmdleten **New-AzureRmApplicationGatewayRedirectConfiguration** skapar en konfiguration för omdirigering för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="37326-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="37326-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37326-110">EXAMPLES</span></span>

### <span data-ttu-id="37326-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37326-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="37326-112">Det här kommandot skapar en Omdirigerad konfiguration med namnet Redirect01 och lagrar resultatet i variabeln som heter $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="37326-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="37326-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37326-113">PARAMETERS</span></span>

### <span data-ttu-id="37326-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="37326-114">-IncludePath</span></span>
<span data-ttu-id="37326-115">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="37326-115">Include path in the redirected url.</span></span>
<span data-ttu-id="37326-116">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="37326-116">Default is true.</span></span>

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

### <span data-ttu-id="37326-117">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="37326-117">-IncludeQueryString</span></span>
<span data-ttu-id="37326-118">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="37326-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="37326-119">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="37326-119">Default is true.</span></span>

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

### <span data-ttu-id="37326-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="37326-120">-Name</span></span>
<span data-ttu-id="37326-121">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="37326-121">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="37326-122">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="37326-122">-RedirectType</span></span>
<span data-ttu-id="37326-123">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="37326-123">The type of redirect</span></span>

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

### <span data-ttu-id="37326-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="37326-124">-TargetListener</span></span>
<span data-ttu-id="37326-125">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="37326-125">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="37326-126">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="37326-126">-TargetListenerID</span></span>
<span data-ttu-id="37326-127">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="37326-127">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="37326-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="37326-128">-TargetUrl</span></span>
<span data-ttu-id="37326-129">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="37326-129">Target URL fo redirection</span></span>

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

### <span data-ttu-id="37326-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37326-130">-DefaultProfile</span></span>
<span data-ttu-id="37326-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37326-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37326-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37326-132">CommonParameters</span></span>
<span data-ttu-id="37326-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37326-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37326-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37326-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37326-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37326-135">INPUTS</span></span>

### <span data-ttu-id="37326-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="37326-136">None</span></span>

## <span data-ttu-id="37326-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37326-137">OUTPUTS</span></span>

### <span data-ttu-id="37326-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37326-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="37326-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37326-139">NOTES</span></span>

## <span data-ttu-id="37326-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37326-140">RELATED LINKS</span></span>

