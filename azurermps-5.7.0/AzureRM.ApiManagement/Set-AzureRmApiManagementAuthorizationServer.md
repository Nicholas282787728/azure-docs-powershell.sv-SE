---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 6424ad453d7e2ee3c4933127cc58e6d3e1193e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583704"
---
# <span data-ttu-id="7940e-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7940e-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7940e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7940e-102">SYNOPSIS</span></span>
<span data-ttu-id="7940e-103">Ändrar en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="7940e-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7940e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7940e-104">SYNTAX</span></span>

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

## <span data-ttu-id="7940e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7940e-105">DESCRIPTION</span></span>
<span data-ttu-id="7940e-106">Cmdleten **set-AzureRmApiManagementAuthorizationServer** ändrar Server informationen för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="7940e-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="7940e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7940e-107">EXAMPLES</span></span>

### <span data-ttu-id="7940e-108">Exempel 1: ändra en auktoriseringsprincip</span><span class="sxs-lookup"><span data-stu-id="7940e-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="7940e-109">Det här kommandot ändrar den angivna Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7940e-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="7940e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7940e-110">PARAMETERS</span></span>

### <span data-ttu-id="7940e-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="7940e-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="7940e-112">Anger en matris med metoder för att skicka en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="7940e-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="7940e-113">psdx_paramvalues AuthorizationHeader och Query.</span><span class="sxs-lookup"><span data-stu-id="7940e-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="7940e-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="7940e-115">Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.</span><span class="sxs-lookup"><span data-stu-id="7940e-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="7940e-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="7940e-117">Anger en matris med metoder för godkännandebegäran.</span><span class="sxs-lookup"><span data-stu-id="7940e-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="7940e-118">psdx_paramvalues skaffa och publicera.</span><span class="sxs-lookup"><span data-stu-id="7940e-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="7940e-119">Standardvärdet är GET.</span><span class="sxs-lookup"><span data-stu-id="7940e-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="7940e-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="7940e-121">Anger en matris med autentiseringsmetoder för klienter.</span><span class="sxs-lookup"><span data-stu-id="7940e-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="7940e-122">psdx_paramvalues grundläggande och brödtext.</span><span class="sxs-lookup"><span data-stu-id="7940e-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="7940e-123">-ClientId</span></span>
<span data-ttu-id="7940e-124">Anger klient-ID för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="7940e-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="7940e-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="7940e-126">Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.</span><span class="sxs-lookup"><span data-stu-id="7940e-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="7940e-127">-ClientSecret</span></span>
<span data-ttu-id="7940e-128">Anger klient hemligheten för den utvecklings konsol som är klient programmet.</span><span class="sxs-lookup"><span data-stu-id="7940e-128">Specifies the client secret of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7940e-129">-Context</span></span>
<span data-ttu-id="7940e-130">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7940e-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7940e-131">-DefaultProfile</span></span>
<span data-ttu-id="7940e-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7940e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="7940e-133">-DefaultScope</span></span>
<span data-ttu-id="7940e-134">Anger standard omfattning för auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="7940e-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-135">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7940e-135">-Description</span></span>
<span data-ttu-id="7940e-136">Anger en beskrivning för en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="7940e-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="7940e-137">-GrantTypes</span></span>
<span data-ttu-id="7940e-138">Anger en matris med beviljande typer.</span><span class="sxs-lookup"><span data-stu-id="7940e-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="7940e-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="7940e-139">psdx_paramvalues</span></span>

- <span data-ttu-id="7940e-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="7940e-140">AuthorizationCode</span></span>
- <span data-ttu-id="7940e-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="7940e-141">ClientCredentials</span></span> 
- <span data-ttu-id="7940e-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="7940e-142">Implicit</span></span> 
- <span data-ttu-id="7940e-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="7940e-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="7940e-144">-Name</span></span>
<span data-ttu-id="7940e-145">Anger namnet på den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="7940e-145">Specifies the name of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7940e-146">-PassThru</span></span>
<span data-ttu-id="7940e-147">passthru</span><span class="sxs-lookup"><span data-stu-id="7940e-147">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="7940e-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="7940e-149">Anger ägar lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="7940e-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="7940e-150">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="7940e-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="7940e-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="7940e-152">Anger resurs ägarens användar namn.</span><span class="sxs-lookup"><span data-stu-id="7940e-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="7940e-153">Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="7940e-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7940e-154">-ServerId</span></span>
<span data-ttu-id="7940e-155">Anger ID: t för den auktoriseringsprincip som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="7940e-155">Specifies the ID of the authorization server to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="7940e-156">-SupportState</span></span>
<span data-ttu-id="7940e-157">Anger om parametern *State* ska användas.</span><span class="sxs-lookup"><span data-stu-id="7940e-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="7940e-158">-TokenBodyParameters</span></span>
<span data-ttu-id="7940e-159">Anger ytterligare text parametrar med hjälp av Application/x-www-form-urlencoded format.</span><span class="sxs-lookup"><span data-stu-id="7940e-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="7940e-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="7940e-161">Anger token-slutpunkten för klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.</span><span class="sxs-lookup"><span data-stu-id="7940e-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7940e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7940e-162">CommonParameters</span></span>
<span data-ttu-id="7940e-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7940e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7940e-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7940e-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7940e-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7940e-165">INPUTS</span></span>

### <span data-ttu-id="7940e-166">Ingen</span><span class="sxs-lookup"><span data-stu-id="7940e-166">None</span></span>
<span data-ttu-id="7940e-167">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7940e-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7940e-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7940e-168">OUTPUTS</span></span>

### <span data-ttu-id="7940e-169">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="7940e-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="7940e-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7940e-170">NOTES</span></span>

## <span data-ttu-id="7940e-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7940e-171">RELATED LINKS</span></span>

[<span data-ttu-id="7940e-172">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7940e-172">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7940e-173">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7940e-173">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7940e-174">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7940e-174">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


