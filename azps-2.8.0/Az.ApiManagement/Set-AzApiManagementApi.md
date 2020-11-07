---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745679"
---
# <span data-ttu-id="9625b-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="9625b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9625b-102">SYNOPSIS</span></span>
<span data-ttu-id="9625b-103">Ändrar ett API.</span><span class="sxs-lookup"><span data-stu-id="9625b-103">Modifies an API.</span></span>

## <span data-ttu-id="9625b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9625b-104">SYNTAX</span></span>

### <span data-ttu-id="9625b-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="9625b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9625b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9625b-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9625b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9625b-107">DESCRIPTION</span></span>
<span data-ttu-id="9625b-108">Cmdleten **set-AzApiManagementApi** ändrar ett API för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9625b-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="9625b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9625b-109">EXAMPLES</span></span>

### <span data-ttu-id="9625b-110">Exempel 1 ändra ett API</span><span class="sxs-lookup"><span data-stu-id="9625b-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="9625b-111">Exempel 2 lägga till ett API i en befintlig ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9625b-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="9625b-112">I det här exemplet läggs ett API till i en befintlig API-version</span><span class="sxs-lookup"><span data-stu-id="9625b-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="9625b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9625b-113">PARAMETERS</span></span>

### <span data-ttu-id="9625b-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9625b-114">-ApiId</span></span>
<span data-ttu-id="9625b-115">Anger ID för det API som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="9625b-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="9625b-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9625b-116">-AuthorizationScope</span></span>
<span data-ttu-id="9625b-117">Anger omfattningen för OAuth-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="9625b-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9625b-118">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="9625b-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9625b-119">-AuthorizationServerId</span></span>
<span data-ttu-id="9625b-120">Anger ID för servern för OAuth-auktorisering.</span><span class="sxs-lookup"><span data-stu-id="9625b-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="9625b-121">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-121">The default value is $Null.</span></span>
<span data-ttu-id="9625b-122">Du måste ange den här parametern om *AuthorizationScope* har angetts.</span><span class="sxs-lookup"><span data-stu-id="9625b-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="9625b-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="9625b-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="9625b-124">OpenId som används för att skicka åtkomsttoken till API: t.</span><span class="sxs-lookup"><span data-stu-id="9625b-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="9625b-125">Se http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="9625b-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="9625b-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9625b-126">This parameter is optional.</span></span> <span data-ttu-id="9625b-127">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="9625b-127">Default value is $null.</span></span>

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

### <span data-ttu-id="9625b-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9625b-128">-Context</span></span>
<span data-ttu-id="9625b-129">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9625b-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9625b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9625b-130">-DefaultProfile</span></span>
<span data-ttu-id="9625b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9625b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9625b-132">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9625b-132">-Description</span></span>
<span data-ttu-id="9625b-133">Anger en beskrivning för webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="9625b-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="9625b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9625b-134">-InputObject</span></span>
<span data-ttu-id="9625b-135">Instans av PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="9625b-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="9625b-136">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9625b-136">This parameter is required.</span></span>

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

### <span data-ttu-id="9625b-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="9625b-137">-Name</span></span>
<span data-ttu-id="9625b-138">Anger namnet på webb-API: t.</span><span class="sxs-lookup"><span data-stu-id="9625b-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="9625b-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="9625b-139">-OpenIdProviderId</span></span>
<span data-ttu-id="9625b-140">OpenId för identitets Server.</span><span class="sxs-lookup"><span data-stu-id="9625b-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="9625b-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9625b-141">This parameter is optional.</span></span> <span data-ttu-id="9625b-142">Standardvärdet är $null.</span><span class="sxs-lookup"><span data-stu-id="9625b-142">Default value is $null.</span></span> <span data-ttu-id="9625b-143">Måste anges om BearerTokenSendingMethods har angetts.</span><span class="sxs-lookup"><span data-stu-id="9625b-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="9625b-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9625b-144">-PassThru</span></span>
<span data-ttu-id="9625b-145">passthru</span><span class="sxs-lookup"><span data-stu-id="9625b-145">passthru</span></span>

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

### <span data-ttu-id="9625b-146">-Path</span><span class="sxs-lookup"><span data-stu-id="9625b-146">-Path</span></span>
<span data-ttu-id="9625b-147">Anger webb-API-sökvägen, som är den sista delen av API: s offentliga URL.</span><span class="sxs-lookup"><span data-stu-id="9625b-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="9625b-148">Denna URL används av API-konsumenter för att skicka en begäran till webb tjänsten och måste vara en till 400 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9625b-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9625b-149">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="9625b-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9625b-150">-Protocols</span></span>
<span data-ttu-id="9625b-151">Anger en matris med webb-API-protokoll.</span><span class="sxs-lookup"><span data-stu-id="9625b-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9625b-152">psdx_paramvalues http och https.</span><span class="sxs-lookup"><span data-stu-id="9625b-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="9625b-153">Det här är de webb protokoll som API: et är tillgängligt för.</span><span class="sxs-lookup"><span data-stu-id="9625b-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9625b-154">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="9625b-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9625b-155">-ServiceUrl</span></span>
<span data-ttu-id="9625b-156">Anger URL-adressen till webb tjänsten som visar API: t.</span><span class="sxs-lookup"><span data-stu-id="9625b-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9625b-157">Denna URL används endast av Azure API Management och är inte offentlig.</span><span class="sxs-lookup"><span data-stu-id="9625b-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9625b-158">URL-adressen måste vara en till 2000 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9625b-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="9625b-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9625b-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9625b-160">Anger namnet på abonnemangs rubriken.</span><span class="sxs-lookup"><span data-stu-id="9625b-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="9625b-161">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="9625b-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9625b-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9625b-163">Anger namnet på parametern för frågesträngen för abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="9625b-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="9625b-164">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9625b-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="9625b-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9625b-165">-SubscriptionRequired</span></span>
<span data-ttu-id="9625b-166">Flagga för att påtvinga SubscriptionRequired för förfrågningar till API: t.</span><span class="sxs-lookup"><span data-stu-id="9625b-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="9625b-167">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9625b-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="9625b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9625b-168">CommonParameters</span></span>
<span data-ttu-id="9625b-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9625b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9625b-170">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9625b-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9625b-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9625b-171">INPUTS</span></span>

### <span data-ttu-id="9625b-172">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9625b-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9625b-173">System. String</span><span class="sxs-lookup"><span data-stu-id="9625b-173">System.String</span></span>

### <span data-ttu-id="9625b-174">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="9625b-175">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="9625b-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9625b-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9625b-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9625b-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9625b-177">OUTPUTS</span></span>

### <span data-ttu-id="9625b-178">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9625b-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9625b-179">NOTES</span></span>

## <span data-ttu-id="9625b-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9625b-180">RELATED LINKS</span></span>

[<span data-ttu-id="9625b-181">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9625b-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9625b-183">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9625b-184">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9625b-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9625b-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


