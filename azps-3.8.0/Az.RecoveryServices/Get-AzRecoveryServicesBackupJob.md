---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088614"
---
# Get-AzRecoveryServicesBackupJob

## Sammanfattning

Hämtar säkerhets kopierings jobb.

## FRÅGESYNTAXEN

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING

Cmdleten **Get-AzRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.
Ange valv kontexten med parametern-VaultId.

## BESKRIVS

### Exempel 1: Hämta alla pågående jobb

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.
Det andra kommandot visar det första objektet i $Joblist matrisen.

### Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Det här kommandot får inte jobbet från den förra veckan i valvet.
Parametern *från* anger en tid sju dagar tidigare angiven i UTC.
Kommandot anger inte ett värde för parametern *to* .
Därför används standardvärdet för den aktuella tiden.

### Exempel 3: få ett pågående jobb och vänta tills det är färdigt

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

Det här skriptet utför det första jobbet som pågår tills jobbet är klart.

Obs! Du kan använda **wait-AzRecoveryServicesBackupJob** cmdlet för att vänta på att ett Azure Backup-jobb ska avslutas i stället för while-slingan.

## MALLPARAMETRAR

### -BackupManagementType

Anger typen av säkerhets kopierings hantering.
För närvarande stöds endast AzureVM, AzureStorage.

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

### -Från

Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.
Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.
Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .
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

### -Jobb

Anger vilket jobb som ska erhållas.

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

Anger ID för ett jobb som den här cmdleten får.
ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.

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

### -Åtgärd

Anger en åtgärd för de jobb som denna cmdlet får.
De acceptabla värdena för den här parametern är:

- Reservdomänkontrollant
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- Terställa

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

Anger en status för de jobb som denna cmdlet får.
De acceptabla värdena för den här parametern är:

- Inaktive
- Startade
- Annullerats
- Brusdämpande
- Rätta
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

### -För att

Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.
Standardvärdet är den aktuella system tiden.
Om du anger den här parametern måste du också ange parametern **-from** .
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stopp-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
