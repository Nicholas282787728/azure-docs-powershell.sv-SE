---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102011"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## Sammanfattning
Hämtar ett grundläggande schema objekt.

## FRÅGESYNTAXEN

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzRecoveryServicesBackupSchedulePolicyObject** får en bas **AzureRMRecoveryServicesSchedulePolicyObject**.
Det här objektet bevaras inte i systemet.
Det är ett tillfälligt objekt som du kan ändra och använda med New-AzRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings skydds princip.

## BESKRIVS

### Exempel 1: Ange schema frekvensen till varje vecka
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.
Det andra kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.
Det tredje kommandot ändrar frekvensen för schemaläggnings principen till varje vecka.
Med det senaste kommandot skapas en säkerhets kopierings skydds princip med det uppdaterade schemat.

### Exempel 2: Ange tid för säkerhets kopiering
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Det första kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.
Det andra kommandot tar bort alla schemalagda körnings tider från $SchPol.
Det tredje kommandot får dagens datum och tid och lagrar det sedan i $DT variabel.
Det fjärde kommandot ersätter de schemalagda kör tiderna med den aktuella tiden.
Du kan bara säkerhetskopiera AzureVM en gång per dag, så för att återställa säkerhets kopierings tiden måste du ersätta det ursprungliga schemat.
Med det senaste kommandot skapas en säkerhets kopierings princip med det nya schemat.

## MALLPARAMETRAR

### -BackupManagementType
Den klass med resurser som skyddas. De acceptabla värdena för den här parametern är:
- AzureVM 
- AzureStorage
- AzureWorkload

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
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

### -WorkloadType
Arbets belastnings typ för resursen. De acceptabla värdena för den här parametern är:
- AzureVM 
- AzureFiles
- MSSQL


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


