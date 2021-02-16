---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217990"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS

Får säkerhetskopieringsjobb.

## SYNTAX

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING

Cmdleten **Get-AzRecoveryServicesBackup En cmdlet** får Azure Backup-jobb för ett visst valv.
Ange valvkontexten med hjälp av parametern -VaultId.

## EXEMPEL

### Exempel 1: Få alla pågående jobb

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Det första kommandot får statusen för ett pågående jobb som en matris och lagrar den sedan $Joblist variabeln.
Det andra kommandot visar det första objektet i $Joblist matrisen.

### Exempel 2: Få alla misslyckade jobb under de senaste 7 dagarna

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Det här kommandot får misslyckade jobb från den senaste veckan i valvet.
*Parametern* Från anger en tid sju dagar tidigare angivet i UTC.
Kommandot anger inte något värde för *parametern Till.*
Därför används standardvärdet för den aktuella tiden.

### Exempel 3: Hämta ett pågående jobb och vänta tills det är klart

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Med det här skriptet avsöks det första jobbet som pågår tills jobbet har slutförts.

Obs! Du kan använda **cmdleten Wait-AzRecoveryServicesBackup Enlsson** till att vänta på att ett Azure Backup-jobb slutförs i stället för att loopa.

### Exempel 4: Få alla AzureVM-jobb de senaste två dagarna som slutförts utan fel

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Första cmdleten hämtar valvobjektet. Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs. Ändra värdet för parametern BackupManagementType till MAB för att hämta MAB-agentjobb.

## PARAMETERS

### -BackupManagementType

Den resursklass som skyddas. De värden som stöds för den här cmdleten är för närvarande AzureVM, AzureStorage, AzureWorkload, MAB.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

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
Om du vill **hämta ett DateTime-objekt** använder du cmdleten **Get-Date.**
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

Anger vilket jobb som ska fås.

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
ID:t är egenskapen JobId för ett **microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase-objekt.**

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
- DisableBackup
- Återställ
- BackupDataMove

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

Anger en status för de jobb som cmdleten hämtar.
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
Om du anger den här parametern måste du också ange **parametern -From.**
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupTailDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupLow](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackup Eni](./Wait-AzRecoveryServicesBackupJob.md)
