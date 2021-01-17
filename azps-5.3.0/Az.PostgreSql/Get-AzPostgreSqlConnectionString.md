---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421344"
---
# Get-AzPostgreSqlConnectionString

## Sammanfattning
Hämta anslutnings strängen enligt klient anslutnings leverantören.

## FRÅGESYNTAXEN

### Skaffa (standard)
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta anslutnings strängen enligt klient anslutnings leverantören.

## BESKRIVS

### Exempel 1: skaffa PostgreSql Server anslutnings sträng efter resurs grupp och Server namn
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

Denna cmdlet hämtar PostgreSql för Server anslutningar efter resurs grupp och Server namn.

### Exempel 2: Hämta PostgreSql Server anslutnings sträng efter identitet
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

Denna cmdlet får PostgreSql Server anslutnings sträng efter identitet.

## MALLPARAMETRAR

### -Klient
Klient anslutnings leverantör.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Käll Server objekt för att skapa replik från.
För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på servern.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen som innehåller resursen kan du hämta det här värdet från Azure Resource Manager API eller portalen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Det prenumerations-ID som identifierar en Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer

## VÄRDEN

### System. String

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : käll Server objekt för att skapa replik från.
  - `Location <String>`: Platsen som resursen finns i.
  - `[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av par med nyckelvärdena.
    - `[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[AdministratorLogin <String>]`: Administratörens inloggnings namn för en server. Kan bara anges när servern skapas (och krävs för att skapa).
  - `[EarliestRestoreDate <DateTime?>]`: Tidig skapelse tid för återställnings punkt (ISO8601-format)
  - `[FullyQualifiedDomainName <String>]`: Serverns fullkvalificerade domän namn.
  - `[IdentityType <IdentityType?>]`: Identitets typen. Ställ in detta på ' SystemAssigned ' för att automatiskt skapa och tilldela en Azure Active Directory-Huvudplats för resursen.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om infrastrukturen för infrastruktur är aktive rad.
  - `[MasterServerId <String>]`: Huvud serverns ID för en replik Server.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Påtvinga en minimal TLS-version för servern.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oberoende nätverks åtkomst tillåts för den här servern. Värdet är valfritt, men om det är skickat måste det vara aktiverat eller inaktiverat
  - `[ReplicaCapacity <Int32?>]`: Det högsta antalet repliker som en huvud server kan ha.
  - `[ReplicationRole <String>]`: Serverns replikeringsrelation.
  - `[SkuCapacity <Int32?>]`: Skalan upp/ut-kapacitet som representerar serverns beräknade enheter.
  - `[SkuFamily <String>]`: Produkt familjen.
  - `[SkuName <String>]`: Namnet på SKU: n, vanligt vis nivå + Family + cores, till exempel B_Gen4_1 GP_Gen5_8.
  - `[SkuSize <String>]`: Storleks koden, som ska tolkas av resursen.
  - `[SkuTier <SkuTier?>]`: Nivån för den aktuella SKU: n, t. ex.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivera SSL-tvång eller inte vid anslutning till server.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Bevarande dagar för säkerhets kopior för servern.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller ej för säkerhets kopiering av Server.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera automatisk tillväxt av lagring.
  - `[StorageProfileStorageMb <Int32?>]`: Högsta tillåtna lagrings utrymme för en server.
  - `[UserVisibleState <ServerState?>]`: Ett tillstånd för en server som är synlig för användaren.
  - `[Version <ServerVersion?>]`: Server version.

## RELATERADE LÄNKAR

