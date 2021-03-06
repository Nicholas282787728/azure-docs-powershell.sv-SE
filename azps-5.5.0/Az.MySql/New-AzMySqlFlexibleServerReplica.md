---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 5b201a035dbd919223d12c5205c4a154bc16fc2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226166"
---
# New-AzMySqlFlexibleServerReplica

## SYNOPSIS
Skapar en replikserver för en flexibel MySQL-server

## SYNTAX

```
New-AzMySqlFlexibleServerReplica -Replica <String> -ResourceGroupName <String> -Master <IServerAutoGenerated>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## BESKRIVNING
Skapar en ny kopia från en befintlig databas.

## EXEMPEL

### Exempel 1: Skapa en ny MySql-serverreplikator
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlFlexibleServerReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----               -------- ------------------ ------- ----------------------- -------       -------        
mysql-test-replica westus2   mysql_test         5.7     10240                   Standard_B1ms Burstable
```

Denna cmdlet skapar en ny MySql-serverreplikator.

### Exempel 2: Skapa en ny MySql-serverreplikator
```powershell
PS C:\> $mysql = Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlFlexibleServerReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----               -------- ------------------ ------- ----------------------- -------       -------        
mysql-test-replica westus2   mysql_test         5.7     10240                   Standard_B1ms Burstable
```

Den här cmdleten med parameterbakgrund (inputobject) skapar en ny MySql-serverreplik.

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

### -Master
Källserverobjektet som ska skapas av en kopia.
Skapa genom att gå till avsnittet ANTECKNINGAR för EGENSKAPER FÖR HUVUD och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Kopia
Namnet på servern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

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
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


MASTER: <IServerAutoGenerated> Källserverobjektet att skapa kopia från.
  - `Location <String>`: Den geoplats där resursen finns
  - `[Tag <ITrackedResourceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[AdministratorLogin <String>]`: Administratörens inloggningsnamn för en server. Kan bara anges när servern skapas (och krävs för att kunna skapas).
  - `[AdministratorLoginPassword <String>]`: Lösenordet för administratörsinloggningen (krävs för att skapa servern).
  - `[AvailabilityZone <String>]`: information om tillgänglighetszon på servern.
  - `[CreateMode <CreateMode?>]`: Läget för att skapa en ny MySQL-server.
  - `[DelegatedSubnetArgumentSubnetArmResourceId <String>]`: armresurs-ID för delegerat undernät.
  - `[HaEnabled <HaEnabledEnum?>]`: Aktivera HA eller inte för en server.
  - `[IdentityType <ResourceIdentityType?>]`: Identitetstyp.
  - `[InfrastructureEncryption <InfrastructureEncryptionEnum?>]`: Status som visar om den serveraktiverade krypteringen av infrastrukturen visas.
  - `[MaintenanceWindowCustomWindow <String>]`: anger om anpassat fönster är aktiverat eller inaktiverat
  - `[MaintenanceWindowDayOfWeek <Int32?>]`: dag i veckan för fönstret för underhåll
  - `[MaintenanceWindowStartHour <Int32?>]`: starttimme för underhållsfönster
  - `[MaintenanceWindowStartMinute <Int32?>]`: startminut för underhållsfönster
  - `[PropertiesTag <IServerPropertiesTags>]`: Programspecifika metadata i form av nyckelvärdespar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[ReplicationRole <String>]`: Replikeringsrollen.
  - `[RestorePointInTime <DateTime?>]`: Tid för att skapa återställningspunkt (ISO8601-format), som anger tiden för återställning från.
  - `[SkuName <String>]`: SKU:ns namn, t.ex. Standard_D32s_v3.
  - `[SkuTier <SkuTier?>]`: Nivån för en viss SKU, t.ex. GeneralPurpose.
  - `[SourceServerId <String>]`: MittQL-källserver-ID.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivera ssl-tillämpning eller inte när du ansluter till servern.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Bevarandedagar för säkerhetskopiering för servern.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivera Utöka lagring automatiskt.
  - `[StorageProfileStorageIop <Int32?>]`: Storage IOPS för en server.
  - `[StorageProfileStorageMb <Int32?>]`: Maximalt tillåtna lagringsutrymme för en server.
  - `[Version <ServerVersion?>]`: Serverversion.

## RELATERADE LÄNKAR

