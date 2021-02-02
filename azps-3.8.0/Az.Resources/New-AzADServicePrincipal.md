---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3a410dfb43cc767b0a73086147042425d42764d1
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251632"
---
# New-AzADServicePrincipal

## SYNOPSIS
Skapar ett nytt azure Active Directory-tjänsthuvudnamn.

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
Skapar ett nytt azure Active Directory-tjänsthuvudnamn. Standardparameteruppsättningen använder standardvärden för parametrar om användaren inte anger något för dem. Mer information om standardvärdena som används finns i beskrivningen för de givna parametrarna nedan.
Den här cmdleten har möjlighet att tilldela en roll till tjänstens huvudnamn med och parametrarna. Om ingen av dessa parametrar tillhandahålls kommer ingen roll att tilldelas `Role` `Scope` till tjänstens huvudnamn. Standardvärdena för och parametrarna är "Deltagare" respektive aktuell prenumeration (obs! Standardvärdena används endast när användaren anger ett värde för en av de två parametrarna, men inte för den `Role` `Scope` andra).
Cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte anges). Om du vill uppdatera programmets specifika parametrar använder du Set-AzADApplication cmdlet.

> [!WARNING]
> När du skapar en tjänsts **huvudnamn med kommandot New-AzADServicePrincipal** innehåller utdata autentiseringsuppgifter som du måste skydda. Alternativt kan du överväga att använda [hanterade identiteter för](/azure/active-directory/managed-identities-azure-resources/overview) att undvika att behöva använda autentiseringsuppgifter.
>
> Som standard **tilldelar New-AzADServicePrincipal** rollen [Deltagare](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvudnamn i prenumerationens omfattning. För att minska risken för ett komprometterat tjänsthuvudnamn, tilldelar du en mer specifik roll och begränsar omfattningen till en resurs eller resursgrupp. Mer information [finns i Steg för att lägga till](/azure/role-based-access-control/role-assignments-steps) en rolltilldelning.

## EXEMPEL

### Exempel 1 – Enkel huvudskapning av AD-tjänst

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Med kommandot ovan skapas ett AD-tjänsts huvudnamn med standardvärden för parametrar som inte anges. Eftersom inget program-ID tillhandahölls skapades ett program för tjänstens huvudnamn. Eftersom inga värden har angetts för, eller `Role` så har den skapade `Scope` tjänstens huvudnamn inga behörigheter.

### Exempel 2 – Enkel skapande av huvudnamn för AD-tjänsten med en angiven roll och standardomfattning

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

Kommandot ovan skapar ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte anges. Eftersom program-ID:t inte tillhandahölls skapades ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapades med behörigheten "Läsare" över den aktuella prenumerationen (eftersom inget värde angavs för `Scope` parametern).

### Exempel 3 – Enkel huvudskapning av AD-tjänsten med en angiven omfattning och standardroll

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Kommandot ovan skapar ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte anges. Eftersom program-ID:t inte tillhandahölls skapades ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapades med behörigheten "Deltagare" (eftersom inget värde har angetts för `Role` parametern) över den angivna resursgruppens omfattning.

### Exempel 4 – Enkel huvudskapning av AD-tjänsten med en angiven omfattning och roll

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Kommandot ovan skapar ett AD-tjänsthuvudnamn med standardvärdena för parametrar som inte anges. Eftersom program-ID:t inte tillhandahölls skapades ett program för tjänstens huvudnamn. Tjänstens huvudnamn skapades med läsbehörigheter över den angivna resursgruppomfattningen.

### Exempel 5 – Skapa ett nytt AD-tjänsthuvudnamn med program-ID med rolltilldelning

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Skapar ett nytt AD-tjänsthuvudnamn för programmet med program-ID '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'. Eftersom inga värden har angetts `Role` för, eller `Scope` så har den skapade tjänstens huvudnamn inga behörigheter.

### Exempel 6 – Skapa ett nytt AD-tjänsthuvudnamn med rörledning

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

Hämtar programmet med objekt-ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' och rör som till New-AzADServicePrincipal-cmdleten för att skapa ett nytt AD-tjänsthuvudnamn för programmet.

### Exempel 7 – Skapa ett nytt AD-tjänsthuvudnamn med hjälp av DisplayName och lösenordsuppgifter

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

Skapar ett nytt program med namnet "ServicePrincipalName" och lösenordet "StrongPassworld!23" och skapar tjänstens huvudnamn baserat på programmet som just skapades. Startdatumet och slutdatumet läggs till i lösenordsuppgifter.

### Exempel 8 : Skapa ett nytt AD-tjänsthuvudnamn med DisplayName och oformaterad nyckel

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

Skapar ett nytt program med namnet "ServicePrincipalName" och certifcate "$cert" och skapar tjänstens huvudnamn baserat på det program som nyss skapades. Slutdatumet läggs till i viktiga autentiseringsuppgifter.

## PARAMETERS

### -ApplicationId
Det unika program-ID:t för en tjänsts huvudnamn i en klientorganisation.
När du skapat den här egenskapen kan den här egenskapen inte ändras.
Om ett program-ID inte anges genereras ett.

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
Värdet för den asymmetriska autentiseringstypen.
Den representerar det 64-kodade bascertifikatet.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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
Eget namn på tjänstens huvudnamn. Om inget visningsnamn anges används det här värdet som standard för azure-powershell-MM-dd-yyyy-HH-mm-ss, där suffixet är tidpunkten då programmet skapades.

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
Slutdatumet för autentiseringsanvändningen.
Standardvärdet för slutdatum är ett år från i dag. För en "asymmetrisk" typ av autentiseringsuppgifter måste detta anges till på eller före datumet som X509-certifikatet är giltigt.

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
Den roll som tjänstens huvudnamn har i omfattningen. Om ett värde anges, men inget värde anges för, får deltagarerollen som `Scope` `Role` `Role` standard.

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
Omfattningen som tjänstens huvudnamn har behörigheter för. Om ett värde `Role` anges, men inget värde anges, används `Scope` den aktuella `Scope` prenumerationen som standard.

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
Om detta anges hoppar du över att skapa standardrolltilldelningen för tjänstens huvudnamn.

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
Startdatumet för autentiseringsanvändningen.
Standardinställningen för startdatum är idag. För en "asymmetrisk" typ av autentiseringsuppgifter måste detta anges till på eller efter datumet som X509-certifikatet är giltigt från.

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
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

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

