---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575017"
---
# Restore-AzureRmBackupItem

## Sammanfattning
Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **restore-AzureRmBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.
Denna cmdlet startar återställning från säkerhets kopierings valvet till ditt konto.

Återställnings åtgärden återställer inte den fullständiga virtuella datorn.
Den återställer diskens data och konfigurations information.
När återställningen är klar måste du skapa den virtuella datorn och starta den.

## BESKRIVS

### Exempel 1: återställa en virtuell dator till en återställnings punkt
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .
Kommandot lagrar objektet i $Container variabel.

Det tredje kommandot får säkerhets kopian i behållaren i $Container genom att använda cmdleten **Get-AzureRmBackupItem** .
Kommandot lagrar objektet i $BackupItem variabel.

Det fjärde kommandot får återställnings punkt för objektet i $BackupItem.
Kommandot lagrar objektet i $RecoveryPoint variabel.

Det sista kommandot återställer återställnings punkten i $RecoveryPoint för kontot med namnet DestinationAccount.

## MALLPARAMETRAR

### -RecoveryPoint
Anger den återställnings punkt där den virtuella datorn ska återställas.
För att få en **AzureRmBackupRecoveryPoint** , Använd cmdleten Get-AzureRmBackupRecoveryPoint.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
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

### AzureRmBackupRecoveryPoint

## VÄRDEN

### AzureRmBackupJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Säkerhets kopiering-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupRecoveryPoint](./Get-AzureRmBackupRecoveryPoint.md)


