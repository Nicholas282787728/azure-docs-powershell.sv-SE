---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577258"
---
# Disable-AzureRmVMDiskEncryption

## Sammanfattning
Inaktiverar kryptering på en IaaS virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **disable-AzureRmVMDiskEncryption** inaktiverar kryptering på infrastrukturen som en tjänst (IaaS) virtuell dator.
Denna cmdlet stöds endast på virtuella Windows-datorer och inte virtuella Linux-datorer.
Denna cmdlet installerar ett tillägg på den virtuella datorn för att inaktivera kryptering.
Om parametern *Name* inte anges skapas ett tillägg med standard namnet "AzureDiskEncryption för Windows VMS".
Varning: den här cmdleten startar om den virtuella datorn.

## BESKRIVS

### Exempel 1: inaktivera kryptering för alla volymer på en virtuell Windows-dator
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

Det här kommandot inaktiverar kryptering för volymer av typen allt för den virtuella datorn med namnet VM002 som tillhör resurs gruppen med namnet Group001.
Eftersom parametern *VolumeType* inte anges ställer cmdleten in värdet till all.

### Exempel 2: inaktivera kryptering för data volymer på en virtuell Windows-dator
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

Det här kommandot inaktiverar kryptering för volymer av typen data för den virtuella datorn med namnet VM004 som tillhör resurs gruppen med namnet Group002.

## MALLPARAMETRAR

### -DisableAutoUpgradeMinorVersion
Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Specifes namnet på resursen för Azure Resource Manager som representerar tillägget.
Om den här parametern inte anges använder denna cmdlet standardinställningen "AzureDiskEncryption för Windows VMs".

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den virtuella datorns resurs grupp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Anger krypterings tillägget.
Om du inte anger ett värde för den här parametern används den senaste versionen av tillägget.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på den virtuella dator som denna cmdlet inaktiverar kryptering på.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VolumeType
Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.
Giltiga värden för Windows Virtual-datorer är: 

- Alla
- TIDIGARE
- Värde.
Om du inte anger ett värde för den här parametern är standardvärdet alla.
Det går för närvarande inte att inaktivera kryptering för Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Denna cmdlet genererar inga utdata.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Remove-AzureRmVMDiskEncryptionExtension](./Remove-AzureRmVMDiskEncryptionExtension.md)

[Set-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


