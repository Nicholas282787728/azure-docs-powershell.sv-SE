---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575019"
---
# New-AzureRmBackupRetentionPolicyObject

## Sammanfattning
Skapar en bevarande princip för säkerhets kopior.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmBackupRetentionPolicyObject** skapar en lagrings princip för Azure Backup.
En bevarande princip definierar hur länge säkerhets kopian behåller en återställnings punkt.
Följande typer av bevarande är: 

- Vardag 
- Vecko 
- Månaders 
- Års 

Skapa en bevarande princip för varje typ av bevarande som du planerar att använda.

En säkerhets kopierings princip är kopplad till minst en bevarande princip.
Använd New-AzureRmBackupProtectionPolicy cmdlet för att skapa en säkerhets kopierings princip.
Du kan istället ange en bevarande princip för Enable-AzureRmBackupProtection cmdlet.

## BESKRIVS

### Exempel 1: skapa en bevarande princip för daglig bevarande
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

Det första kommandot skapar en bevarande princip för 30 dagar efter varje dag och lagrar sedan den i $Daily variabel.

Det andra kommandot visar innehållet i $Daily.

### Exempel 2: skapa en bevarande princip per månad
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

Det första kommandot skapar en bevarande princip som behåller den tionde och tjugonde varje månad under tolv månader.
Kommandot lagrar bevarande principen i $Monthly variabel.

Det andra kommandot visar innehållet i $Monthly.

## MALLPARAMETRAR

### -DailyRetention
Anger att den här cmdleten skapar en daglig bevarande princip.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfMonth
Anger vilka dagar i månaden som identifierar vilka återställnings punkter som säkerhets kopior finns kvar och hur länge.
De acceptabla värdena för den här parametern är: heltal mellan 1 och 28 och sist.
Ange den här parametern om du anger parametrarna *DailyRetention* , *MonthlyRetentionInDailyFormat* och *YearlyRetentionInDailyFormat* .

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Anger en matris med dagar i veckan.
De dagar som denna cmdlet anger för att identifiera vilka återställnings punkter som säkerhets kopian sparas och hur länge.
De acceptabla värdena för den här parametern är:

- Dagarna 
- Torsdag 
- Onsdagen 
- Torsdag 
- Fredag 
- Afton 
- Lördag

Ange den här parametern om du anger parametrarna *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* och *YearlyRetentionInWeeklyFormat* .

Se till att de vecko dagar du väljer för säkerhets kopiering och kvarhållande är justerade.
Till exempel, om din säkerhets kopia är inställd för lördagar, måste bevarande principer också använda lördag.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInDailyFormat
Anger att den här cmdleten skapar en månatlig princip i önskat format.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Anger att denna cmdlet skapar en månatlig princip i vecko format.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Anger vilka månader som har återställnings punkter som säkerhets kopian kvarhåller.
De acceptabla värdena för den här parametern är: namn på månader, till exempel januari och februari.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bevarande
Anger den bevarande period, i dagar, månader eller år, för vilken säkerhets kopian lagrar en säkerhets kopie rad.
Enheten beror på om den här cmdleten väljer ett alternativ för daglig, månatlig eller årlig bevarande.
Om du till exempel anger parametern *DailyRetention* , tolkar cmdleten den aktuella parametern som ett antal dagar.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklyRetention
Anger att denna cmdlet skapar en bevarande princip för varje vecka.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekNumber
Anger veckorna för den månad som visar vilka återställnings punkter som säkerhets kopior kvarstår och hur länge.
De acceptabla värdena för den här parametern är:

- Skapas 
- Igen 
- Utanför 
- Sång 
- Senast

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Anger att den här cmdleten skapar en årlig bevarande princip i varje dagligt format.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Anger att den här cmdleten skapar en årlig bevarande princip i varje vecka.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### AzureRmBackupRetentionPolicy

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


