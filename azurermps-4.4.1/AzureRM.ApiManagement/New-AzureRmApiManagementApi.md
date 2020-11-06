---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578664"
---
# <span data-ttu-id="059d0-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="059d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="059d0-102">SYNOPSIS</span></span>
<span data-ttu-id="059d0-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="059d0-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="059d0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="059d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="059d0-105">DESCRIPTION</span></span>
<span data-ttu-id="059d0-106">Cmdleten **New-AzureRmApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="059d0-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="059d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="059d0-107">EXAMPLES</span></span>

### <span data-ttu-id="059d0-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="059d0-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="059d0-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="059d0-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="059d0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="059d0-110">PARAMETERS</span></span>

### <span data-ttu-id="059d0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="059d0-111">-ApiId</span></span>
<span data-ttu-id="059d0-112">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="059d0-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="059d0-113">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="059d0-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="059d0-114">-AuthorizationScope</span></span>
<span data-ttu-id="059d0-115">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="059d0-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="059d0-116">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-116">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="059d0-117">-AuthorizationServerId</span></span>
<span data-ttu-id="059d0-118">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="059d0-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="059d0-119">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-119">The default value is $Null.</span></span>
<span data-ttu-id="059d0-120">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="059d0-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="059d0-121">-Context</span></span>
<span data-ttu-id="059d0-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="059d0-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="059d0-123">-Description</span></span>
<span data-ttu-id="059d0-124">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="059d0-124">Specifies a description for the web API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="059d0-125">-Name</span></span>
<span data-ttu-id="059d0-126">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="059d0-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="059d0-127">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="059d0-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-128">-Path</span><span class="sxs-lookup"><span data-stu-id="059d0-128">-Path</span></span>
<span data-ttu-id="059d0-129">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="059d0-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="059d0-130">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="059d0-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="059d0-131">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-131">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-132">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="059d0-132">-ProductIds</span></span>
<span data-ttu-id="059d0-133">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="059d0-133">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="059d0-134">-Protocols</span></span>
<span data-ttu-id="059d0-135">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="059d0-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="059d0-136">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="059d0-136">Valid values are http, https.</span></span>
<span data-ttu-id="059d0-137">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="059d0-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="059d0-138">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-138">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="059d0-139">-ServiceUrl</span></span>
<span data-ttu-id="059d0-140">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="059d0-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="059d0-141">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="059d0-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="059d0-142">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="059d0-142">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="059d0-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="059d0-144">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="059d0-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="059d0-145">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-145">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="059d0-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="059d0-147">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="059d0-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="059d0-148">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="059d0-148">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059d0-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059d0-149">-DefaultProfile</span></span>
<span data-ttu-id="059d0-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="059d0-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059d0-151">CommonParameters</span></span>
<span data-ttu-id="059d0-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059d0-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059d0-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="059d0-154">INPUTS</span></span>

## <span data-ttu-id="059d0-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="059d0-155">OUTPUTS</span></span>

### <span data-ttu-id="059d0-156">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="059d0-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="059d0-157">NOTES</span></span>

## <span data-ttu-id="059d0-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="059d0-158">RELATED LINKS</span></span>

[<span data-ttu-id="059d0-159">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="059d0-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="059d0-161">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="059d0-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="059d0-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="059d0-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


