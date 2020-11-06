---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1a9eb2ef731e7ce555fbac1a08cd8468de83ebc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582559"
---
# New-AzureRmRecoveryServicesBackupProtectionPolicy

## Sammanfattning
Skapar en säkerhets kopierings princip.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmRecoveryServicesBackupProtectionPolicy** skapar en säkerhets kopierings skydds princip i ett valv.
En skydds princip är kopplad till minst en bevarande princip.
Bevarande principen definierar hur länge en återställnings punkt behålls med Azure Backup.
Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta standard princip för bevarande.
Och du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta standard schemaläggnings principen.
**SchedulePolicy** -och **RetentionPolicy** -objekten används som indata för den **nya-AzureRmRecoveryServicesBackupProtectionPolicy-** cmdleten.
Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.

## BESKRIVS

### Exempel 1: skapa en säkerhets kopierings princip
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Det första kommandot får en grundläggande **SchedulePolicyObject** och lagrar det sedan i $SchPol variabel.
Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.
I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid.
Det fjärde kommandot lägger till dagens datum och aktuellt klock slag i $Dt som den schemalagda körnings tiden till schemaläggnings principen.
Det femte kommandot får ett bas **RetentionPolicy** -objekt och lagrar det sedan i $RetPol variabel.
Det sjätte kommandot ställer in policyn för bevarande av tids perioden till 365 dagar.
Med kommandot slut skapas ett **BackupProtectionPolicy** -objekt baserat på schema-och bevarande principer som skapas av föregående kommandon.

## MALLPARAMETRAR

### -BackupManagementType
Anger typen av säkerhets kopierings hantering.
De acceptabla värdena för den här parametern är:
- AzureVM 
- AzureSQLDatabase

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Namn
Anger namnet på policyn.

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
Anger bas **RetentionPolicy** -objektet.
Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta ett **RetentionPolicy** -objekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
Anger bas **SchedulePolicy** -objektet.
Du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta ett **SchedulePolicy** -objekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultId
ARM-ID för Recovery Services-valvet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkloadType
Anger arbets belastnings typen.
De acceptabla värdena för den här parametern är:
- AzureVM 
- AzureSQLDatabase

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. WorkloadType

### System. Nullable ' 1 [[Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. Models. BackupManagementType, Microsoft. Azure. kommandon. RecoveryServices. backup. Models, version = 4.3.1.0, Culture = neutralt, PublicKeyToken = null]]

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase

### System. String
Parametrar: VaultId (ByValue)

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Enable-AzureRmRecoveryServicesBackupProtection](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzureRmRecoveryServicesBackupSchedulePolicyObject](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


