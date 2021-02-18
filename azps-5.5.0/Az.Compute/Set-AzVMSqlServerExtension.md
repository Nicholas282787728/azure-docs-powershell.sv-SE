---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231031"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Anger Azure SQL Server-tillägget på en virtuell dator.

## SYNTAX

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Set-AzVMSqlServerExtension-cmdleten** anger AzureSQL Server-tillägget på en virtuell dator.

## EXEMPEL

### Exempel 1: Ange inställningar för automatisk korrigering på en virtuell dator
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Det första kommandot skapar ett konfigurationsobjekt med cmdleten **New-AzVMSqlServerAutoPatchingConfig.**
Kommandot lagrar konfigurationen i den $AutoPatchingConfig variabeln.
Det andra kommandot hämtar den virtuella datorn med namnet VirtualMa machinee11 på tjänsten Service02 med hjälp av Get-AzVM-cmdleten.
Kommandot skickar objektet till den aktuella cmdleten med hjälp av rörledningsoperatorn.
Den aktuella cmdleten anger inställningarna för automatisk korrigering i $AutoPatchingConfig för den virtuella datorn.
Kommandot skickar den virtuella datorn till Update-AzVM cmdlet.

### Exempel 2: Ange inställningar för automatisk säkerhetskopiering på en virtuell dator
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Det första kommandot skapar ett konfigurationsobjekt med cmdleten **New-AzVMSqlServerAutoBackupConfig.**
Kommandot lagrar konfigurationen i den $AutoBackupConfig variabeln.
Det andra kommandot hämtar den virtuella datorn med namnet VirtualMa machinee11 på tjänsten Service02 och skickar den sedan till den aktuella cmdleten.
Den aktuella cmdleten anger inställningarna för automatisk säkerhetskopiering $AutoBackupConfig den virtuella datorn.
Kommandot skickar den virtuella datorn till Update-AzVM cmdlet.

### Exempel 3: Inaktivera ett SQL Server-tillägg på en virtuell dator
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Det här kommandot får en virtuell dator med namnet VirtualMa machinee08 på Service03 och skickar det sedan till den aktuella cmdleten.
Kommandot inaktiverar tillägget för virtuell SQL Server-dator på den virtuella datorn.

### Exempel 4: Avinstallera ett SQL Server-tillägg på en viss virtuell dator
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Det här kommandot får en virtuell dator med namnet VirtualMa machinee08 på Service03 och skickar det sedan till den aktuella cmdleten.
Kommandot avinstallerar ett tillägg för virtuell SQL Server-dator på den virtuella datorn.

## PARAMETERS

### -AutoBackupSettings
Anger de automatiska inställningarna för säkerhetskopiering av SQL Server.
Om du vill **skapa ett AutoBackupSettings-objekt** använder du New-AzVMSqlServerAutoBackupConfig cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Anger de automatiska inställningarna för SQL Server-korrigeringar.
Om du vill **skapa ett AutoPatchingSettings-objekt** använder du New-AzVMSqlServerAutoPatchingConfig cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger platsen för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på SQL Server-tillägget.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Anger versionen av SQL Server-tillägget.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på den virtuella datorn där den här cmdleten anger SQL Server-tillägget.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

### Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


