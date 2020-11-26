---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321908"
---
# <span data-ttu-id="932a8-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="932a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="932a8-102">SYNOPSIS</span></span>
<span data-ttu-id="932a8-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="932a8-103">Modifies an API.</span></span>

## <span data-ttu-id="932a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="932a8-104">SYNTAX</span></span>

### <span data-ttu-id="932a8-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="932a8-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="932a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="932a8-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="932a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="932a8-107">DESCRIPTION</span></span>
<span data-ttu-id="932a8-108">Cmdleten **set-AzApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="932a8-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="932a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="932a8-109">EXAMPLES</span></span>

### <span data-ttu-id="932a8-110">Exempel 1: ändra ett API</span><span class="sxs-lookup"><span data-stu-id="932a8-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="932a8-111">Exempel 2: lägga till ett API i en befintlig ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="932a8-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="932a8-112">I det här exemplet läggs ett API till i en befintlig API-version</span><span class="sxs-lookup"><span data-stu-id="932a8-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="932a8-113">Exempel 3: ändra server delens ServiceUrl där API: t pekar</span><span class="sxs-lookup"><span data-stu-id="932a8-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="932a8-114">Det här exemplet uppdaterar ServiceUrl som `echo-api` pekar på.</span><span class="sxs-lookup"><span data-stu-id="932a8-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="932a8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="932a8-115">PARAMETERS</span></span>

### <span data-ttu-id="932a8-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="932a8-116">-ApiId</span></span>
<span data-ttu-id="932a8-117">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="932a8-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="932a8-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="932a8-118">-AuthorizationScope</span></span>
<span data-ttu-id="932a8-119">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="932a8-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="932a8-120">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="932a8-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="932a8-121">-AuthorizationServerId</span></span>
<span data-ttu-id="932a8-122">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="932a8-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="932a8-123">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-123">The default value is $Null.</span></span>
<span data-ttu-id="932a8-124">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="932a8-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="932a8-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="932a8-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="932a8-126">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="932a8-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="932a8-127">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="932a8-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="932a8-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="932a8-128">This parameter is optional.</span></span> <span data-ttu-id="932a8-129">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="932a8-129">Default value is $null.</span></span>

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

### <span data-ttu-id="932a8-130">-Kontext</span><span class="sxs-lookup"><span data-stu-id="932a8-130">-Context</span></span>
<span data-ttu-id="932a8-131">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="932a8-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="932a8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932a8-132">-DefaultProfile</span></span>
<span data-ttu-id="932a8-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="932a8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="932a8-134">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="932a8-134">-Description</span></span>
<span data-ttu-id="932a8-135">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="932a8-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="932a8-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="932a8-136">-InputObject</span></span>
<span data-ttu-id="932a8-137">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="932a8-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="932a8-138">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="932a8-138">This parameter is required.</span></span>

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

### <span data-ttu-id="932a8-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="932a8-139">-Name</span></span>
<span data-ttu-id="932a8-140">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="932a8-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="932a8-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="932a8-141">-OpenIdProviderId</span></span>
<span data-ttu-id="932a8-142">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="932a8-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="932a8-143">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="932a8-143">This parameter is optional.</span></span> <span data-ttu-id="932a8-144">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="932a8-144">Default value is $null.</span></span> <span data-ttu-id="932a8-145">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="932a8-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="932a8-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="932a8-146">-PassThru</span></span>
<span data-ttu-id="932a8-147">passthru</span><span class="sxs-lookup"><span data-stu-id="932a8-147">passthru</span></span>

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

### <span data-ttu-id="932a8-148">-Path</span><span class="sxs-lookup"><span data-stu-id="932a8-148">-Path</span></span>
<span data-ttu-id="932a8-149">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="932a8-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="932a8-150">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="932a8-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="932a8-151">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="932a8-152">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="932a8-152">-Protocols</span></span>
<span data-ttu-id="932a8-153">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="932a8-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="932a8-154">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="932a8-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="932a8-155">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="932a8-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="932a8-156">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="932a8-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="932a8-157">-ServiceUrl</span></span>
<span data-ttu-id="932a8-158">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="932a8-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="932a8-159">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="932a8-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="932a8-160">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="932a8-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="932a8-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="932a8-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="932a8-162">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="932a8-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="932a8-163">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="932a8-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="932a8-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="932a8-165">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="932a8-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="932a8-166">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="932a8-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="932a8-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="932a8-167">-SubscriptionRequired</span></span>
<span data-ttu-id="932a8-168">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="932a8-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="932a8-169">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="932a8-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="932a8-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932a8-170">CommonParameters</span></span>
<span data-ttu-id="932a8-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="932a8-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932a8-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="932a8-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932a8-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="932a8-173">INPUTS</span></span>

### <span data-ttu-id="932a8-174">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="932a8-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="932a8-175">System. String</span><span class="sxs-lookup"><span data-stu-id="932a8-175">System.String</span></span>

### <span data-ttu-id="932a8-176">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="932a8-177">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="932a8-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="932a8-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="932a8-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="932a8-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="932a8-179">OUTPUTS</span></span>

### <span data-ttu-id="932a8-180">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="932a8-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="932a8-181">NOTES</span></span>

## <span data-ttu-id="932a8-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="932a8-182">RELATED LINKS</span></span>

[<span data-ttu-id="932a8-183">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="932a8-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="932a8-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="932a8-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="932a8-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="932a8-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

