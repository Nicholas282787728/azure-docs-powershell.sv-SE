---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576025"
---
# Start-AzureRmSqlServerUpgrade

## Sammanfattning
Startar uppgraderingen av en SQL Database-Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureRmSqlServerUpgrade** startar uppgraderingen av en Azure SQL Database Server version 11 till version 12.
Du kan övervaka förloppet för en uppgradering med hjälp av Get-AzureRmSqlServerUpgrade cmdlet.

## BESKRIVS

### Exempel 1: uppgradera en server
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Det här kommandot uppgraderar den server som heter Server01 tilldelad till resurs gruppen TesourceGroup01.

### Exempel 2: uppgradera en server med hjälp av schema tid och databas rekommendation
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Det första kommandot skapar en tid om fem minuter i framtiden med hjälp av Get-Date cmdlet.
Kommandot lagrar datumet i variabeln $ScheduleTime.
Om du vill ha mer information skriver du `Get-Help Get-Date` .
Det andra kommandot skapar ett **RecommendedDatabaseProperties** -objekt och lagrar sedan objektet i variabeln $DatabaseMap.
Nästa tre kommandon tilldelar värden till egenskaper för det objekt som lagras i $DatabaseMap.
Det sista kommandot uppgraderar den befintliga servern som heter Server01 till version 12,0.
Den tidigaste tiden för uppgraderingen är fem minuter efter att du har kört kommandot enligt $ScheduleTime variabel.
Efter uppgraderingen kör databas ContosoDB standard versionen och har tjänst nivå mål S0.

## MALLPARAMETRAR

### -DatabaseCollection
Anger en matris med **RecommendedDatabaseProperties** -objekt som denna cmdlet använder för Server uppgraderingen.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ElasticPoolCollection
Anger en matris med **UpgradeRecommendedElasticPoolProperties** -objekt som ska användas för Server uppgraderingen.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som servern är tilldelad till.

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

### -ScheduleUpgradeAfterUtcDateTime
Anger den tidigaste tiden, som ett **datetime** -objekt, för att uppgradera servern.
Ange ett värde i ISO8601-format i UTC (Coordinated Universal Time).
Om du vill ha mer information skriver du `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Anger namnet på den server som cmdleten uppgraderar.

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

### -ServerVersion
Anger den version som denna cmdlet uppgraderar till servern.
Det enda giltiga värdet är 12,0.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Stopp-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)


