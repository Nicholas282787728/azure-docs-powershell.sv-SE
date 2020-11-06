---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582067"
---
# Set-AzureRmBackupProtectionPolicy

## Sammanfattning
Ändrar en befintlig skydds princip.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### NoScheduleParamSet (standard)
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig skydds princip i Azure Backup.
Du kan ändra följande komponent komponenter: 

- Namn
- Säkerhets kopierings schema
- Bevarande principer

Alla ändringar kan påverka säkerhets kopiering och bevarande av objekt som är kopplade till principen.

## BESKRIVS

## MALLPARAMETRAR

### -BackupTime
Anger den nya säkerhets kopierings tiden som ett **datetime** -objekt för principen.
Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.
Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dagligen
Visar att säkerhets kopieringen körs på ett dagligt schema.

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Anger en matris med dagar i veckan.
Med den här principen körs säkerhets kopior på de dagar som anges i den här parametern.
De acceptabla värdena för den här parametern är:

- Dagarna 
- Torsdag 
- Onsdagen 
- Torsdag 
- Fredag 
- Afton 
- Lördag

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Anger det nya namnet för principen.
Det här namnet måste vara unikt i ett valv.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionPolicy
Anger skydds princip som denna cmdlet ändrar.
Använd Get-AzureRmBackupProtectionPolicy cmdlet för att få ett **AzureRmBackupProtectionPolicy** -objekt.

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Anger en matris med bevarande principer för säkerhets kopierings principen.
För att hämta **AzureRmBackupRetentionPolicy** -objekt, Använd cmdleten New-AzureRmBackupRetentionPolicyObject.

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vecka
Visar att säkerhets kopieringen körs på ett vecko schema.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### AzureRmBackupProtectionPolicy

## VÄRDEN

### Ingen

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


