---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575718"
---
# Get-AzureRmVMAccessExtension

## Sammanfattning
Hämtar information om VMAccess-tillägget.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmVMAccessExtension** hämtar information om tillägget virtuell dator åtkomst (VMAccess).

## BESKRIVS

### Exempel 1: skaffa VMAccess-tillägget
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

Det här kommandot får tillägget VMAccess med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.

### Exempel 2: Hämta instans vyn för VMAccess-tillägget
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

Det här kommandot hämtar instans vyn för VMAccess-tillägget med namnet ContosoTest för den virtuella datorn med namnet VirtualMachine07.

## MALLPARAMETRAR

### -Namn
Anger namnet på den fil ändelse som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
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

### -Status
Anger att denna cmdlet endast får instans vyn av tillägget.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på en virtuell dator.
Denna cmdlet hämtar information om VMAccess för den virtuella datorn som den här parametern anger.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmVMAccessExtension](./Remove-AzureRmVMAccessExtension.md)

[Set-AzureRmVMAccessExtension](./Set-AzureRmVMAccessExtension.md)

[Get-AzureRmVMExtension](./Get-AzureRmVMExtension.md)


