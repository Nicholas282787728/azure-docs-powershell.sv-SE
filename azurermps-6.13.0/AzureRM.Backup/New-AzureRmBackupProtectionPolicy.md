---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574039"
---
# New-AzureRmBackupProtectionPolicy

## Sammanfattning
Skapar en säkerhets kopierings princip.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### NoScheduleParamSet (standard)
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmBackupProtectionPolicy** skapar en Azure Backup-princip som ett Azure PowerShell-objekt.
En säkerhets kopierings princip anger när och hur ofta säkerhets kopieringen ska säkerhetskopiera ett objekt.
I Enable-AzureRmBackupProtection cmdlet används en säkerhets kopierings princip.

## BESKRIVS

### Exempel 1: skapa en daglig säkerhets kopierings princip med daglig och månads vis bevarande
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.
Kommandot lagrar objektet i $Vault variabel.
Med det andra kommandot skapas en bevarande princip för 30 dagar efter varje dag och sparas sedan i $Daily variabel.
Det tredje kommandot skapar en bevarande princip som behåller säkerhets kopian på den tionde och tjugonde dagen i varje månad under tolv månader.
Kommandot lagrar bevarande principen i $Monthly variabel.
Med kommandot slut skapas en säkerhets kopierings princip för valvet i $Vault som har en daglig säkerhets kopia av 3:00 PM.
Kommandot tilldelar de bevarande principer som lagras i $Daily och $Monthly.
Resultatet sparas i $ProtectionPolicy variabel.

## MALLPARAMETRAR

### -BackupTime
Anger klock slaget som ett **datetime** -objekt för säkerhets kopieringen.
För att få ett **datum/tid** -värde, Använd cmdleten Get-Date.
Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Dagligen
Visar att säkerhets kopieringen körs på ett dagligt schema.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
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
- Söndag om du anger en *vecko* parameter anger du den här parametern.

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
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

### -Namn
Anger ett namn för säkerhets kopierings principen.
Välj ett namn som är unikt i valvet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Anger en matris med bevarande principer för säkerhets kopierings principen.
För att få en **AzureRmBackupRetentionPolicy** , Använd cmdleten New-AzureRmBackupRetentionPolicyObject.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Skriv
Anger den typ av säkerhets kopia som policyn gäller.
För närvarande är det enda värdet som stöds AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valv
Anger det Azure Backup-valv som säkerhets kopierings principen tillhör.
Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Vecka
Anger att säkerhets kopierings principen utlöstes varje vecka en eller flera dagar i veckan.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. DateTime

### System. string []

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupRetentionPolicy []

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault
Parametrar: valv (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupProtectionPolicy

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Set-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


