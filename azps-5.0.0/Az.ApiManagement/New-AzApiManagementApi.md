---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269688"
---
# <span data-ttu-id="07c1b-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="07c1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="07c1b-103">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="07c1b-103">Creates an API.</span></span>

## <span data-ttu-id="07c1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07c1b-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="07c1b-106">Cmdleten **New-AzApiManagementApi** skapar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="07c1b-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="07c1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="07c1b-108">Exempel 1: skapa ett API</span><span class="sxs-lookup"><span data-stu-id="07c1b-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="07c1b-109">Det här kommandot skapar ett API med namnet EchoApi med den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="07c1b-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="07c1b-110">Exempel 2: skapa ett API genom att kopiera all åtgärd, taggar, produkter och principer från eko-API och till en ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="07c1b-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="07c1b-111">Det här kommandot skapar ett API `echoapiv3` i ApiVersionSet `xmsVersionSet` och kopierar all åtgärd, taggar och principer från source API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="07c1b-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="07c1b-112">Den åsidosätter SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="07c1b-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="07c1b-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="07c1b-113">Example 3</span></span>

<span data-ttu-id="07c1b-114">Skapar ett API.</span><span class="sxs-lookup"><span data-stu-id="07c1b-114">Creates an API.</span></span> <span data-ttu-id="07c1b-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="07c1b-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="07c1b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07c1b-116">PARAMETERS</span></span>

### <span data-ttu-id="07c1b-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="07c1b-117">-ApiId</span></span>
<span data-ttu-id="07c1b-118">Anger ID för det API som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="07c1b-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="07c1b-119">Om du inte anger den här parametern skapar den här cmdleten ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="07c1b-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="07c1b-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07c1b-120">-ApiVersion</span></span>
<span data-ttu-id="07c1b-121">API-version av API för att skapa.</span><span class="sxs-lookup"><span data-stu-id="07c1b-121">Api Version of the Api to create.</span></span> <span data-ttu-id="07c1b-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="07c1b-123">-ApiVersionDescription</span></span>
<span data-ttu-id="07c1b-124">Beskrivning av API-version.</span><span class="sxs-lookup"><span data-stu-id="07c1b-124">Api Version Description.</span></span> <span data-ttu-id="07c1b-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="07c1b-126">-ApiVersionSetId</span></span>
<span data-ttu-id="07c1b-127">En resurs-ID för den relaterade API-versionen.</span><span class="sxs-lookup"><span data-stu-id="07c1b-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="07c1b-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="07c1b-129">-AuthorizationScope</span></span>
<span data-ttu-id="07c1b-130">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="07c1b-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="07c1b-131">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="07c1b-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="07c1b-132">-AuthorizationServerId</span></span>
<span data-ttu-id="07c1b-133">Anger ID för OAuth-Authorization-servern.</span><span class="sxs-lookup"><span data-stu-id="07c1b-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="07c1b-134">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-134">The default value is $Null.</span></span>
<span data-ttu-id="07c1b-135">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="07c1b-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="07c1b-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="07c1b-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="07c1b-137">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="07c1b-138">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="07c1b-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="07c1b-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-139">This parameter is optional.</span></span> <span data-ttu-id="07c1b-140">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-140">Default value is $null.</span></span>

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

### <span data-ttu-id="07c1b-141">-Kontext</span><span class="sxs-lookup"><span data-stu-id="07c1b-141">-Context</span></span>
<span data-ttu-id="07c1b-142">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="07c1b-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="07c1b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c1b-143">-DefaultProfile</span></span>
<span data-ttu-id="07c1b-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07c1b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c1b-145">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="07c1b-145">-Description</span></span>
<span data-ttu-id="07c1b-146">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="07c1b-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="07c1b-147">-Name</span></span>
<span data-ttu-id="07c1b-148">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="07c1b-149">Det här är det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="07c1b-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="07c1b-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="07c1b-150">-OpenIdProviderId</span></span>
<span data-ttu-id="07c1b-151">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="07c1b-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="07c1b-152">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-152">This parameter is optional.</span></span> <span data-ttu-id="07c1b-153">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-153">Default value is $null.</span></span> <span data-ttu-id="07c1b-154">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="07c1b-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="07c1b-155">-Path</span><span class="sxs-lookup"><span data-stu-id="07c1b-155">-Path</span></span>
<span data-ttu-id="07c1b-156">Anger webb API-sökvägen, som är den sista delen av API: s offentliga URL och motsvarar fältet Web API URL-suffix i administrations portalen.</span><span class="sxs-lookup"><span data-stu-id="07c1b-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="07c1b-157">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="07c1b-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="07c1b-158">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="07c1b-159">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="07c1b-159">-ProductIds</span></span>
<span data-ttu-id="07c1b-160">Anger en matris med produkt-ID: n där du kan lägga till det nya API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="07c1b-161">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="07c1b-161">-Protocols</span></span>
<span data-ttu-id="07c1b-162">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="07c1b-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="07c1b-163">Giltiga värden är http, https.</span><span class="sxs-lookup"><span data-stu-id="07c1b-163">Valid values are http, https.</span></span>
<span data-ttu-id="07c1b-164">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="07c1b-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="07c1b-165">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="07c1b-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="07c1b-166">-ServiceUrl</span></span>
<span data-ttu-id="07c1b-167">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="07c1b-168">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="07c1b-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="07c1b-169">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="07c1b-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="07c1b-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="07c1b-170">-SourceApiId</span></span>
<span data-ttu-id="07c1b-171">API-identifierare för käll-API.</span><span class="sxs-lookup"><span data-stu-id="07c1b-171">Api identifier of the source API.</span></span> <span data-ttu-id="07c1b-172">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="07c1b-173">-SourceApiRevision</span></span>
<span data-ttu-id="07c1b-174">API-revision av käll-API.</span><span class="sxs-lookup"><span data-stu-id="07c1b-174">Api Revision of the source API.</span></span> <span data-ttu-id="07c1b-175">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="07c1b-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="07c1b-177">Anger rubrik namnet för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="07c1b-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="07c1b-178">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="07c1b-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="07c1b-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="07c1b-180">Anger parameter namnet för frågesträngen för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="07c1b-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="07c1b-181">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="07c1b-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="07c1b-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="07c1b-182">-SubscriptionRequired</span></span>
<span data-ttu-id="07c1b-183">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="07c1b-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="07c1b-184">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07c1b-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="07c1b-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c1b-185">CommonParameters</span></span>
<span data-ttu-id="07c1b-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c1b-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c1b-187">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07c1b-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c1b-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07c1b-188">INPUTS</span></span>

### <span data-ttu-id="07c1b-189">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07c1b-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07c1b-190">System. String</span><span class="sxs-lookup"><span data-stu-id="07c1b-190">System.String</span></span>

### <span data-ttu-id="07c1b-191">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="07c1b-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="07c1b-192">System. string []</span><span class="sxs-lookup"><span data-stu-id="07c1b-192">System.String[]</span></span>

## <span data-ttu-id="07c1b-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07c1b-193">OUTPUTS</span></span>

### <span data-ttu-id="07c1b-194">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="07c1b-195">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07c1b-195">NOTES</span></span>

## <span data-ttu-id="07c1b-196">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07c1b-196">RELATED LINKS</span></span>

[<span data-ttu-id="07c1b-197">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="07c1b-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="07c1b-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="07c1b-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="07c1b-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07c1b-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


