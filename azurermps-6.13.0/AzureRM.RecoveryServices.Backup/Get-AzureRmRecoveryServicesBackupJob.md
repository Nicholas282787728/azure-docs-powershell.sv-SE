---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582564"
---
# Get-AzureRmRecoveryServicesBackupJob

## Sammanfattning
Hämtar säkerhets kopierings jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.
Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.

## BESKRIVS

### Exempel 1: Hämta alla pågående jobb
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.
Det andra kommandot visar det första objektet i $Joblist matrisen.

### Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Det här kommandot får inte jobbet från den förra veckan i valvet.
Parametern *från* anger en tid sju dagar tidigare angiven i UTC.
Kommandot anger inte ett värde för parametern *to* .
Därför används standardvärdet för den aktuella tiden.

### Exempel 3: få ett pågående jobb och vänta tills det är färdigt
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Det här skriptet utför det första jobbet som pågår tills jobbet är klart.

## MALLPARAMETRAR

### -BackupManagementType
Anger typen av säkerhets kopierings hantering.
För närvarande stöds endast AzureVM, AzureStorage.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

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

### -Från
Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.
Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.
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
Anger namnet på det säkerhets kopierings jobb som ska visas.

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
ID är InstanceId-egenskapen för ett **AzureRmRecoveryServicesBackupJob** -objekt.
För att få ett **AzureRmRecoveryServicesBackupJob** -objekt, Använd Get-AzureRmRecoveryServicesBackupJob.

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
- Registrera dig
- Terställa
- Låsa upp
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
Om du anger den här parametern måste du också ange parametern *från* .
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String
Parametrar: VaultId (ByValue)

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmRecoveryServicesBackupJobDetails](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[Stopp-AzureRmRecoveryServicesBackupJob](./Stop-AzureRmRecoveryServicesBackupJob.md)

[Wait-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


