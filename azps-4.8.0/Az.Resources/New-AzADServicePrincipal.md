---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9fc7b3de271188c2f8ebd0be3293892a6fae56e3
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251785"
---
# New-AzADServicePrincipal

## SYNOPSIS
Skapar ett nytt Azure Active Directory-tjänsthuvudnamn.

## SYNTAX

### SimpleParameterSet (standard)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING

Skapar ett nytt Azure Active Directory-tjänsthuvudnamn. Standardparameteruppsättningen använder standardvärden för parametrar om de inte anges. Mer information om standardvärden finns i beskrivningen av varje parameter. Den här cmdleten har möjlighet att tilldela en roll till tjänstens huvudnamn med **parametrarna Roll** **och Omfattning.** Om båda utelämnas tilldelas deltagarrollen till tjänstens huvudnamn. Standardvärdena för **parametrarna Roll** **och Omfattning** är **Deltagare** för den aktuella prenumerationen. Cmdleten skapar ett program och anger dess egenskaper om inget ApplicationId tillhandahålls. Om du vill uppdatera programspecifika parametrar använder du [cmdleten Update-AzADApplication.](./update-azadapplication.md)

> [!WARNING]
> När du skapar en tjänsts **huvudnamn med kommandot New-AzADServicePrincipal** innehåller utdata autentiseringsuppgifter som du måste skydda. Alternativt kan du överväga att använda [hanterade identiteter för](/azure/active-directory/managed-identities-azure-resources/overview) att undvika att behöva använda autentiseringsuppgifter.
>
> Som standard **tilldelar New-AzADServicePrincipal** rollen [Deltagare](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvudnamn i prenumerationens omfattning. För att minska risken för ett komprometterat tjänsthuvudnamn, tilldelar du en mer specifik roll och begränsar omfattningen till en resurs eller resursgrupp. Mer information [finns i Steg för att lägga till](/azure/role-based-access-control/role-assignments-steps) en rolltilldelning.

## EXEMPEL

### Exempel 1: Enkel huvudskapning av AD-tjänsten

I följande exempel skapas ett AD-tjänsthuvudnamn med standardvärden för parametrar som inte har angetts. Eftersom inget program-ID tillhandahålls skapas ett program för tjänstens huvudnamn. Eftersom inga värden anges för **roll eller** **omfattning** tilldelas den skapade tjänstens huvudnamn **deltagarrollen** för den aktuella prenumerationen.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Exempel 2: Enkel huvudskapning av AD-tjänsten med en angiven roll och standardomfattning

I följande exempel skapas ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte har angetts. Eftersom program-ID:t inte tillhandahålls skapas ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapas med **läsbehörigheter** för den aktuella prenumerationen eftersom inget värde tillhandahålls för **omfattningsparametern.**

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### Exempel 3: Enkel huvudskapning av AD-tjänsten med en angiven omfattning och standardroll

I följande exempel skapas ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte har angetts. Eftersom program-ID:t inte tillhandahålls skapas ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapas med **behörigheten** Deltagare för den angivna resursgruppens omfattning eftersom inget värde anges för **rollparametern.**

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Exempel 4: Enkel huvudskapning av AD-tjänsten med en angiven omfattning och roll

I följande exempel skapas ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte har angetts. Eftersom program-ID:t inte tillhandahålls skapas ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapas med **läsbehörigheter** för den angivna resursgruppens omfattning.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Exempel 5: Skapa ett nytt AD-tjänsthuvudnamn med program-ID med rolltilldelning

I följande exempel skapas ett nytt AD-tjänsthuvudnamn för programmet med program-ID '00000000-0000-0000-0000-000000000000'. Eftersom inga värden anges för **roll eller** **omfattning** tilldelas den skapade tjänstens huvudnamn **deltagarrollen** för den aktuella prenumerationen.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Exempel 6: Skapa ett nytt AD-tjänsthuvudnamn med rörledning

I följande exempel hämtas programmet med objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' med [get-AzADApplication-cmdleten.](./get-azadapplication.md) Resultaten ledas till `New-AzADServicePrincipal` cmdleten för att skapa ett nytt AD-tjänsthuvudnamn för programmet.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Exempel 7: Skapa ett nytt AD-tjänsthuvudnamn med hjälp av DisplayName och lösenordsuppgifter

I följande exempel skapas ett nytt program med namnet **ServicePrincipalName** och ett lösenord för **StrongPassworld!23.** Tjänstens huvudnamn skapas baserat på det skapade programmet. Startdatumet och slutdatumet läggs till i lösenords credentialen.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### Exempel 8: Skapa ett nytt AD-tjänsthuvudnamn med DisplayName och oformaterad nyckel

I följande exempel skapas ett nytt program med namnet **ServicePrincipalName** och ett **$cert.** Tjänstens huvudnamn skapas baserat på det program som skapats. Slutdatumet läggs till i viktiga autentiseringsuppgifter.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMETERS

### -ApplicationId

Det unika program-ID:t för en tjänsts huvudnamn i en klientorganisation. När du skapat den här egenskapen kan den här egenskapen inte ändras. Om inget program-ID anges för ett befintligt program skapas ett program.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

Det objekt som representerar programmet som tjänstens huvudnamn skapas för.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Värdet för den asymmetriska typen av autentiseringsuppgifter. Den representerar base64-kodat certifikat.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DisplayName

Eget namn på tjänstens huvudnamn. Om inget visningsnamn anges används **azure-powershell-MM-dd-yyyy-HH-mm-ss** som standard, där suffixet är tidpunkten då programmet skapades.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

Slutdatumet för autentiseringsanvändningen. Standardvärdet för slutdatum är ett år från i dag.
För en asymmetrisk typ av autentiseringsuppgifter måste detta anges till på eller före datumet som X509-certifikatet är giltigt.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential

Samlingen med viktiga autentiseringsuppgifter som är kopplade till programmet.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

Den samling med lösenordsuppgifter som är kopplade till programmet.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role

Den roll som tjänstens huvudnamn har över omfattningen. Om inget värde anges används **rollrollen** som standard för **deltagarrollen.**

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning

Omfattningen som tjänstens huvudnamn har behörigheter för. Om inget värde anges används **den** aktuella prenumerationen som standard.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment

Hoppa över att skapa standardrolltilldelningen för tjänstens huvudnamn om detta anges.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startdatum

Startdatumet för autentiseringsanvändningen. Standardinställningen för startdatum är idag. För en asymmetrisk typ av autentiseringsuppgifter måste detta anges till det datum som X509-certifikatet är giltigt från eller efter det datum som X509-certifikatet är giltigt från.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)
## INDATA

### System.Guid

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

### Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]

### Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]

### System.DateTime

## UTDATA

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWra azure

## ANTECKNINGAR

Nyckelord: azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, mall, distribution

## RELATERADE LÄNKAR

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)
