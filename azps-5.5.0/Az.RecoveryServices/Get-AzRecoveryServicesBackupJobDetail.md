---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 6c12cccff6305c96bf2df037e32b8af35170454a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227054"
---
# Get-AzRecoveryServicesBackupJobDetail

## SYNOPSIS

Hämtar information för ett säkerhetskopieringsjobb.

## SYNTAX

### JobFilterSet (standard)
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdFilterSet
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING

Cmdleten **Get-AzRecoveryServicesBackupTailDetail** hämtar jobbinformation för Azure Backup för ett visst jobb.
Ange valvkontexten med hjälp av parametern -VaultId.

Varning! **Aliaset Get-AzRecoveryServicesBackupTailDetails** tas bort i en kommande version av brytningsändringen.

## EXEMPEL

### Exempel 1: Hämta jobbinformation för säkerhetskopiering för misslyckade jobb

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

Det första kommandot hämtar relevant valv. Det andra kommandot får en matris med misslyckade jobb i valvet och lagrar dem sedan $Jobs matrisen.
Det tredje kommandot hämtar jobbinformation för det första misslyckade jobbet i $Jobs och lagrar dem sedan i $JobDetails variabeln.
Det sista kommandot visar felinformation för de misslyckade jobben.

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

Anger vilket jobb som ska fås.
Om du vill **hämta ett BackupPost-objekt** använder du cmdleten **Get-AzRecoveryServicesBackup Den här** cmdleten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Anger ID för ett säkerhetskopieringsjobb.
ID:t är egenskapen JobId för ett **microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase-objekt.**

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
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

### System.String

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.JobBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupLow](./Get-AzRecoveryServicesBackupJob.md)
