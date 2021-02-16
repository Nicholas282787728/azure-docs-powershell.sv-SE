---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212246"
---
# Connect-AzAccount

## SYNOPSIS
Anslut till Azure med ett autentiserat konto för användning med cmdlets från Az PowerShell-modulerna.

## SYNTAX

### UserWithSubscriptionId (standard)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING

Cmdleten ansluter till Azure med ett autentiserat konto för användning med `Connect-AzAccount` cmdlets från Az PowerShell-modulerna. Du kan bara använda det autentiserade kontot med Azure Resource Manager-begäranden. Om du vill lägga till ett autentiserat konto för användning med Service Management använder du `Add-AzureAccount` cmdleten från Azure PowerShell-modulen. Om det inte finns något sammanhang för den aktuella användaren fylls användarens snabblista med ett sammanhang för var och en av de 25 första prenumerationerna.
Du hittar listan med sammanhang som skapats för användaren genom att `Get-AzContext -ListAvailable` köra. Om du vill hoppa över den här kontextpopulationen anger du **parametern SkipContext Population.** När du har kör denna cmdlet kan du koppla bort från ett Azure-konto med hjälp av `Disconnect-AzAccount` .

## EXEMPEL

### Exempel 1: Ansluta till ett Azure-konto

Det här exemplet ansluter till ett Azure-konto. Du måste ange ett Microsoft-konto eller autentiseringsuppgifter för organisations-ID. Om multifaktorautentisering har aktiverats för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens huvudautentisering.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 2: (Endast Windows PowerShell 5.1) Ansluta till Azure med autentiseringsuppgifter för organisations-ID

Det här scenariot fungerar bara i Windows PowerShell 5.1. Det första kommandot uppmanar användaren att ange autentiseringsuppgifter och lagrar dem i `$Credential` variabeln. Det andra kommandot ansluter till ett Azure-konto med autentiseringsuppgifterna som lagras `$Credential` i. Det här kontot autentiseras med Azure med autentiseringsuppgifter för organisations-ID.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 3: Ansluta till Azure med ett huvudkonto för tjänsten

Det första kommandot uppmanar dig att ange tjänstens huvudautentiseringsuppgifter och lagrar dem i `$Credential` variabeln. Ange ditt program-ID för användarnamnet och tjänstens huvudhemlighet som lösenordet när du uppmanas att göra det. Det andra kommandot ansluter den angivna Azure-innehavaren med hjälp av tjänstens huvudautentiseringsuppgifter som lagras i `$Credential` variabeln. **ServicePrincipal-växelparametern** anger att kontot autentiseras som en tjänsts huvudnamn.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 4: Använda en interaktiv inloggning för att ansluta till en viss klientorganisation och prenumeration

Det här exemplet ansluter till ett Azure-konto med den angivna klientorganisationen och prenumerationen.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 5: Ansluta med en hanterad tjänstidentitet

Det här exemplet ansluter med hjälp av MSI (Managed Service Identity) i värdmiljön. Du kan till exempel logga in på Azure från en virtuell dator som har en tilldelad MSI.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 6: Ansluta med identitetsinloggning för hanterad tjänst och Klientnr

Det här exemplet ansluter med hjälp av identiteten för hanterad tjänst i **myUserAssignedIdentity.** Det lägger till den användare som tilldelats identiteten på den virtuella datorn och ansluter sedan med klient-ID för den användare som tilldelats identiteten. Mer information finns i Konfigurera [hanterade identiteter för Azure-resurser på en Azure VM.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exempel 7: Ansluta med certifikat

Det här exemplet ansluter till ett Azure-konto med certifikatbaserad huvudautentisering för tjänsten.
Tjänstens huvudnamn som används för autentisering måste skapas med det angivna certifikatet. Mer information om hur du skapar ett själv signerat certifikat och tilldelar dem behörigheter finns i Använda Azure PowerShell för att skapa ett [tjänsthuvudnamn med ett certifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## PARAMETERS

### -AccessToken

Anger en åtkomsttoken.

> [!CAUTION]
> Åtkomsttoken är en typ av autentiseringsuppgifter. Du bör vidta lämpliga säkerhetsåtgärder för att hålla dem konfidentiella. Tidsgränsen för Access-token kan också förhindra att långvariga uppgifter slutförs.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId

Konto-ID för åtkomsttoken i **parameteruppsättningen i AccessToken.** Konto-ID för hanterad tjänst i **parameteruppsättningen ManagedService.** Kan vara ett hanterat tjänstresurs-ID eller det associerade klient-ID:t.
Lämna fältet tomt om du vill använda den systemidentitet som tilldelats.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Program-ID för tjänstens huvudnamn.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint

Hash-kod för certifikat eller Thumbprint.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContextName

Namn på standard-Azure-kontexten för den här inloggningen. Mer information om Azure-sammanhang finns i [Azure PowerShell-sammanhangsobjekt.](/powershell/azure/context-persistence)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential

Anger ett **PSCredential-objekt.** Om du vill ha mer information **om PSCredential-objektet** skriver du `Get-Help Get-Credential` . **PSCredential-objektet** anger användar-ID och lösenord för autentiseringsuppgifter för organisations-ID, eller program-ID och hemligt för tjänstens huvudautentiseringsuppgifter.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile

Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Miljö

Miljö som innehåller Azure-kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Skriva över det befintliga sammanhanget med samma namn utan att tillfrågas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken

AccessToken för Graph Service.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

Logga in med en identitet för hanterad tjänst.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken

AccessToken för KeyVault Service.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName

Föråldrad. Om du vill använda anpassad MSI-slutpunkt anger du MSI_ENDPOINT, t.ex. " http://localhost:50342/oauth2/token ". Värdnamn för den hanterade tjänsten.

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort

Föråldrad. Om du vill använda anpassad MSI-slutpunkt anger du MSI_ENDPOINT, t.ex. " http://localhost:50342/oauth2/token ". Portnummer för den hanterade tjänsten.

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret

Föråldrad. Om du vill använda anpassade MSI-hemliga inställningar anger du MSI_SECRET. Token för inloggning till den hanterade tjänsten.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxContextPopulation

Max prenumerationsnummer för att fylla i sammanhang efter inloggning. Standardvärdet är 25. Om du vill fylla i alla prenumerationer på sammanhang ställer du in på -1.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning

Avgör omfattningen av kontextändringar, till exempel om ändringar bara gäller den aktuella processen eller för alla sessioner som startas av användaren.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
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

Anger att det här kontot autentiseras genom att ange tjänstens huvudautentiseringsuppgifter.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipContextPopulation

Hoppar över en kontextpopulation om inga sammanhang hittas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipValidation

Hoppa över verifiering för åtkomsttoken.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prenumeration

Prenumerationsnamn eller ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Klientorganisation

Valfritt klientorganisationsnamn eller ID.

> [!NOTE]
> På grund av begränsningar i det aktuella API:t måste du använda ett klientorganisations-ID i stället för ett klientnamn när du ansluter med ett B2B-konto (företag till företag).

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication

Använd autentisering med enhetskod i stället för en webbläsarkontroll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta

Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## ANTECKNINGAR

## RELATERADE LÄNKAR
