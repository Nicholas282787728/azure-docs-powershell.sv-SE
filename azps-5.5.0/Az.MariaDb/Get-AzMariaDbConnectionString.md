---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224334"
---
# Get-AzMariaDbConnectionString

## SYNOPSIS
Hämta anslutningssträng för en MariaDB under ett visst ramverk.

## SYNTAX

### Servernamn (standard)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESKRIVNING
Hämta anslutningssträng för en MariaDB under ett visst ramverk.

## EXEMPEL

### Exempel 1: Hämta en anslutningssträng för MariaDB
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

Det här kommandot får en anslutningssträng av MariaDB.

### Exempel 2: Hämta en anslutningssträng för MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

Det här kommandot får en anslutningssträng av MariaDB.

## PARAMETERS

### -Klient
Anslut klienttyp

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
region DefaultParameters Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
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
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen som innehåller resursen.

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Prenumerations-ID är en del av URI:n för varje servicesamtal

```yaml
Type: System.String
Parameter Sets: ServerName
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

### Microsoft.Azure.PowerShell.cmdlets.MariaDb.Models.Api20180601Preview.IServer

## UTDATA

### System.String

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : Identity Parameter
  - `Location <String>`: Platsen som resursen finns i.
  - `[Tag <ITrackedResourceTags>]`: Programspecifika metadata i form av nyckelvärdepar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[AdministratorLogin <String>]`: Administratörens inloggningsnamn för en server. Kan bara anges när servern skapas (och krävs för att kunna skapas).
  - `[EarliestRestoreDate <DateTime?>]`: Tidigaste tid då återställningspunkten skapades (ISO8601-format)
  - `[FullyQualifiedDomainName <String>]`: Det fullständigt kvalificerade domännamnet för en server.
  - `[IdentityType <IdentityType?>]`: Identitetstyp. Ställ in den på SystemAssigned för att automatiskt skapa och tilldela resursen ett Azure Active Directory-huvudnamn.
  - `[MasterServerId <String>]`: Huvudserver-ID:t för en replikserver.
  - `[ReplicaCapacity <Int32?>]`: Maximalt antal repliker som en huvudserver kan ha.
  - `[ReplicationRole <String>]`: Serverns replikeringsroll.
  - `[SkuCapacity <Int32?>]`: Upp-/utskalningskapaciteten, som representerar serverns beräkningsenheter.
  - `[SkuFamily <String>]`: Familjen med maskinvara.
  - `[SkuName <String>]`: Namnet på SKU:n, vanligtvis nivå + familj + kärnor, t.ex. B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Storlekskoden, som ska tolkas av resursen efter behov.
  - `[SkuTier <SkuTier?>]`: Nivån för en viss SKU, t.ex. Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivera ssl-tillämpning eller inte när du ansluter till servern.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Bevarandedagar för säkerhetskopiering för servern.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivera geo-redundanta eller inte för serversäkerhetskopiering.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera Utöka lagring automatiskt.
  - `[StorageProfileStorageMb <Int32?>]`: Maximalt tillåtna lagringsutrymme för en server.
  - `[UserVisibleState <ServerState?>]`: En status för en server som är synlig för användaren.
  - `[Version <ServerVersion?>]`: Serverversion.

## RELATERADE LÄNKAR

