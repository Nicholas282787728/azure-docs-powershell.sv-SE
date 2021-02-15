---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: c9b1519307c97712105e8e6f6e5a124d0337785a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214103"
---
# Restore-AzMySqlServer

## SYNOPSIS
Återställa en server från en befintlig säkerhetskopia

## SYNTAX

### GeoRestore (standard)
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESKRIVNING
Återställa en server från en befintlig säkerhetskopia

## EXEMPEL

### Exempel 1: Återställ MinQL-server med GeoReplica Restore
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Med den här cmdleten återställs MySql-servern med GeoReplica Restore.

### Exempel 2: Återställa MinQL-server med PointInTime-återställning
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Dessa cmdlets återställer MySql-servern med PointInTime Restore.

## PARAMETERS

### -As Ent
Kör kommandot som ett jobb.

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
Källserverobjektet att återställa från.
Skapa genom att gå till avsnittet NOTES för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Plats
Platsen som resursen finns i.

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

### -Name
Namnet på servern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Kör kommandot asynkront.

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

### -ResourceGroupName
Namnet på resursgruppen som innehåller resursen. Du kan hämta det här värdet från Azure Resource Manager API eller portalen.

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

### -RestorePointInTime
Platsen som resursen finns i.

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Namnet på SKU:n, vanligtvis nivå + familj + kärnor, t.ex. B_Gen4_1, GP_Gen5_8.

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

### -SubscriptionId
Det prenumerations-ID som identifierar en Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Programspecifika metadata i form av nyckelvärdepar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
Använda geoläge för att återställa

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
Använda PointInTime-läge för att återställa

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
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

### Microsoft.Azure.PowerShell.cmdlets.MySql.Models.Api20171201.IServer

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.MySql.Models.Api20171201.IServer

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> Det källserverobjekt som du vill återställa från.
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

