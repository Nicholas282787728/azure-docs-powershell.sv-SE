---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404181"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Skapar en serveranslutningskontext.

## SYNTAX

### ByServerNameWithSqlAuth (standard)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten New-AzureSqlDatabaseServerContext** skapar en Azure SQL Database-serveranslutningskontext.
Använd SQL Server-autentisering för att skapa en anslutningskontext till en SQL Database-server med hjälp av angivna autentiseringsuppgifter.
Du kan ange SQL Database-servern efter namn, med det fullständigt kvalificerade namnet eller efter URL.
Om du vill ha en autentiseringsuppgifter använder du cmdleten Get-Credential där du uppmanas att ange användarnamn och lösenord.

Använd **cmdleten New-AzureSqlDatabaseServerContext** med certifikatbaserad autentisering för att skapa ett anslutningssammanhang till den angivna SQL Database-servern med hjälp av angivna Azure-prenumerationsdata.
Du kan ange SQL Database Server efter namn eller efter fullständigt kvalificerat namn.
Du kan ange prenumerationsdata som en parameter eller så kan de hämtas från den aktuella Azure-prenumerationen.
Använd cmdleten Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx för att välja den aktuella Azure-prenumerationen.

## EXEMPEL

### Exempel 1: Skapa ett sammanhang med hjälp av SQL Server-autentisering
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

I det här exemplet används SQL Server-autentisering.

Det första kommandot uppmanar dig att ange autentiseringsuppgifter som serveradministratör och lagrar autentiseringsuppgifterna i $Credential variabeln.

Det andra kommandot ansluter till SQL Database-servern med namnet lpqd0zgav8y med hjälp av $Credential.

Det slutliga kommandot skapar en databas med namnet Databas17 på den server som ingår i kontexten i $Context.

### Exempel 2: Skapa ett sammanhang med hjälp av certifikatbaserad autentisering
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

I det här exemplet används den certifikatbaserade autentiseringen.

De två första kommandona tilldelar värden $SubscriptionId och $Thumbprint variabler.

Det tredje kommandot får certifikatet som identifieras av thumbprinten i $Thumbprint och lagrar det $Certificate.

Med det fjärde kommandot blir prenumerationen Prenumeration07 och det femte kommandot väljer prenumerationen.

Det slutliga kommandot skapar ett sammanhang i den aktuella prenumerationen för servern med namnet lpqd0zgav8y.

## PARAMETERS

### -Credential
Anger ett autentiseringsobjekt som ger dig tillgång till servern med SQL Server-autentisering.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Anger det fullständigt kvalificerade domännamnet (FQDN) för Azure SQL Database-servern.
Till exempel Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Anger URL-adressen som denna cmdlet använder för åtkomst till Azure SQL DatabaseManagement-portalen för servern.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Anger den Azure-profil som cmdleten läser upp.
Om du inte anger en profil läser den här cmdleten från den lokala standardprofilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servernamn
Anger namnet på databasservern.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Anger namnet på den Azure-prenumeration som denna cmdlet använder för att skapa anslutningskontexten.
Om du inte anger ett värde för den här parametern använder cmdleten den aktuella prenumerationen.
Kör cmdlet Select-AzureSubscription för att ändra den aktuella prenumerationen.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Anger att den här cmdleten använder Azure-prenumerationen för att skapa anslutningskontexten.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

## UTDATA

### Microsoft.WindowsAzure.Commands.sqlDatabase.Services.Server.iServerDataServiceContext

## ANTECKNINGAR
* Om du autentiserar utan att ange en domän, och om du använder Windows PowerShell 2.0, returnerar cmdleten Get-Credential ett omslutsstreck () före användarnamnet, till exempel \\ \användare. Windows PowerShell 3.0 lägger inte till det omde snedstrecket. Det här omslagsstrecket känns inte igen av parametern *Credential* för cmdleten **New-AzureSqlDatabaseServerContext.** Om du vill ta bort den använder du kommandon som ser ut ungefär så här:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## RELATERADE LÄNKAR



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


