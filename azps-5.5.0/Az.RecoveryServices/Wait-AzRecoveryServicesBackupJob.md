---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217886"
---
# Wait-AzRecoveryServicesBackupJob

## SYNOPSIS

Väntar på att säkerhetskopieringsjobbet ska slutföras.

## SYNTAX

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING

Cmdleten **Wait-AzRecoveryServicesBackup En** cmdlet väntar på att ett Azure-säkerhetskopieringsjobb ska slutföras.
Säkerhetskopieringsjobb kan ta lång tid.
Om du kör ett säkerhetskopieringsjobb som en del av ett skript kanske du vill tvinga skriptet att vänta på att jobbet slutförs innan det fortsätter till andra aktiviteter.
Ett skript som innehåller den här cmdleten kan vara enklare än ett som avsöker säkerhetskopieringstjänsten efter jobbstatus.
Ange valvkontexten med hjälp av parametern -VaultId.

## EXEMPEL

### Exempel 1: Vänta tills ett jobb är klart

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

Med det här skriptet avsöks det första jobbet som pågår tills jobbet har slutförts eller timeout-perioden på 1 timme har gått ut.

## PARAMETERS

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

### -Job

Anger jobbet som ska vänta på.
Om du vill **hämta ett BackupPost-objekt** använder du cmdleten **Get-AzRecoveryServicesBackup Den här** cmdleten.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout

Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska slutföras.
Vi rekommenderar att ange ett time out-värde.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### System.Object

### System.String

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupLow](./Get-AzRecoveryServicesBackupJob.md)
