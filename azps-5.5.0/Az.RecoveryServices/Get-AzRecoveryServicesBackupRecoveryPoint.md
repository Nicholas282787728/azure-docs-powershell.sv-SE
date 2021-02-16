---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227039"
---
# Get-AzRecoveryServicesBackupRecoveryPoint

## SYNOPSIS

Hämtar återställningspunkterna för ett säkerhetskopierat objekt.

## SYNTAX

### NoFilterParameterSet (standard)
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RecoveryPointId
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING

Cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** får återställningspunkterna för ett säkerhetskopierat Azure-säkerhetskopieringsobjekt.
När ett objekt har säkerhetskopierats har ett **AzureRmRecoveryServicesBackupRecoveryPoint-objekt** en eller flera återställningspunkter.
Ange valvkontexten med hjälp av parametern -VaultId.

## EXEMPEL

### Exempel 1: Hämta återställningspunkter från den senaste veckan för ett objekt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

Det första kommandot får valv-objekt baserat på vaultName. Det andra kommandot hämtar datumet från sju dagar sedan och lagrar det i variabeln $StartDate variabeln.
Det tredje kommandot får dagens datum och lagrar det sedan i $EndDate variabeln.
Det fjärde kommandot hämtar AzureVM-behållare för säkerhetskopiering och lagrar dem i $Container variabeln. Det femte kommandot hämtar säkerhetskopian baserat på workloadType, vaultId och lagrar det sedan i $BackupItem variabeln.
Det senaste kommandot får en matris med återställningspunkter för objektet i $BackupItem och lagrar dem sedan i $RP variabeln.

## PARAMETERS

### -DefaultProfile

Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -EndDate

Anger slutet av datumintervallet.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item

Anger det objekt som cmdleten hämtar återställningspunkter för.
Om du vill **hämta ett AzureRmRecoveryServicesBackupItem-objekt** använder du cmdleten **Get-AzRecoveryServicesBackupItem.**

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFileDownloadLocation

Anger platsen där indatafilen ska hämtas för att återställa KeyVault-nyckeln för en krypterad virtuell dator.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPointId

Anger återställningspunktens ID.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startdatum

Anger början av datumintervallet.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
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

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.ItemBase

### System.String

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.RecoveryPointBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupContainer](./Get-AzRecoveryServicesBackupContainer.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)
