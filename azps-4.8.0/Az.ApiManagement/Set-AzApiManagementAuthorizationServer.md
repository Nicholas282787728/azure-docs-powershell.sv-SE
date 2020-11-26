---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 4f484f200f2807cb814badbf93401061e670e72b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103341"
---
# <span data-ttu-id="c9307-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9307-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="c9307-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9307-102">SYNOPSIS</span></span>
<span data-ttu-id="c9307-103">Ändrar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c9307-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="c9307-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9307-104">SYNTAX</span></span>

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

## <span data-ttu-id="c9307-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9307-105">DESCRIPTION</span></span>
<span data-ttu-id="c9307-106">Cmdleten **set-AzApiManagementAuthorizationServer** ändrar Server informationen för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c9307-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="c9307-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9307-107">EXAMPLES</span></span>

### <span data-ttu-id="c9307-108">Exempel 1: ändra en auktoriseringsprincip</span><span class="sxs-lookup"><span data-stu-id="c9307-108">Example 1: Modify an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="c9307-109">Det här kommandot ändrar den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c9307-109">This command modifies the specified API Management authorization server.</span></span>

### <span data-ttu-id="c9307-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c9307-110">Example 2</span></span>

<span data-ttu-id="c9307-111">Ändrar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c9307-111">Modifies an authorization server.</span></span> <span data-ttu-id="c9307-112">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="c9307-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementAuthorizationServer -AccessTokenSendingMethods AuthorizationHeader -AuthorizationEndpointUrl 'https://contoso/authv2' -AuthorizationRequestMethods Get -ClientAuthenticationMethods Basic -ClientId 'clientid' -ClientRegistrationPageUrl 'https://contoso/signupv2' -ClientSecret '0000000000000000000000000000000000000' -Context <PsApiManagementContext> -DefaultScope <String> -GrantTypes AuthorizationCode -Name 'Contoso OAuth2 server' -ServerId 0123456789 -TokenEndpointUrl 'https://contoso/tokenv2'
```

## <span data-ttu-id="c9307-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9307-113">PARAMETERS</span></span>

### <span data-ttu-id="c9307-114">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="c9307-114">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="c9307-115">Anger en matris med metoder för att skicka en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="c9307-115">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="c9307-116">psdx_paramvalues AuthorizationHeader och Query.</span><span class="sxs-lookup"><span data-stu-id="c9307-116">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="c9307-117">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c9307-117">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="c9307-118">Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.</span><span class="sxs-lookup"><span data-stu-id="c9307-118">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="c9307-119">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="c9307-119">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="c9307-120">Anger en matris med metoder för godkännandebegäran.</span><span class="sxs-lookup"><span data-stu-id="c9307-120">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="c9307-121">psdx_paramvalues skaffa och publicera.</span><span class="sxs-lookup"><span data-stu-id="c9307-121">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="c9307-122">Standardvärdet är GET.</span><span class="sxs-lookup"><span data-stu-id="c9307-122">The default value is GET.</span></span>

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

### <span data-ttu-id="c9307-123">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="c9307-123">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="c9307-124">Anger en matris med autentiseringsmetoder för klienter.</span><span class="sxs-lookup"><span data-stu-id="c9307-124">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="c9307-125">psdx_paramvalues grundläggande och brödtext.</span><span class="sxs-lookup"><span data-stu-id="c9307-125">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="c9307-126">-ClientId</span><span class="sxs-lookup"><span data-stu-id="c9307-126">-ClientId</span></span>
<span data-ttu-id="c9307-127">Anger klient-ID för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="c9307-127">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="c9307-128">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="c9307-128">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="c9307-129">Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.</span><span class="sxs-lookup"><span data-stu-id="c9307-129">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="c9307-130">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="c9307-130">-ClientSecret</span></span>
<span data-ttu-id="c9307-131">Anger klient hemligheten för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="c9307-131">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="c9307-132">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c9307-132">-Context</span></span>
<span data-ttu-id="c9307-133">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c9307-133">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c9307-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9307-134">-DefaultProfile</span></span>
<span data-ttu-id="c9307-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9307-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9307-136">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="c9307-136">-DefaultScope</span></span>
<span data-ttu-id="c9307-137">Anger standard omfattning för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="c9307-137">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="c9307-138">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c9307-138">-Description</span></span>
<span data-ttu-id="c9307-139">Anger en beskrivning för en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c9307-139">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="c9307-140">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="c9307-140">-GrantTypes</span></span>
<span data-ttu-id="c9307-141">Anger en matris med beviljande typer.</span><span class="sxs-lookup"><span data-stu-id="c9307-141">Specifies an array of grant types.</span></span>
<span data-ttu-id="c9307-142">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c9307-142">psdx_paramvalues</span></span>
- <span data-ttu-id="c9307-143">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="c9307-143">AuthorizationCode</span></span>
- <span data-ttu-id="c9307-144">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="c9307-144">ClientCredentials</span></span> 
- <span data-ttu-id="c9307-145">Implicit</span><span class="sxs-lookup"><span data-stu-id="c9307-145">Implicit</span></span> 
- <span data-ttu-id="c9307-146">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="c9307-146">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="c9307-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9307-147">-Name</span></span>
<span data-ttu-id="c9307-148">Anger namnet på den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c9307-148">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="c9307-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9307-149">-PassThru</span></span>
<span data-ttu-id="c9307-150">passthru</span><span class="sxs-lookup"><span data-stu-id="c9307-150">passthru</span></span>

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

### <span data-ttu-id="c9307-151">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="c9307-151">-ResourceOwnerPassword</span></span>
<span data-ttu-id="c9307-152">Anger ägar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="c9307-152">Specifies the resource owner password.</span></span>
<span data-ttu-id="c9307-153">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="c9307-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="c9307-154">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="c9307-154">-ResourceOwnerUsername</span></span>
<span data-ttu-id="c9307-155">Anger resurs ägarens användar namn.</span><span class="sxs-lookup"><span data-stu-id="c9307-155">Specifies the resource owner user name.</span></span>
<span data-ttu-id="c9307-156">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="c9307-156">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="c9307-157">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c9307-157">-ServerId</span></span>
<span data-ttu-id="c9307-158">Anger ID: t för den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c9307-158">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="c9307-159">-SupportState</span><span class="sxs-lookup"><span data-stu-id="c9307-159">-SupportState</span></span>
<span data-ttu-id="c9307-160">Anger om parametern *State* ska användas.</span><span class="sxs-lookup"><span data-stu-id="c9307-160">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="c9307-161">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="c9307-161">-TokenBodyParameters</span></span>
<span data-ttu-id="c9307-162">Anger ytterligare text parametrar med hjälp av Application/x-www-form-urlencoded format.</span><span class="sxs-lookup"><span data-stu-id="c9307-162">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="c9307-163">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c9307-163">-TokenEndpointUrl</span></span>
<span data-ttu-id="c9307-164">Anger token-slutpunkten för klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.</span><span class="sxs-lookup"><span data-stu-id="c9307-164">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="c9307-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9307-165">CommonParameters</span></span>
<span data-ttu-id="c9307-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9307-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9307-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9307-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9307-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9307-168">INPUTS</span></span>

### <span data-ttu-id="c9307-169">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9307-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9307-170">System. String</span><span class="sxs-lookup"><span data-stu-id="c9307-170">System.String</span></span>

### <span data-ttu-id="c9307-171">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="c9307-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="c9307-172">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="c9307-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="c9307-173">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="c9307-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="c9307-174">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c9307-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c9307-175">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c9307-175">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c9307-176">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="c9307-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="c9307-177">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9307-177">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9307-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9307-178">OUTPUTS</span></span>

### <span data-ttu-id="c9307-179">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9307-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="c9307-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9307-180">NOTES</span></span>

## <span data-ttu-id="c9307-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9307-181">RELATED LINKS</span></span>

[<span data-ttu-id="c9307-182">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9307-182">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c9307-183">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9307-183">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c9307-184">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9307-184">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

