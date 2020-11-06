---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574767"
---
# Set-AzureRmSqlDatabaseAuditingPolicy

## Sammanfattning
Anger gransknings principen för en databas.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmSqlDatabaseAuditingPolicy** ändrar gransknings principen för en Azure SQL-databas.
Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.
Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.
Du kan också definiera bevarande för tabellen gransknings loggar genom att ange värdet för parametrarna *RetentionInDays* och *TableIdentifier* för att definiera perioden och dirigeringen för tabell namnen för gransknings loggen.
Ange parametern *EventType* för att definiera vilka händelse typer som ska granskas.
När cmdleten körs är den aktive rad.
För tabell granskning slutar granskning sluta använda den principen om databasen använde serverns princip för granskning innan du körde den här cmdleten. För att en BLOB-granskning ska visas om databasen använde serverns princip för granskning innan du körde den här cmdleten finns båda gransknings principerna sida vid sida.
Om cmdleten lyckas och du använder *Passthru* -parametern returneras ett objekt som avbeskriverr den aktuella gransknings principen utöver databasens identifierare.
Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.
Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.

## BESKRIVS

### Exempel 1: Ange gransknings principen för en databas för att använda tabell granskning
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att använda lagrings kontot som heter Storage31.

### Exempel 2: Ange lagrings konto nycklar för en befintlig gransknings princip för en databas
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

Det här kommandot anger den gransknings princip för databasen som heter Database01 på Server01 för att fortsätta använda samma lagrings konto namn men för att nu använda den sekundära knappen.

### Exempel 3: Ange gransknings principen för en databas för att använda en viss händelse typ
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### Exempel 4: Ange gransknings principen för en databas för att använda BLOB-granskning
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

Det här kommandot anger gransknings principen för databasen som heter Database01 på Server01.
Principen loggar händelse typen för Login_Failure.
Kommandot ändrar inte lagrings inställningarna.

## MALLPARAMETRAR

### -AuditAction
Ange en eller flera gransknings åtgärder.
Den här parametern kan endast användas för BLOB-granskning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Ange en eller flera gransknings åtgärds grupper.
Den här parametern kan endast användas för BLOB-granskning.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditType
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på databasen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventType
Anger vilka händelse typer som ska granskas.
Den här parametern gäller endast för tabell granskning.
Du kan ange flera händelse typer.
Du kan ange alla om du vill granska alla händelse typer eller inget för att ange att inga händelser ska granskas.
Om du anger alla eller ingen samtidigt körs cmdleten inte.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Denna cmdlet genererar som standard inga utdata.

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
Anger namnet på den resurs grupp som databasen har tilldelats till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Anger antalet bevarande dagar för tabellen gransknings loggar.
Värdet noll (0) innebär att tabellen inte bevaras.
Standardvärdet är noll.
Om du anger ett värde som är större än noll måste du ange ett värde för parametern *TableIdentifer* .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Anger namnet på den server som är värd för databasen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Anger namnet på lagrings kontot för granskning av databasen.
Jokertecken är inte tillåtna.
Denna parameter är inte obligatorisk.
Om du inte anger den här parametern använder cmdleten det lagrings konto som har definierats tidigare som en del av gransknings principen för databasen.
Om det är första gången en databas gransknings princip definieras och du inte anger den här parametern Miss lyckas cmdleten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Anger vilken av lagrings åtkomst nycklar som ska användas.
De acceptabla värdena för den här parametern är:
- Första
- Sekundär standardvärdet är primärt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
Anger namnet på tabellen gransknings loggar.
Ange det här värdet om du anger ett värde som är större än noll för parametern *RetentionInDays* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. SQL. granskning. Model. AuditType

### Microsoft. Azure. commands. SQL. granskning. Model. AuditActionGroups []

### System. string []

### System. String

### System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## VÄRDEN

### Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Remove-AzureRmSqlDatabaseAuditing](./Remove-AzureRmSqlDatabaseAuditing.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)


