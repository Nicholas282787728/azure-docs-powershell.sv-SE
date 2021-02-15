---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238958"
---
# Add-AzVmssSecret

## SYNOPSIS
Gör en VMSS hemligt.

## SYNTAX

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzVmssSecret** lägger till en hemligt namn i VMSS (Virtual Machine Scale Set).
Hemligheten måste lagras i ett Azure-nyckelvalv.
Mer information om nyckelvalv finns i Vad [är Azure-nyckelvalv?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Mer information om cmdlets finns i [Azure-cmdlets](/powershell/module/az.keyvault) för nyckelvalv eller [Set-AzKeyVaultSecret-cmdleten.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## EXEMPEL

### Exempel 1: Lägg till en hemligt i VMSS
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

I det här exemplet läggs en hemlig information till VMSS.
Det första kommandot använder cmdleten Get-AzKeyVault för att få ett valv hemligt från valvet ContosoVault och lagrar resultatet i variabeln $Vault.
Det andra kommandot använder cmdleten **New-AzVmssVaultCertificateConfig** för att skapa en konfiguration av ett nyckelvalv-certifikat med den angivna certifikat-URL:en från certifikatarkivet med namnet Certifikat och lagrar resultaten i variabeln $CertConfig.
Det tredje kommandot använder cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och lagrar resultatet för variabeln $VMSS.
Det fjärde kommandot lägger till en hemligt i VMSS med valvhemligheten med hjälp av nyckelresurs-ID:t och valvcertifikatet som lagras i $Vault och $CertConfig variabler.

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

### -SourceVaultId
Anger resurs-ID för nyckelvalvet som innehåller certifikaten som du kan lägga till i den virtuella datorn.
Det här värdet är också nyckeln till att lägga till flera certifikat.
Det innebär att du kan använda samma värde för *SourceVaultId-parametern* när du lägger till flera certifikat från samma nyckelvalv.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultCertificate
Anger det **valv-certifikatobjekt** som innehåller certifikat-URL:en och certifikatnamnet.
Du kan skapa objektet med cmdleten [New-AzVmssVaultCertificateConfig.](./New-AzVmssVaultCertificateConfig.md)

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger VMSS-objektet.
Du kan skapa det här objektet med cmdleten [New-AzVmssConfig.](./New-AzVmssConfig.md)

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### Microsoft.Azure.Management.Compute.Models.VaultCertificate[]

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)
