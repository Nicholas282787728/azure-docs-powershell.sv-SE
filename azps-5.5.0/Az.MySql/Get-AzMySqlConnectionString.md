---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: 65eb0d924391e6e12b3b81ac487b746e1b91fa94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226223"
---
# Get-AzMySqlConnectionString

## SYNOPSIS
Hämta anslutningssträngen enligt klientanslutningsleverantören.

## SYNTAX

### Hämta (standard)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESKRIVNING
Hämta anslutningssträngen enligt klientanslutningsleverantören.

## EXEMPEL

### Exempel 1: Hämta minQL-serveranslutningssträng efter resursgrupp och servernamn
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

Den här cmdleten får MySql-serveranslutningssträngen av resursgrupp och servernamn.

### Exempel 2: Hämta minQL-serveranslutningssträng efter identitet
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

Den här cmdleten får MySql-serveranslutningssträng efter identitet.

## PARAMETERS

### -Klient
Klientanslutningsleverantör.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Servern för anslutningssträngen.
Skapa genom att gå till avsnittet NOTES för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
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
Namnet på resursgruppen som innehåller resursen. Du kan hämta det här värdet från Azure Resource Manager API eller portalen.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.MySql.Models.Api20171201.IServer

## UTDATA

### System.String

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> Servern för anslutningssträngen.
  - `Location <String>`: Den geoplats där resursen finns
  - `[Tag <ITrackedResourceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[AdministratorLogin <String>]`: Administratörens inloggningsnamn för en server. Kan bara anges när servern skapas (och krävs för att kunna skapas).
  - `[EarliestRestoreDate <DateTime?>]`: Tidigaste tid då återställningspunkten skapades (ISO8601-format)
  - `[FullyQualifiedDomainName <String>]`: Det fullständigt kvalificerade domännamnet för en server.
  - `[IdentityType <IdentityType?>]`: Identitetstyp. Ställ in den på SystemAssigned för att automatiskt skapa och tilldela resursen ett Azure Active Directory-huvudnamn.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Status som visar om den serveraktiverade krypteringen av infrastrukturen visas.
  - `[MasterServerId <String>]`: Huvudserver-ID:t för en replikserver.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Framtvinga en minimal TLS-version för servern.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Oavsett om offentlig nätverksåtkomst tillåts för den här servern eller inte. Värdet är valfritt men om det överförs måste det vara Aktiverat eller Inaktiverat
  - `[ReplicaCapacity <Int32?>]`: Maximalt antal repliker som en huvudserver kan ha.
  - `[ReplicationRole <String>]`: Serverns replikeringsroll.
  - `[SkuCapacity <Int32?>]`: Upp-/utskalningskapaciteten, som representerar serverns beräkningsenheter.
  - `[SkuFamily <String>]`: Familjen av maskinvara.
  - `[SkuName <String>]`: Namnet på SKU:n, vanligtvis nivå + familj + kärnor, t.ex. B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Storlekskoden, som ska tolkas av resursen efter behov.
  - `[SkuTier <SkuTier?>]`: Nivån för en viss SKU, t.ex. Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivera ssl-tillämpning eller inte när du ansluter till servern.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Bevarandedagar för säkerhetskopiering för servern.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera Geo-redundant eller inte för säkerhetskopiering av servern.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera Utöka lagring automatiskt.
  - `[StorageProfileStorageMb <Int32?>]`: Maximalt tillåtna lagringsutrymme för en server.
  - `[UserVisibleState <ServerState?>]`: En status för en server som är synlig för användaren.
  - `[Version <ServerVersion?>]`: Serverversion.

## RELATERADE LÄNKAR

