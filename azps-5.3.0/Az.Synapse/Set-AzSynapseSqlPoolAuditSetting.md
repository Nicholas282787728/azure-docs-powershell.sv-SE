---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523909"
---
# Set-AzSynapseSqlPoolAuditSetting

## Sammanfattning
Ändrar gransknings inställningarna för en Azure Synapse-BA SQL-pool.

## FRÅGESYNTAXEN

### SetByNameParameterSet (standard)
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByParentObjectParameterSet
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzSynapseSqlPoolAuditSetting** ändrar gransknings inställningarna för en Azure SYNAPSE Analytics SQL-pool.
När Blob Storage är ett mål för gransknings loggar anger du parametern *StorageAccountResourceId* för att bestämma lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna. Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

Aktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.

### Exempel 2
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

Inaktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.

### Exempel 3
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

Aktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool med avancerad filtrering med ett T-SQL-predikat.

### Exempel 4
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

Ta bort inställningen Advanced filter from gransknings principen för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool.

### Exempel 5
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

Inaktivera gransknings principen för blob-lagring för en Azure Synapse Analytics SQL-pool med namnet ContosoSqlPool via pipeline.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

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

### -AuditAction
Uppsättningen gransknings åtgärder.

De åtgärder som stöds för granskning är:

ANVÄNDA

UPPDATERA

Placera

TA bort

GENOMFÖR

MOTTAR

INNEHÅLLER

Det allmänna formuläret för att definiera en åtgärd som ska granskas är:

\[åtgärd \] för \[ objekt \] efter \[ huvud konto\]

Observera att \[ objektet \] i ovanstående format kan referera till ett objekt, till exempel en tabell, en vy eller en lagrad procedur eller en hel databas eller ett helt schema.
För de sistnämnda fallen är formulär databasen:: \[ dbname \] och schema:: \[ SchemaName \] används.

Till exempel:

Välj i dbo. nontable av offentlig

Välj på databas:: min databas av offentlig

Välj på SCHEMA:: mina schema av offentlig

Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuditActionGroup
Den rekommenderade uppsättningen åtgärds grupper som ska användas är följande kombination – detta granskar alla frågor och lagrade procedurer som körs mot databasen samt lyckade och misslyckade inloggningar:



"BATCH_COMPLETED_GROUP",

"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",

"FAILED_DATABASE_AUTHENTICATION_GROUP"

Ovanstående kombination är även den uppsättning som är konfigurerad som standard.
Dessa grupper täcker alla SQL-uttryck och lagrade procedurer som körs mot databasen och ska inte användas i kombination med andra grupper eftersom detta kommer att leda till dubbletter av gransknings loggar.

Mer information finns i https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobStorageTargetState
Anger om Blob Storage är en destination för gransknings poster.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -InputObject
Objekt i SQL-pool, vanligt vis passerar genom pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namn på SQL-poolen Synapse.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Denna cmdlet returnerar inte ett objekt som standard.
Om denna växel anges returnerar den sant om den är klar.

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

### -PredicateExpression
Uttrycket T-SQL predikat (WHERE-satsen) som används för att filtrera gransknings loggar.

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

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID för Synapse SQL-pool.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionInDays
Antalet bevarande dagar för gransknings loggar.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceId
Resurs-ID för lagrings konto

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

### -StorageKeyType
Anger vilken av lagrings åtkomst nycklar som ska användas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Namn på Synapse-arbetsyta.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
objekt för arbets yta, vanligt vis passerar genom pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace

### Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool

## VÄRDEN

### Microsoft. Azure. commands. Synapse. Models. SqlPoolAuditModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
