---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584575"
---
# Restore-AzureRmRecoveryServicesBackupItem

## Sammanfattning
Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **restore-AzureRmRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.
Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.

Återställnings åtgärden återställer inte den fullständiga virtuella datorn.
Den återställer diskens data och konfigurations information.
När återställningen är klar måste du skapa den virtuella datorn och starta den.

Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.

## BESKRIVS

### Exempel 1: Återställ ett objekt till en återställnings punkt
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.

Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.

Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.

Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.

Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.
Det angivna datum intervallet är de senaste sju dagarna.

Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.

## MALLPARAMETRAR

### -RecoveryPoint
Anger den återställnings punkt där den virtuella datorn ska återställas.
Använd Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet för att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Anger namnet på mål lagrings kontot i prenumerationen.
Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.

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

### -StorageAccountResourceGroupName
Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.
Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### RecoveryPointBase
Parametern ' RecoveryPoint ' godkänner värdet av typen ' RecoveryPointBase ' från pipeline

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Säkerhets kopiering-AzureRmRecoveryServicesBackupItem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


