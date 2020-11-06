---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573384"
---
# Connect-AzureRmAccount

## Sammanfattning
Anslut till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### UserWithSubscriptionId (standard)
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Connect-AzureRmAccount cmdlet ansluter till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.

Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.

Använd Add-AzureAccount eller Import-AzurePublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.

När du har kört denna cmdlet kan du koppla ner från ett Azure-konto med AzureRmAccount.

## BESKRIVS

### Exempel 1: Använd en interaktiv inloggning för att ansluta till ett Azure-konto
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Det här kommandot ansluter till ett Azure-konto.

Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.

Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.

### Exempel 2: ansluta till ett Azure-konto med autentiseringsuppgifter för organisations-ID
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.

Det andra kommandot ansluter till ett Azure-konto med autentiseringsuppgifterna som lagras i $Credential.

Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.

Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.

### Exempel 3: ansluta till ett huvud konto för Azure-tjänsten
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.

Det andra kommandot ansluter till Azure med hjälp av tjänstens huvud uppgifter som lagrats i $Credential för den angivna innehavaren.

Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.

### Exempel 4: använda en interaktiv inloggning för att ansluta till ett konto för en viss klient organisation och prenumeration
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Det här kommandot ansluter till ett Azure-konto och konfigurerat AzureRM PowerShell för att köra cmdletar för angiven klient organisation och prenumeration som standard.

### Exempel 5: lägga till ett konto med inloggning med hanterad tjänst identitet
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Det här kommandot loggar in med den hanterade tjänst identiteten för värd miljön (om du till exempel körde det på en VirtualMachine med en tilldelad hanterad tjänst identitet, tillåter detta att koden loggar in med den tilldelade identiteten)

## MALLPARAMETRAR

### -AccessToken
Anger en åtkomsttoken.

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Konto-ID för åtkomsttoken

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
SPN

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Certifikat-hash (tumavtryck)

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContextName
Namn på standard kontext från den här inloggningen.  Du kan välja den här kontexten efter inloggning.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autentiseringsuppgift
Anger ett PSCredential-objekt.
Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.

PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### -Miljö
Miljö som innehåller kontot att logga in på

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Skriv över den befintliga kontexten med samma namn, om det finns någon.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
AccessToken för Graph-tjänsten

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Logga in med hanterad tjänst identitet i den aktuella miljön.

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken
AccessToken för valv tjänsten

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName
Värdnamn för hanterad tjänst inloggning

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort
Port nummer för hanterad tjänst inloggning

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning
Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipValidation
Hoppa över verifiering för åtkomsttoken

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnemang
Prenumerationens namn eller ID

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TenantId
Valfritt klient namn eller ID

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Strängvärdet
Parametern ' SubscriptionId ' godkänner värdet för typen String från pipeline

### Strängvärdet
Parametern ' SubscriptionName ' godkänner värdet för typen String från pipeline

## VÄRDEN

### PSAzureProfile
Autentiseringsuppgifter, prenumeration, konto och information om klient organisationen för den inloggade användaren.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

