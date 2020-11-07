---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: ed7043746aa5ce59e733737acf8da61bdb44b0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757511"
---
# <span data-ttu-id="14f36-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14f36-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="14f36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14f36-102">SYNOPSIS</span></span>
<span data-ttu-id="14f36-103">Ändrar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="14f36-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14f36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14f36-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14f36-105">DESCRIPTION</span></span>
<span data-ttu-id="14f36-106">Cmdleten **set-AzureRmApiManagementAuthorizationServer** ändrar Server informationen för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="14f36-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="14f36-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14f36-107">EXAMPLES</span></span>

### <span data-ttu-id="14f36-108">Exempel 1: ändra en auktoriseringsprincip</span><span class="sxs-lookup"><span data-stu-id="14f36-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="14f36-109">Det här kommandot ändrar den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="14f36-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="14f36-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14f36-110">PARAMETERS</span></span>

### <span data-ttu-id="14f36-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="14f36-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="14f36-112">Anger en matris med metoder för att skicka en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="14f36-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="14f36-113">psdx_paramvalues AuthorizationHeader och Query.</span><span class="sxs-lookup"><span data-stu-id="14f36-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="14f36-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="14f36-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="14f36-115">Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.</span><span class="sxs-lookup"><span data-stu-id="14f36-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="14f36-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="14f36-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="14f36-117">Anger en matris med metoder för godkännandebegäran.</span><span class="sxs-lookup"><span data-stu-id="14f36-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="14f36-118">psdx_paramvalues skaffa och publicera.</span><span class="sxs-lookup"><span data-stu-id="14f36-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="14f36-119">Standardvärdet är GET.</span><span class="sxs-lookup"><span data-stu-id="14f36-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f36-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="14f36-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="14f36-121">Anger en matris med autentiseringsmetoder för klienter.</span><span class="sxs-lookup"><span data-stu-id="14f36-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="14f36-122">psdx_paramvalues grundläggande och brödtext.</span><span class="sxs-lookup"><span data-stu-id="14f36-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="14f36-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="14f36-123">-ClientId</span></span>
<span data-ttu-id="14f36-124">Anger klient-ID för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="14f36-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="14f36-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="14f36-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="14f36-126">Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.</span><span class="sxs-lookup"><span data-stu-id="14f36-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="14f36-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="14f36-127">-ClientSecret</span></span>
<span data-ttu-id="14f36-128">Anger klient hemligheten för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="14f36-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="14f36-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="14f36-129">-Context</span></span>
<span data-ttu-id="14f36-130">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="14f36-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="14f36-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="14f36-131">-DefaultScope</span></span>
<span data-ttu-id="14f36-132">Anger standard omfattning för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="14f36-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="14f36-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="14f36-133">-Description</span></span>
<span data-ttu-id="14f36-134">Anger en beskrivning för en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="14f36-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="14f36-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="14f36-135">-GrantTypes</span></span>
<span data-ttu-id="14f36-136">Anger en matris med beviljande typer.</span><span class="sxs-lookup"><span data-stu-id="14f36-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="14f36-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="14f36-137">psdx_paramvalues</span></span>

- <span data-ttu-id="14f36-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="14f36-138">AuthorizationCode</span></span>
- <span data-ttu-id="14f36-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="14f36-139">ClientCredentials</span></span> 
- <span data-ttu-id="14f36-140">Implicit</span><span class="sxs-lookup"><span data-stu-id="14f36-140">Implicit</span></span> 
- <span data-ttu-id="14f36-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="14f36-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="14f36-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="14f36-142">-Name</span></span>
<span data-ttu-id="14f36-143">Anger namnet på den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="14f36-143">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="14f36-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14f36-144">-PassThru</span></span>
<span data-ttu-id="14f36-145">passthru</span><span class="sxs-lookup"><span data-stu-id="14f36-145">passthru</span></span>

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

### <span data-ttu-id="14f36-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="14f36-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="14f36-147">Anger ägar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="14f36-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="14f36-148">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="14f36-148">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="14f36-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="14f36-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="14f36-150">Anger resurs ägarens användar namn.</span><span class="sxs-lookup"><span data-stu-id="14f36-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="14f36-151">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="14f36-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="14f36-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="14f36-152">-ServerId</span></span>
<span data-ttu-id="14f36-153">Anger ID: t för den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="14f36-153">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="14f36-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="14f36-154">-SupportState</span></span>
<span data-ttu-id="14f36-155">Anger om parametern *State* ska användas.</span><span class="sxs-lookup"><span data-stu-id="14f36-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="14f36-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="14f36-156">-TokenBodyParameters</span></span>
<span data-ttu-id="14f36-157">Anger ytterligare text parametrar med hjälp av Application/x-www-form-urlencoded format.</span><span class="sxs-lookup"><span data-stu-id="14f36-157">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="14f36-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="14f36-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="14f36-159">Anger token-slutpunkten för klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.</span><span class="sxs-lookup"><span data-stu-id="14f36-159">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="14f36-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f36-160">-DefaultProfile</span></span>
<span data-ttu-id="14f36-161">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14f36-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f36-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f36-162">CommonParameters</span></span>
<span data-ttu-id="14f36-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f36-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f36-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f36-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f36-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14f36-165">INPUTS</span></span>

## <span data-ttu-id="14f36-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14f36-166">OUTPUTS</span></span>

### <span data-ttu-id="14f36-167">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="14f36-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="14f36-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14f36-168">NOTES</span></span>

## <span data-ttu-id="14f36-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14f36-169">RELATED LINKS</span></span>

[<span data-ttu-id="14f36-170">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14f36-170">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="14f36-171">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14f36-171">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="14f36-172">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="14f36-172">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


