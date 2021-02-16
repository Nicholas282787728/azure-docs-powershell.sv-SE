---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227006"
---
# Get-AzRecoveryServicesVault

## SYNOPSIS

Hämtar en lista över Recovery Services-valv.

## SYNTAX

### ByTagNameValueParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING

Cmdleten **Get-AzRecoveryServicesVault** får en lista med Recovery Services-valv i den aktuella prenumerationen.

## EXEMPEL

### Exempel 1

```
PS C:\> Get-AzRecoveryServicesVault
```

Hämta listan med valv i vald prenumeration.

### Exempel 2

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

Hämta listan med valv i resursgrupp i vald prenumeration.

### Exempel 3

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

Den första cmdleten får valvet i resursgruppen med ett visst namn. Sedan kommer vi åt MSI-informationen från valvet.

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

### -Name

Anger namnet på valvet som frågan ska söka efter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName

Anger namnet på den Azure-resursgrupp som det angivna Recovery Services-objektet ska hämtas från.

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

### -Tag

Anger vilka taggar som ska sökas efter

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagName

Anger nyckeln för taggen som ska sökas efter

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue

Anger värdet för taggen som ska sökas efter

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## ANTECKNINGAR
Get-AzRecoveryServicesVault den gamla versionen av Az.RecoveryServices(<=2.10.0) fungerar inte med Az.Accounts(>=1.8.1) på grund av felaktig sammansättningsreferens. Modulen Az.RecoveryServices måste uppgraderas till 2.11.0 eller nyare om du använder de senaste az- eller az.kontona.

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesVaultSettingsFile](./Get-AzRecoveryServicesVaultSettingsFile.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)
