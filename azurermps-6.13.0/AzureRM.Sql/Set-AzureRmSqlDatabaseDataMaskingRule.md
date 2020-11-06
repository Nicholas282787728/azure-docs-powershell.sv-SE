---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 4e5f2578d0e9dbb2139b330ec0a7c2fe81b3124e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574765"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## Sammanfattning
Anger egenskaper för en data masknings regel för en databas.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmSqlDatabaseDataMaskingRule** anger en regel för data maskering för en Azure SQL-databas.
Använd cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* , *databasename* och *RuleID* för att identifiera regeln.
Du kan ange parametrar för *SchemaName* , *TableName* och *columnName* för att omreglera regeln.
Ange parametern *MaskingFunction* om du vill ändra hur data maskeras.
Om du anger ett värde för tal eller text för *MaskingFunction* kan du ange *NumberFrom* -och *NumberTo* -parametrar för maskering av mask eller *PrefixSize* , *ReplacementString* och *SuffixSize* för text maskning.
Om kommandot lyckas, och om du anger parametern *Passthru* , returnerar cmdleten ett objekt som beskriver regel egenskaperna för data maskering och regel-ID.
Regel-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** , **databasename** och **RuleID**.
Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.

## BESKRIVS

### Exempel 1: ändra området för en regel för data maskering i en databas
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Det här kommandot ändrar en regel för data maskering med ID-Rule17.
Den regeln körs i databasen som heter Database01 på Server Server01.
Det här kommandot ändrar gränserna för det intervall som ett slumptal skapas i.
Det nya området är mellan 23 och 42.

## MALLPARAMETRAR

### -ColumnName
Anger namnet på den kolumn som är avsedd för Maskerings regeln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -MaskingFunction
Anger den Maskerings funktion som används i regeln.
De acceptabla värdena för den här parametern är:
- Vis
- Nomaskering
- Textrad
- Numeriska
- SocialSecurityNumber
- CreditCardNumber
- E-post standardvärdet är standard.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Anger det nedre gräns numret för intervallet som ett slumpmässigt värde är markerat för.
Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .
Standardvärdet är 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Anger det övre gräns numret för intervallet som ett slumpmässigt värde är markerat.
Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .
Standardvärdet är 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

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

### -PrefixSize
Anger antalet tecken i början av den text som inte är maskerad.
Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .
Standardvärdet är 0.

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

### -ReplacementString
Anger antalet tecken i slutet av texten som inte maskeras.
Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .
Standardvärdet är 0.

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

### -SchemaName
Anger namnet på ett schema.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -SuffixSize
Anger antalet tecken i slutet av texten som inte maskeras.
Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .
Standardvärdet är 0.

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

### -TableName
Anger namnet på den databas tabell som innehåller den maskerade kolumnen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### System. String

### System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Nullable ' 1 [[system. Double, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## VÄRDEN

### Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[New-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)


