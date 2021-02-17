---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223398"
---
# Get-AzRecoveryServicesBackupManagementServer

## SYNOPSIS
Får SCDPM- och Azure Backup Management-servrar.

## SYNTAX

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzRecoveryServicesBackupManagementServer** får en lista med servrar för säkerhetskopieringshantering som är registrerade i ett valv.
Det finns två typer av servrar för säkerhetskopieringshantering: System Center Data Protection Manager (SCDPM) och Azure Backup Management-servrar.
Servrar för säkerhetskopieringshantering installeras separat för att hantera säkerhetskopiering.
Ange valvkontexten med hjälp Set-AzRecoveryServicesVaultContext cmdleten innan du använder den aktuella cmdleten.

## EXEMPEL

### Exempel 1: Hämta alla servrar för säkerhetskopieringshantering
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

Med det här kommandot registreras alla servrar för säkerhetskopieringshantering med valvet.

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

### -Name
Anger namnet på den server för säkerhetskopieringshantering som ska fås.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### Microsoft.Azure.Commands.RecoveryServices.Backup.cmdlets.Models.BackupEngineBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Unregister-AzRecoveryServicesBackupManagementServer](./Unregister-AzRecoveryServicesBackupManagementServer.md)


