---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099200"
---
# New-AzureSqlDatabaseServerContext

## Sammanfattning
Skapar en server anslutnings kontext.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **New-AzureSqlDatabaseServerContext** skapar en kontext för anslutning till en Azure SQL-databasserver.
Använd SQL Server-autentisering för att skapa en anslutnings kontext till en SQL-databasserver med hjälp av de angivna autentiseringsuppgifterna.
Du kan ange SQL Server-servern efter namn, efter det fullständiga namnet eller URL-adressen.
För att få en autentiseringsuppgift kan du använda Get-Credential cmdlet som uppmanar dig att ange användar namn och lösen ord.

Använd cmdleten **New-AzureSqlDatabaseServerContext** med certifikatbaserad inloggningsautentisering för att skapa en anslutnings kontext till angiven SQL-databasserver med de angivna Azure-prenumerationens data.
Du kan ange SQL-databasserver via namn eller med det fullständigt kvalificerade namnet.
Du kan ange abonnemangs data som en parameter eller kan hämtas från det nuvarande Azure-abonnemanget.
Använd cmdleten Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx för att välja det aktuella Azure-abonnemanget.

## BESKRIVS

### Exempel 1: skapa en kontext med SQL Server-identifiering
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

I det här exemplet används SQL Server-identifieringen.

I det första kommandot uppmanas du att ange Server administratörs uppgifter och autentiseringsuppgifterna lagras i $Credential variabel.

Det andra kommandot ansluter till SQL-databas servern med namnet lpqd0zbr8y med hjälp av $Credential.

Med kommandot Final skapas en databas som heter Database17 på den server som är en del av kontexten i $Context.

### Exempel 2: skapa en kontext med certifikatbaserad inloggningsautentisering
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

I det här exemplet används certifikatbaserad lösenordsautentisering.

De två första kommandona tilldelar värden till $SubscriptionId och $Thumbprint variabler.

Det tredje kommandot får certifikatet som identifieras av tumavtrycket i $Thumbprint och lagrar det i $Certificate.

Det fjärde kommandot anger att prenumerationen ska vara Subscription07 och det femte kommandot väljer abonnemanget.

Med kommandot slut skapas en kontext i den aktuella prenumerationen för den server som heter lpqd0zbr8y.

## MALLPARAMETRAR

### -Autentiseringsuppgift
Anger ett objekt som ger SQL Server-autentisering för dig åtkomst till servern.

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
Anger FQDN-namnet (fullkvalificerat domän namn) för Azure SQL Database-servern.
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
Anger URL-adressen som används för att komma åt DatabaseManagement-portalen för Azure SQL för servern.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -ServerName
Anger namnet på databas servern.

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
Anger namnet på den Azure-prenumeration som denna cmdlet använder för att skapa anslutnings kontexten.
Om du inte anger ett värde för denna parameter används den aktuella prenumerationen i cmdleten.
Kör cmdleten Select-AzureSubscription om du vill ändra det aktuella abonnemanget.

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
Anger att denna cmdlet använder Azure-prenumeration för att skapa en anslutnings kontext.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. IServerDataServiceContext

## ANMÄRKNINGAR
* Om du verifierar utan att ange en domän och om du använder Windows PowerShell 2,0 returnerar Get-Credential cmdleten ett omvänt snedstreck ( \\ ) läggs till till användar namnet, till exempel \user. Windows PowerShell 3,0 lägger inte till omvända snedstreck. Det omvända snedstrecket känns inte igen av parametern *Credential* i cmdleten **New-AzureSqlDatabaseServerContext** . Om du vill ta bort den använder du kommandon som ser ut ungefär så här:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## RELATERADE LÄNKAR

[Azure SQL-databas-cmdletar](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


