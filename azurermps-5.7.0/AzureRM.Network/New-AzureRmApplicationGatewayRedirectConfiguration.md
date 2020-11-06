---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574903"
---
# <span data-ttu-id="d95a5-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95a5-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d95a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d95a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d95a5-103">Skapar en konfiguration för omdirigering för en programport.</span><span class="sxs-lookup"><span data-stu-id="d95a5-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d95a5-104">SYNTAX</span></span>

### <span data-ttu-id="d95a5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d95a5-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d95a5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d95a5-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d95a5-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="d95a5-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d95a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d95a5-108">DESCRIPTION</span></span>
<span data-ttu-id="d95a5-109">Cmdleten **New-AzureRmApplicationGatewayRedirectConfiguration** skapar en konfiguration för omdirigering för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d95a5-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="d95a5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d95a5-110">EXAMPLES</span></span>

### <span data-ttu-id="d95a5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d95a5-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="d95a5-112">Det här kommandot skapar en Omdirigerad konfiguration med namnet Redirect01 och lagrar resultatet i variabeln som heter $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="d95a5-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="d95a5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d95a5-113">PARAMETERS</span></span>

### <span data-ttu-id="d95a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95a5-114">-DefaultProfile</span></span>
<span data-ttu-id="d95a5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d95a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95a5-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="d95a5-116">-IncludePath</span></span>
<span data-ttu-id="d95a5-117">Ta med sökväg i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d95a5-117">Include path in the redirected url.</span></span>
<span data-ttu-id="d95a5-118">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="d95a5-118">Default is true.</span></span>

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

### <span data-ttu-id="d95a5-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="d95a5-119">-IncludeQueryString</span></span>
<span data-ttu-id="d95a5-120">Inkludera frågesträngen i den omdirigerade URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="d95a5-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="d95a5-121">Standard är sant.</span><span class="sxs-lookup"><span data-stu-id="d95a5-121">Default is true.</span></span>

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

### <span data-ttu-id="d95a5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d95a5-122">-Name</span></span>
<span data-ttu-id="d95a5-123">Namnet på omdirigerings konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d95a5-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="d95a5-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="d95a5-124">-RedirectType</span></span>
<span data-ttu-id="d95a5-125">Typ av omdirigering</span><span class="sxs-lookup"><span data-stu-id="d95a5-125">The type of redirect</span></span>

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

### <span data-ttu-id="d95a5-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="d95a5-126">-TargetListener</span></span>
<span data-ttu-id="d95a5-127">HTTPListener att skicka begäran till</span><span class="sxs-lookup"><span data-stu-id="d95a5-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="d95a5-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="d95a5-128">-TargetListenerID</span></span>
<span data-ttu-id="d95a5-129">ID för lyssnings tjänsten för att omdirigera begäran till</span><span class="sxs-lookup"><span data-stu-id="d95a5-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="d95a5-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="d95a5-130">-TargetUrl</span></span>
<span data-ttu-id="d95a5-131">Mål webb adress för omdirigering</span><span class="sxs-lookup"><span data-stu-id="d95a5-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="d95a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95a5-132">CommonParameters</span></span>
<span data-ttu-id="d95a5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95a5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95a5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d95a5-135">INPUTS</span></span>

### <span data-ttu-id="d95a5-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="d95a5-136">None</span></span>

## <span data-ttu-id="d95a5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d95a5-137">OUTPUTS</span></span>

### <span data-ttu-id="d95a5-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95a5-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d95a5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d95a5-139">NOTES</span></span>

## <span data-ttu-id="d95a5-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d95a5-140">RELATED LINKS</span></span>

