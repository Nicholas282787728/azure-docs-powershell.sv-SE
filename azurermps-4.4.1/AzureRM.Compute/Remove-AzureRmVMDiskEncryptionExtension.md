---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3fc1424fe2cde9b2137ca6925a8788fa5c8a8139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755300"
---
# Remove-AzureRmVMDiskEncryptionExtension

## Sammanfattning
Tar bort disk krypterings tillägget från en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmVMDiskEncryptionExtension** tar bort disk krypterings tillägget från en virtuell dator.
Om inget tilläggs namn anges tar denna cmdlet bort tillägget med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserade virtuella datorer.
Denna cmdlet inaktiverar inte kryptering på den virtuella datorn.
Det tar bort tillägget och den associerade tilläggs konfigurationen från den virtuella datorn.

## BESKRIVS

### Exempel 1: ta bort disk krypterings tillägget från en virtuell dator.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Det här kommandot tar bort tillägget med standard namnet AzureDiskEncryption för en virtuell dator som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för Linux-baserad virtuell dator med namnet MyTestVM.

### Exempel 2: ta bort ett disk krypterings tillägg från en virtuell dator.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Det här kommandot tar bort krypterings tillägget med namnet MyDiskEncryptionExtension från den virtuella datorn med namnet MyTestVM.

## MALLPARAMETRAR

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

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på Azure Resource Manager-resursen som representerar tillägget.
Den Set-AzureRmVMDiskEncryptionExtension cmdleten ställer in det här namnet på AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows och AzureDiskEncryptionForLinux för virtuella Linux-datorer.
Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzureRmVMDiskEncryptionExtension** eller använt ett annat resurs namn i en resurs hanterares mall.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.

Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Set-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


