---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: f1853c8f9e1e8449d0b607cadede215ec42b8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755782"
---
# New-AzureRmApiManagementAuthorizationServer

## Sammanfattning
Skapar en auktoriseringsprincip.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmApiManagementAuthorizationServer** skapar en auktoriseringsprincip för Azure API Management.

## BESKRIVS

### Exempel 1: skapa en auktoriseringsprincip
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

Det här kommandot skapar en auktoriseringsprincip.

## MALLPARAMETRAR

### -AccessTokenSendingMethods
Anger en matris med metoder för att skicka en åtkomsttoken.
psdx_paramvalues AuthorizationHeader och Query.

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

### -AuthorizationEndpointUrl
Anger behörighets slut punkten för att autentisera resurs ägare och erhålla godkännande.

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

### -AuthorizationRequestMethods
Anger en matris med metoder för godkännandebegäran.
Giltiga värden är: GET, POST.
Standardvärdet är GET.

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

### -ClientAuthenticationMethods
Anger en matris med autentiseringsmetoder för klienter.
psdx_paramvalues grundläggande och brödtext.

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

### -ClientId
Anger klient-ID för den utvecklings konsol som är klient programmet.

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

### -ClientRegistrationPageUrl
Anger slut punkten för klient registreringen för att registrera klienter med auktoriseringsservern och skaffa klient referenser.

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

### -ClientSecret
Anger klient hemligheten för den utvecklings konsol som är klient programmet.

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

### -Kontext
Anger ett **PsApiManagementContext** -objekt.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.
 
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

### -DefaultScope
Anger standard omfattning för auktoriseringsservern.

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

### -Beskrivning
Anger en beskrivning för en auktoriseringsprincip.

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

### -GrantTypes
Anger en matris med beviljande typer.
psdx_paramvalues

- AuthorizationCode
- ClientCredentials 
- Implicit 
- ResourceOwnerPassword

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

### -Namn
Anger namnet på den auktoriseringsprincip som ska skapas.

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

### -ResourceOwnerPassword
Anger ägar lösen ordet.
Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .

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

### -ResourceOwnerUsername
Anger resurs ägarens användar namn.
Du måste ange den här parametern om ResourceOwnerPassword anges i parametern *GrantTypes* .

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

### -ServerId
Anger ID för den auktoriseringsprincip som ska skapas.

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

### -SupportState
Anger om parametern *State* ska användas.

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

### -TokenBodyParameters
Anger ytterligare text parametrar med hjälp av **Application/x-www-form-urlencoded** format.

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

### -TokenEndpointUrl
Anger URL-adressen till den token som används av klienter för att få åtkomst till tokens i Exchange för att under rättas om godkännande bemyndiganden eller Refresh tokens.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

