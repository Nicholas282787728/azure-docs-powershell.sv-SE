---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227023"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
Hämtar ett principobjekt för basschemat.

## SYNTAX

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzRecoveryServicesBackupSchedulePolicyObject** får en bas **för AzureRMRecoveryServicesSchedulePolicyObject.**
Det här objektet finns inte kvar i systemet.
Det är ett tillfälligt objekt som du kan ändra och använda med cmdleten New-AzRecoveryServicesBackupProtectionPolicy för att skapa en ny princip för säkerhetskopieringsskydd.

## EXEMPEL

### Exempel 1: Ställ in schemafrekvensen till varje vecka
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Det första kommandot hämtar bevarandeprincipobjektet och lagrar det sedan i $RetPol variabeln.
Det andra kommandot hämtar schemaprincipobjektet och lagrar det sedan i $SchPol variabeln.
Det tredje kommandot ändrar frekvensen för schemaprincipen till varje vecka.
Det senaste kommandot skapar en princip för säkerhetskopieringsskydd med det uppdaterade schemat.

### Exempel 2: Ange säkerhetskopieringstiden
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Det första kommandot hämtar schemaprincipobjektet och lagrar det sedan i $SchPol variabeln.
Med det andra kommandot tas alla schemalagda körningstider bort från $SchPol.
Det tredje kommandot hämtar dagens datum och aktuell tid och lagrar det sedan i $DT variabeln.
Det fjärde kommandot ersätter de schemalagda körningarna med den aktuella tiden.
Du kan bara säkerhetskopiera AzureVM en gång per dag, så om du vill återställa säkerhetskopieringstiden måste du ersätta det ursprungliga schemat.
Med det senaste kommandot skapas en princip för säkerhetskopieringsskydd med det nya schemat.

## PARAMETERS

### -BackupManagementType
Den resursklass som skyddas. De godtagbara värdena för den här parametern är:
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
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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
Typ av arbetsbelastning för resursen. De godtagbara värdena för den här parametern är:
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.SchedulePolicyBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


