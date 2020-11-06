---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584576"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## Sammanfattning
Ändrar en säkerhets kopierings princip.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig Azure Backup-säkerhetsprincip.
Du kan ändra schema för säkerhets kopiering och bevarande princip.

De ändringar du gör påverkar säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.

Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.

## BESKRIVS

### Exempel 1: ändra en säkerhets kopierings princip
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

Det första kommandot får ett bas objekt i SchedulePolicy och lagrar det sedan i $SchPol variabel.

Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.

I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid och sedan lagras de i $DT variabel.

Det fjärde kommandot lägger till datum och tid i $DT till tids schema principen.

Det femte kommandot får ett grundläggande bevarande princip objekt och lagrar det sedan i $RetPol variabel.

Med sjätte kommandot anges varaktigheten till 365 dagar.

Det sjunde kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.

Det slutliga kommandot ändrar säkerhets kopierings princip för $Pol genom att använda en schema princip i $SchPol och bevarande principen i $RetPol.

## MALLPARAMETRAR

### -Princip
Anger säkerhets kopierings principen som denna cmdlet ändrar.
För att hämta ett **BackupProtectionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupProtectionPolicy.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Anger grundläggande bevarande princip.
För att hämta ett **RetentionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Anger det grundläggande schemaobjektet.
Du kan hämta ett **SchedulePolicy** -objekt med Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-objektet.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### PolicyBase
Parametern ' policy ' godkänner värdet av typen ' PolicyBase ' från pipeline

## VÄRDEN

### System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. JobBase]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[New-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


