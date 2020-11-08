---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: e7074b799e1c664ceb17499b04b8d4d2ff3acb5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091590"
---
# <span data-ttu-id="f30a1-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f30a1-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="f30a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f30a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f30a1-103">Ändrar en API-revision</span><span class="sxs-lookup"><span data-stu-id="f30a1-103">Modifies an API Revision</span></span>

## <span data-ttu-id="f30a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f30a1-104">SYNTAX</span></span>

### <span data-ttu-id="f30a1-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="f30a1-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30a1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f30a1-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f30a1-107">DESCRIPTION</span></span>
<span data-ttu-id="f30a1-108">Cmdleten **set-AzApiManagementApiRevision** ändrar en Azure API-revision för API.</span><span class="sxs-lookup"><span data-stu-id="f30a1-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="f30a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f30a1-109">EXAMPLES</span></span>

### <span data-ttu-id="f30a1-110">Exempel 1 ändra en API-revision</span><span class="sxs-lookup"><span data-stu-id="f30a1-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="f30a1-111">Cmdleten uppdaterar `2` ändringen av API: t `echo-api` med en ny beskrivning, protokoll och sökväg.</span><span class="sxs-lookup"><span data-stu-id="f30a1-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="f30a1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f30a1-112">PARAMETERS</span></span>

### <span data-ttu-id="f30a1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f30a1-113">-ApiId</span></span>
<span data-ttu-id="f30a1-114">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="f30a1-114">Identifier of existing API.</span></span>
<span data-ttu-id="f30a1-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f30a1-116">-ApiRevision</span></span>
<span data-ttu-id="f30a1-117">Identifierare för befintlig API-revision.</span><span class="sxs-lookup"><span data-stu-id="f30a1-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="f30a1-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f30a1-119">-AuthorizationScope</span></span>
<span data-ttu-id="f30a1-120">Scope för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f30a1-120">OAuth operations scope.</span></span>
<span data-ttu-id="f30a1-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-121">This parameter is optional.</span></span>
<span data-ttu-id="f30a1-122">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-122">Default value is $null.</span></span>

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

### <span data-ttu-id="f30a1-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f30a1-123">-AuthorizationServerId</span></span>
<span data-ttu-id="f30a1-124">ID för OAuth-Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="f30a1-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="f30a1-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-125">This parameter is optional.</span></span>
<span data-ttu-id="f30a1-126">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-126">Default value is $null.</span></span>
<span data-ttu-id="f30a1-127">Måste anges om AuthorizationScope har angetts.</span><span class="sxs-lookup"><span data-stu-id="f30a1-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="f30a1-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="f30a1-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="f30a1-129">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="f30a1-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="f30a1-130">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="f30a1-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="f30a1-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-131">This parameter is optional.</span></span> <span data-ttu-id="f30a1-132">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-132">Default value is $null.</span></span>

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

### <span data-ttu-id="f30a1-133">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f30a1-133">-Context</span></span>
<span data-ttu-id="f30a1-134">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f30a1-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f30a1-135">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-135">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30a1-136">-DefaultProfile</span></span>
<span data-ttu-id="f30a1-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f30a1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30a1-138">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f30a1-138">-Description</span></span>
<span data-ttu-id="f30a1-139">Beskrivning av Web API.</span><span class="sxs-lookup"><span data-stu-id="f30a1-139">Web API description.</span></span>
<span data-ttu-id="f30a1-140">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="f30a1-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f30a1-141">-InputObject</span></span>
<span data-ttu-id="f30a1-142">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="f30a1-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="f30a1-143">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="f30a1-144">-Name</span></span>
<span data-ttu-id="f30a1-145">Webb-API-namn.</span><span class="sxs-lookup"><span data-stu-id="f30a1-145">Web API name.</span></span>
<span data-ttu-id="f30a1-146">Det offentliga namnet på API: t som visas på portalerna för utvecklare och administratörer.</span><span class="sxs-lookup"><span data-stu-id="f30a1-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="f30a1-147">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-147">This parameter is required.</span></span>

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

### <span data-ttu-id="f30a1-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="f30a1-148">-OpenIdProviderId</span></span>
<span data-ttu-id="f30a1-149">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="f30a1-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="f30a1-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-150">This parameter is optional.</span></span> <span data-ttu-id="f30a1-151">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-151">Default value is $null.</span></span> <span data-ttu-id="f30a1-152">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="f30a1-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="f30a1-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f30a1-153">-PassThru</span></span>
<span data-ttu-id="f30a1-154">Om det anges kommer instansen av Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi typ som representerar set API.</span><span class="sxs-lookup"><span data-stu-id="f30a1-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="f30a1-155">-Path</span><span class="sxs-lookup"><span data-stu-id="f30a1-155">-Path</span></span>
<span data-ttu-id="f30a1-156">Web API Path.</span><span class="sxs-lookup"><span data-stu-id="f30a1-156">Web API Path.</span></span>
<span data-ttu-id="f30a1-157">Sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="f30a1-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="f30a1-158">Denna URL kommer att användas av API-konsumenter för att skicka förfrågningar till webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f30a1-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f30a1-159">Måste vara 1 till 400 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="f30a1-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f30a1-160">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-160">This parameter is optional.</span></span>
<span data-ttu-id="f30a1-161">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-161">Default value is $null.</span></span>

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

### <span data-ttu-id="f30a1-162">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f30a1-162">-Protocols</span></span>
<span data-ttu-id="f30a1-163">Webb-API-protokoll (http, https).</span><span class="sxs-lookup"><span data-stu-id="f30a1-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="f30a1-164">Protokoll som finns tillgängliga för API.</span><span class="sxs-lookup"><span data-stu-id="f30a1-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="f30a1-165">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-165">This parameter is required.</span></span>
<span data-ttu-id="f30a1-166">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-166">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f30a1-167">-ServiceUrl</span></span>
<span data-ttu-id="f30a1-168">En URL för webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="f30a1-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="f30a1-169">Denna URL kommer endast att användas av Azure API Management och blir inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="f30a1-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="f30a1-170">Måste vara 1 till 2000 tecken långt.</span><span class="sxs-lookup"><span data-stu-id="f30a1-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="f30a1-171">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f30a1-171">This parameter is required.</span></span>

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

### <span data-ttu-id="f30a1-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="f30a1-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f30a1-173">Rubrik namn för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f30a1-173">Subscription key header name.</span></span>
<span data-ttu-id="f30a1-174">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-174">This parameter is optional.</span></span>
<span data-ttu-id="f30a1-175">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-175">Default value is $null.</span></span>

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

### <span data-ttu-id="f30a1-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f30a1-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f30a1-177">Namn på frågesträng för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="f30a1-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="f30a1-178">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-178">This parameter is optional.</span></span>
<span data-ttu-id="f30a1-179">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="f30a1-179">Default value is $null.</span></span>

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

### <span data-ttu-id="f30a1-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f30a1-180">-SubscriptionRequired</span></span>
<span data-ttu-id="f30a1-181">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="f30a1-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="f30a1-182">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f30a1-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="f30a1-183">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f30a1-183">-Confirm</span></span>
<span data-ttu-id="f30a1-184">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f30a1-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30a1-185">-WhatIf</span></span>
<span data-ttu-id="f30a1-186">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f30a1-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30a1-187">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f30a1-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30a1-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30a1-188">CommonParameters</span></span>
<span data-ttu-id="f30a1-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30a1-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30a1-190">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f30a1-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30a1-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f30a1-191">INPUTS</span></span>

### <span data-ttu-id="f30a1-192">System. String</span><span class="sxs-lookup"><span data-stu-id="f30a1-192">System.String</span></span>

### <span data-ttu-id="f30a1-193">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f30a1-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f30a1-194">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f30a1-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="f30a1-195">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="f30a1-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f30a1-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f30a1-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f30a1-197">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f30a1-197">OUTPUTS</span></span>

### <span data-ttu-id="f30a1-198">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f30a1-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f30a1-199">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f30a1-199">NOTES</span></span>

## <span data-ttu-id="f30a1-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f30a1-200">RELATED LINKS</span></span>

[<span data-ttu-id="f30a1-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f30a1-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="f30a1-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f30a1-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="f30a1-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f30a1-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)