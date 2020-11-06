---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574367"
---
# Get-AzureRmVMDscExtensionStatus

## Sammanfattning
Hämtar statusen för DSC-filtillägg för en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmVMDscExtensionStatus** får statusen för den önskade tilläggs HANTERAREN (DSC) för en virtuell dator i en resurs grupp.
När en konfiguration används, ger denna cmdlet utdata som är konsekvent med Start-DscConfiguration cmdlet.

## BESKRIVS

## MALLPARAMETRAR

### -Namn
Anger namnet på Azure Resource Manager-resursen som representerar tillägget.
Set-AzureRmVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzureRmVMDscExtensionStatus**.
Ange endast den här parametern om du har ändrat standard namnet i set cmdlet eller använt ett annat resurs namn i en resurs hanterares mall.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -VMName
Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

[Set-AzureRmVMDscExtension](./Set-AzureRmVMDscExtension.md)


