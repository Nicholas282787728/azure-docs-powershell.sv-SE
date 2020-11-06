---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: cfba050b3ec6e464465d72e5f8d236f3b253fd0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578660"
---
# <span data-ttu-id="7bff7-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7bff7-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7bff7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bff7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bff7-103">Skapar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="7bff7-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bff7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bff7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bff7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bff7-105">DESCRIPTION</span></span>
<span data-ttu-id="7bff7-106">Cmdleten **New-AzureRmApiManagementAuthorizationServer** skapar en auktoriseringsprincip för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="7bff7-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="7bff7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bff7-107">EXAMPLES</span></span>

### <span data-ttu-id="7bff7-108">Exempel 1: skapa en auktoriseringsprincip</span><span class="sxs-lookup"><span data-stu-id="7bff7-108">Example 1: Create an authorization server</span></span>
```
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="7bff7-109">Det här kommandot skapar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="7bff7-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="7bff7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bff7-110">PARAMETERS</span></span>

### <span data-ttu-id="7bff7-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="7bff7-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="7bff7-112">Anger en matris med metoder för att skicka en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="7bff7-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="7bff7-113">psdx_paramvalues AuthorizationHeader och Query.</span><span class="sxs-lookup"><span data-stu-id="7bff7-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="7bff7-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="7bff7-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="7bff7-115">Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.</span><span class="sxs-lookup"><span data-stu-id="7bff7-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="7bff7-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="7bff7-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="7bff7-117">Anger en matris med metoder för godkännandebegäran.</span><span class="sxs-lookup"><span data-stu-id="7bff7-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="7bff7-118">Giltiga värden är: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="7bff7-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="7bff7-119">Standardvärdet är GET.</span><span class="sxs-lookup"><span data-stu-id="7bff7-119">The default value is GET.</span></span>

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

### <span data-ttu-id="7bff7-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="7bff7-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="7bff7-121">Anger en matris med autentiseringsmetoder för klienter.</span><span class="sxs-lookup"><span data-stu-id="7bff7-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="7bff7-122">psdx_paramvalues grundläggande och brödtext.</span><span class="sxs-lookup"><span data-stu-id="7bff7-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="7bff7-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="7bff7-123">-ClientId</span></span>
<span data-ttu-id="7bff7-124">Anger klient-ID för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="7bff7-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="7bff7-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="7bff7-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="7bff7-126">Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.</span><span class="sxs-lookup"><span data-stu-id="7bff7-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="7bff7-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="7bff7-127">-ClientSecret</span></span>
<span data-ttu-id="7bff7-128">Anger klient hemligheten för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="7bff7-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="7bff7-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7bff7-129">-Context</span></span>
<span data-ttu-id="7bff7-130">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7bff7-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7bff7-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="7bff7-131">-DefaultScope</span></span>
<span data-ttu-id="7bff7-132">Anger standard omfattning för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="7bff7-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="7bff7-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7bff7-133">-Description</span></span>
<span data-ttu-id="7bff7-134">Anger en beskrivning för en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="7bff7-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="7bff7-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="7bff7-135">-GrantTypes</span></span>
<span data-ttu-id="7bff7-136">Anger en matris med beviljande typer.</span><span class="sxs-lookup"><span data-stu-id="7bff7-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="7bff7-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="7bff7-137">psdx_paramvalues</span></span>

- <span data-ttu-id="7bff7-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="7bff7-138">AuthorizationCode</span></span>
- <span data-ttu-id="7bff7-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="7bff7-139">ClientCredentials</span></span> 
- <span data-ttu-id="7bff7-140">Implicit</span><span class="sxs-lookup"><span data-stu-id="7bff7-140">Implicit</span></span> 
- <span data-ttu-id="7bff7-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="7bff7-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="7bff7-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bff7-142">-Name</span></span>
<span data-ttu-id="7bff7-143">Anger namnet på den auktoriseringsprincip som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7bff7-143">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="7bff7-144">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="7bff7-144">-ResourceOwnerPassword</span></span>
<span data-ttu-id="7bff7-145">Anger ägar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="7bff7-145">Specifies the resource owner password.</span></span>
<span data-ttu-id="7bff7-146">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="7bff7-146">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="7bff7-147">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="7bff7-147">-ResourceOwnerUsername</span></span>
<span data-ttu-id="7bff7-148">Anger resurs ägarens användar namn.</span><span class="sxs-lookup"><span data-stu-id="7bff7-148">Specifies the resource owner user name.</span></span>
<span data-ttu-id="7bff7-149">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="7bff7-149">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="7bff7-150">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7bff7-150">-ServerId</span></span>
<span data-ttu-id="7bff7-151">Anger ID för den auktoriseringsprincip som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7bff7-151">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="7bff7-152">-SupportState</span><span class="sxs-lookup"><span data-stu-id="7bff7-152">-SupportState</span></span>
<span data-ttu-id="7bff7-153">Anger om parametern *State* ska användas.</span><span class="sxs-lookup"><span data-stu-id="7bff7-153">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="7bff7-154">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="7bff7-154">-TokenBodyParameters</span></span>
<span data-ttu-id="7bff7-155">Anger ytterligare text parametrar med hjälp av **Application/x-www-form-urlencoded** format.</span><span class="sxs-lookup"><span data-stu-id="7bff7-155">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="7bff7-156">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="7bff7-156">-TokenEndpointUrl</span></span>
<span data-ttu-id="7bff7-157">Anger URL-adressen till den token som används av klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.</span><span class="sxs-lookup"><span data-stu-id="7bff7-157">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="7bff7-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bff7-158">-DefaultProfile</span></span>
<span data-ttu-id="7bff7-159">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bff7-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bff7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bff7-160">CommonParameters</span></span>
<span data-ttu-id="7bff7-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bff7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bff7-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bff7-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bff7-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bff7-163">INPUTS</span></span>

## <span data-ttu-id="7bff7-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bff7-164">OUTPUTS</span></span>

### <span data-ttu-id="7bff7-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="7bff7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="7bff7-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bff7-166">NOTES</span></span>

## <span data-ttu-id="7bff7-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bff7-167">RELATED LINKS</span></span>

