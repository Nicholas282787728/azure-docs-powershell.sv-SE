---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399829"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS
Får säkerhetskopieringsjobb.

## SYNTAX

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzRecoveryServicesBackup En** cmdlet får Azure Backup-jobb för ett visst valv.
Ange valvkontexten med hjälp Set-AzRecoveryServicesVaultContext cmdleten innan du använder den aktuella cmdleten.

## EXEMPEL

### Exempel 1: Hämta alla pågående jobb
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Det första kommandot får statusen för ett pågående jobb som en matris och lagrar den sedan $Joblist variabeln.
Det andra kommandot visar det första objektet i $Joblist matrisen.

### Exempel 2: Få alla misslyckade jobb under de senaste 7 dagarna
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Det här kommandot får misslyckade jobb från den senaste veckan i valvet.
*Parametern* Från anger en tid sju dagar tidigare angivet i UTC.
Kommandot anger inte något värde för *parametern Till.*
Därför används standardvärdet för den aktuella tiden.

### Exempel 3: Hämta ett pågående jobb och vänta tills det är klart
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Med det här skriptet avsöks det första jobbet som pågår tills jobbet har slutförts.

## PARAMETERS

### -BackupManagementType
Anger typen för hantering av säkerhetskopiering.
För närvarande stöds endast AzureVM och AzureStorage.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
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

### -Från
Anger starten, som ett **DateTime-objekt,** för ett tidsperiodintervall för de jobb som den här cmdleten hämtar.
Om du vill **hämta ett DateTime-objekt** använder Get-Date-cmdleten.
Om du vill ha mer information **om DateTime-objekt** skriver du `Get-Help Get-Date` .
Använd UTC-format för datum.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Anger namnet på det säkerhetskopieringsjobb som ska fås.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Anger ID för ett jobb som cmdleten hämtar.
ID:t är egenskapen InstanceId för ett **AzureRmRecoveryServicesBackup Ett Objekt.**
Om du vill **hämta ett AzureRmRecoveryServicesBackupPost-objekt** använder du Get-AzRecoveryServicesBackupService.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operation
Anger en åtgärd för de jobb som den här cmdleten hämtar.
De godtagbara värdena för den här parametern är:
- Säkerhetskopiering
- ConfigureBackup
- DeleteBackupData
- Registrera dig
- Återställ
- Ta bort skydd
- Avregistrera

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Anger en status för de jobb som den här cmdleten hämtar.
De godtagbara värdena för den här parametern är:
- InProgress
- Misslyckades
- Annullerad
- Avbryta
- Slutförd
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Anger slutet, som ett **DateTime-objekt,** för ett tidsperiodintervall för de jobb som den här cmdleten hämtar.
Standardvärdet är den aktuella systemtiden.
Om du anger den här parametern måste du också ange *från-parametern.*
Använd UTC-format för datum.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM ID för Recovery Services Vault.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase

## ANTECKNINGAR

## RELATERADE LÄNKAR


[Stop-AzRecoveryServicesBackupLow](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackup Eni](./Wait-AzRecoveryServicesBackupJob.md)


