---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092726"
---
# <span data-ttu-id="99793-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="99793-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99793-102">SYNOPSIS</span></span>
<span data-ttu-id="99793-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="99793-103">Creates an API.</span></span>

## <span data-ttu-id="99793-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99793-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99793-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99793-105">DESCRIPTION</span></span>
<span data-ttu-id="99793-106">Cmdleten **New-AzApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="99793-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="99793-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99793-107">EXAMPLES</span></span>

### <span data-ttu-id="99793-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="99793-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="99793-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="99793-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="99793-110">Exempel 1: skapa ett API genom att kopiera all åtgärd, taggar, produkter och principer från eko-API och till en ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="99793-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="99793-111">Det här kommandot skapar ett API `echoapiv3` i ApiVersionSet `xmsVersionSet` och kopierar all åtgärd, taggar och principer från source API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="99793-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="99793-112">Den åsidosätter SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="99793-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="99793-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99793-113">PARAMETERS</span></span>

### <span data-ttu-id="99793-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="99793-114">-ApiId</span></span>
<span data-ttu-id="99793-115">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="99793-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="99793-116">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="99793-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="99793-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99793-117">-ApiVersion</span></span>
<span data-ttu-id="99793-118">API-version av API för att skapa.</span><span class="sxs-lookup"><span data-stu-id="99793-118">Api Version of the Api to create.</span></span> <span data-ttu-id="99793-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="99793-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="99793-120">-ApiVersionDescription</span></span>
<span data-ttu-id="99793-121">Beskrivning av API-version.</span><span class="sxs-lookup"><span data-stu-id="99793-121">Api Version Description.</span></span> <span data-ttu-id="99793-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="99793-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="99793-123">-ApiVersionSetId</span></span>
<span data-ttu-id="99793-124">En resurs-ID för den relaterade API-versionen.</span><span class="sxs-lookup"><span data-stu-id="99793-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="99793-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="99793-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="99793-126">-AuthorizationScope</span></span>
<span data-ttu-id="99793-127">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="99793-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="99793-128">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="99793-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="99793-129">-AuthorizationServerId</span></span>
<span data-ttu-id="99793-130">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="99793-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="99793-131">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-131">The default value is $Null.</span></span>
<span data-ttu-id="99793-132">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="99793-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="99793-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="99793-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="99793-134">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="99793-135">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="99793-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="99793-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-136">This parameter is optional.</span></span> <span data-ttu-id="99793-137">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="99793-137">Default value is $null.</span></span>

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

### <span data-ttu-id="99793-138">-Kontext</span><span class="sxs-lookup"><span data-stu-id="99793-138">-Context</span></span>
<span data-ttu-id="99793-139">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="99793-139">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99793-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99793-140">-DefaultProfile</span></span>
<span data-ttu-id="99793-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99793-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99793-142">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="99793-142">-Description</span></span>
<span data-ttu-id="99793-143">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="99793-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="99793-144">-Name</span></span>
<span data-ttu-id="99793-145">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="99793-146">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="99793-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="99793-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="99793-147">-OpenIdProviderId</span></span>
<span data-ttu-id="99793-148">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="99793-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="99793-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-149">This parameter is optional.</span></span> <span data-ttu-id="99793-150">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="99793-150">Default value is $null.</span></span> <span data-ttu-id="99793-151">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="99793-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="99793-152">-Path</span><span class="sxs-lookup"><span data-stu-id="99793-152">-Path</span></span>
<span data-ttu-id="99793-153">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="99793-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="99793-154">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="99793-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="99793-155">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="99793-156">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="99793-156">-ProductIds</span></span>
<span data-ttu-id="99793-157">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="99793-158">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="99793-158">-Protocols</span></span>
<span data-ttu-id="99793-159">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="99793-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="99793-160">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="99793-160">Valid values are http, https.</span></span>
<span data-ttu-id="99793-161">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="99793-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="99793-162">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-162">The default value is $Null.</span></span>

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

### <span data-ttu-id="99793-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="99793-163">-ServiceUrl</span></span>
<span data-ttu-id="99793-164">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="99793-165">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="99793-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="99793-166">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="99793-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="99793-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="99793-167">-SourceApiId</span></span>
<span data-ttu-id="99793-168">API-identifierare för käll-API.</span><span class="sxs-lookup"><span data-stu-id="99793-168">Api identifier of the source API.</span></span> <span data-ttu-id="99793-169">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="99793-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="99793-170">-SourceApiRevision</span></span>
<span data-ttu-id="99793-171">API-revision av käll-API.</span><span class="sxs-lookup"><span data-stu-id="99793-171">Api Revision of the source API.</span></span> <span data-ttu-id="99793-172">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="99793-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="99793-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="99793-174">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="99793-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="99793-175">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="99793-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="99793-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="99793-177">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="99793-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="99793-178">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="99793-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="99793-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="99793-179">-SubscriptionRequired</span></span>
<span data-ttu-id="99793-180">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="99793-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="99793-181">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="99793-181">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99793-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99793-182">CommonParameters</span></span>
<span data-ttu-id="99793-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99793-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99793-184">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99793-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99793-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99793-185">INPUTS</span></span>

### <span data-ttu-id="99793-186">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99793-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99793-187">System. String</span><span class="sxs-lookup"><span data-stu-id="99793-187">System.String</span></span>

### <span data-ttu-id="99793-188">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="99793-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="99793-189">System. string []</span><span class="sxs-lookup"><span data-stu-id="99793-189">System.String[]</span></span>

## <span data-ttu-id="99793-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99793-190">OUTPUTS</span></span>

### <span data-ttu-id="99793-191">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="99793-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99793-192">NOTES</span></span>

## <span data-ttu-id="99793-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99793-193">RELATED LINKS</span></span>

[<span data-ttu-id="99793-194">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="99793-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="99793-196">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="99793-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="99793-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="99793-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


