---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: c8ce26ba354f25066d7139318f5e6a5ec3e23c49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091584"
---
# <span data-ttu-id="ad08f-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ad08f-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="ad08f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad08f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad08f-103">Ändrar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="ad08f-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="ad08f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad08f-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad08f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad08f-105">DESCRIPTION</span></span>
<span data-ttu-id="ad08f-106">Cmdleten **set-AzApiManagementAuthorizationServer** ändrar Server informationen för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="ad08f-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="ad08f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad08f-107">EXAMPLES</span></span>

### <span data-ttu-id="ad08f-108">Exempel 1: ändra en auktoriseringsprincip</span><span class="sxs-lookup"><span data-stu-id="ad08f-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="ad08f-109">Det här kommandot ändrar den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="ad08f-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="ad08f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad08f-110">PARAMETERS</span></span>

### <span data-ttu-id="ad08f-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="ad08f-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="ad08f-112">Anger en matris med metoder för att skicka en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="ad08f-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="ad08f-113">psdx_paramvalues AuthorizationHeader och Query.</span><span class="sxs-lookup"><span data-stu-id="ad08f-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ad08f-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="ad08f-115">Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.</span><span class="sxs-lookup"><span data-stu-id="ad08f-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="ad08f-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="ad08f-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="ad08f-117">Anger en matris med metoder för godkännandebegäran.</span><span class="sxs-lookup"><span data-stu-id="ad08f-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="ad08f-118">psdx_paramvalues skaffa och publicera.</span><span class="sxs-lookup"><span data-stu-id="ad08f-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="ad08f-119">Standardvärdet är GET.</span><span class="sxs-lookup"><span data-stu-id="ad08f-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="ad08f-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="ad08f-121">Anger en matris med autentiseringsmetoder för klienter.</span><span class="sxs-lookup"><span data-stu-id="ad08f-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="ad08f-122">psdx_paramvalues grundläggande och brödtext.</span><span class="sxs-lookup"><span data-stu-id="ad08f-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ad08f-123">-ClientId</span></span>
<span data-ttu-id="ad08f-124">Anger klient-ID för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="ad08f-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="ad08f-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="ad08f-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="ad08f-126">Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.</span><span class="sxs-lookup"><span data-stu-id="ad08f-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="ad08f-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ad08f-127">-ClientSecret</span></span>
<span data-ttu-id="ad08f-128">Anger klient hemligheten för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="ad08f-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="ad08f-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ad08f-129">-Context</span></span>
<span data-ttu-id="ad08f-130">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad08f-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ad08f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad08f-131">-DefaultProfile</span></span>
<span data-ttu-id="ad08f-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad08f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad08f-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="ad08f-133">-DefaultScope</span></span>
<span data-ttu-id="ad08f-134">Anger standard omfattning för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="ad08f-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="ad08f-135">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ad08f-135">-Description</span></span>
<span data-ttu-id="ad08f-136">Anger en beskrivning för en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="ad08f-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="ad08f-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="ad08f-137">-GrantTypes</span></span>
<span data-ttu-id="ad08f-138">Anger en matris med beviljande typer.</span><span class="sxs-lookup"><span data-stu-id="ad08f-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="ad08f-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ad08f-139">psdx_paramvalues</span></span>
- <span data-ttu-id="ad08f-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="ad08f-140">AuthorizationCode</span></span>
- <span data-ttu-id="ad08f-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="ad08f-141">ClientCredentials</span></span> 
- <span data-ttu-id="ad08f-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="ad08f-142">Implicit</span></span> 
- <span data-ttu-id="ad08f-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="ad08f-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad08f-144">-Name</span></span>
<span data-ttu-id="ad08f-145">Anger namnet på den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ad08f-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="ad08f-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad08f-146">-PassThru</span></span>
<span data-ttu-id="ad08f-147">passthru</span><span class="sxs-lookup"><span data-stu-id="ad08f-147">passthru</span></span>

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

### <span data-ttu-id="ad08f-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="ad08f-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="ad08f-149">Anger ägar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="ad08f-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="ad08f-150">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="ad08f-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="ad08f-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="ad08f-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="ad08f-152">Anger resurs ägarens användar namn.</span><span class="sxs-lookup"><span data-stu-id="ad08f-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="ad08f-153">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="ad08f-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="ad08f-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ad08f-154">-ServerId</span></span>
<span data-ttu-id="ad08f-155">Anger ID: t för den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="ad08f-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="ad08f-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="ad08f-156">-SupportState</span></span>
<span data-ttu-id="ad08f-157">Anger om parametern *State* ska användas.</span><span class="sxs-lookup"><span data-stu-id="ad08f-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="ad08f-158">-TokenBodyParameters</span></span>
<span data-ttu-id="ad08f-159">Anger ytterligare text parametrar med hjälp av Application/x-www-form-urlencoded format.</span><span class="sxs-lookup"><span data-stu-id="ad08f-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08f-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ad08f-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="ad08f-161">Anger token-slutpunkten för klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.</span><span class="sxs-lookup"><span data-stu-id="ad08f-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="ad08f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad08f-162">CommonParameters</span></span>
<span data-ttu-id="ad08f-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad08f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad08f-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad08f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad08f-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad08f-165">INPUTS</span></span>

### <span data-ttu-id="ad08f-166">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad08f-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad08f-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ad08f-167">System.String</span></span>

### <span data-ttu-id="ad08f-168">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="ad08f-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="ad08f-169">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="ad08f-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="ad08f-170">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="ad08f-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="ad08f-171">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ad08f-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ad08f-172">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad08f-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ad08f-173">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="ad08f-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="ad08f-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad08f-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad08f-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad08f-175">OUTPUTS</span></span>

### <span data-ttu-id="ad08f-176">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ad08f-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="ad08f-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad08f-177">NOTES</span></span>

## <span data-ttu-id="ad08f-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad08f-178">RELATED LINKS</span></span>

[<span data-ttu-id="ad08f-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ad08f-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="ad08f-180">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ad08f-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="ad08f-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ad08f-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


