---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 482a558e469e3f8094e4b619ef61ec37f076f739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091591"
---
# <span data-ttu-id="fa6b3-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="fa6b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6b3-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-103">Modifies an API.</span></span>

## <span data-ttu-id="fa6b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa6b3-104">SYNTAX</span></span>

### <span data-ttu-id="fa6b3-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="fa6b3-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa6b3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa6b3-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa6b3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa6b3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa6b3-108">Cmdleten **set-AzApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="fa6b3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa6b3-109">EXAMPLES</span></span>

### <span data-ttu-id="fa6b3-110">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="fa6b3-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="fa6b3-111">Exempel 2 lägga till ett API i en befintlig ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fa6b3-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="fa6b3-112">I det här exemplet läggs ett API till i en befintlig API-version</span><span class="sxs-lookup"><span data-stu-id="fa6b3-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="fa6b3-113">Exempel 3 ändra server delens ServiceUrl där API: t pekar</span><span class="sxs-lookup"><span data-stu-id="fa6b3-113">Example 3 Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="fa6b3-114">Det här exemplet uppdaterar ServiceUrl som `echo-api` pekar på.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="fa6b3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa6b3-115">PARAMETERS</span></span>

### <span data-ttu-id="fa6b3-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fa6b3-116">-ApiId</span></span>
<span data-ttu-id="fa6b3-117">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="fa6b3-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fa6b3-118">-AuthorizationScope</span></span>
<span data-ttu-id="fa6b3-119">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="fa6b3-120">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="fa6b3-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="fa6b3-121">-AuthorizationServerId</span></span>
<span data-ttu-id="fa6b3-122">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="fa6b3-123">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-123">The default value is $Null.</span></span>
<span data-ttu-id="fa6b3-124">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="fa6b3-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="fa6b3-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="fa6b3-126">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="fa6b3-127">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="fa6b3-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="fa6b3-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-128">This parameter is optional.</span></span> <span data-ttu-id="fa6b3-129">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-129">Default value is $null.</span></span>

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

### <span data-ttu-id="fa6b3-130">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fa6b3-130">-Context</span></span>
<span data-ttu-id="fa6b3-131">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fa6b3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6b3-132">-DefaultProfile</span></span>
<span data-ttu-id="fa6b3-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa6b3-134">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fa6b3-134">-Description</span></span>
<span data-ttu-id="fa6b3-135">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="fa6b3-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa6b3-136">-InputObject</span></span>
<span data-ttu-id="fa6b3-137">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="fa6b3-138">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fa6b3-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa6b3-139">-Name</span></span>
<span data-ttu-id="fa6b3-140">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="fa6b3-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="fa6b3-141">-OpenIdProviderId</span></span>
<span data-ttu-id="fa6b3-142">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="fa6b3-143">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-143">This parameter is optional.</span></span> <span data-ttu-id="fa6b3-144">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-144">Default value is $null.</span></span> <span data-ttu-id="fa6b3-145">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="fa6b3-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa6b3-146">-PassThru</span></span>
<span data-ttu-id="fa6b3-147">passthru</span><span class="sxs-lookup"><span data-stu-id="fa6b3-147">passthru</span></span>

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

### <span data-ttu-id="fa6b3-148">-Path</span><span class="sxs-lookup"><span data-stu-id="fa6b3-148">-Path</span></span>
<span data-ttu-id="fa6b3-149">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="fa6b3-150">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="fa6b3-151">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="fa6b3-152">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fa6b3-152">-Protocols</span></span>
<span data-ttu-id="fa6b3-153">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="fa6b3-154">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="fa6b3-155">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="fa6b3-156">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="fa6b3-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fa6b3-157">-ServiceUrl</span></span>
<span data-ttu-id="fa6b3-158">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="fa6b3-159">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="fa6b3-160">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="fa6b3-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fa6b3-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fa6b3-162">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="fa6b3-163">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="fa6b3-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fa6b3-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fa6b3-165">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="fa6b3-166">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="fa6b3-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="fa6b3-167">-SubscriptionRequired</span></span>
<span data-ttu-id="fa6b3-168">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="fa6b3-169">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa6b3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6b3-170">CommonParameters</span></span>
<span data-ttu-id="fa6b3-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6b3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6b3-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa6b3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6b3-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa6b3-173">INPUTS</span></span>

### <span data-ttu-id="fa6b3-174">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fa6b3-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fa6b3-175">System. String</span><span class="sxs-lookup"><span data-stu-id="fa6b3-175">System.String</span></span>

### <span data-ttu-id="fa6b3-176">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="fa6b3-177">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="fa6b3-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fa6b3-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa6b3-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa6b3-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa6b3-179">OUTPUTS</span></span>

### <span data-ttu-id="fa6b3-180">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fa6b3-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa6b3-181">NOTES</span></span>

## <span data-ttu-id="fa6b3-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa6b3-182">RELATED LINKS</span></span>

[<span data-ttu-id="fa6b3-183">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="fa6b3-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="fa6b3-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="fa6b3-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="fa6b3-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fa6b3-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


