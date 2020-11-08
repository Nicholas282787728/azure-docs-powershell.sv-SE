---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100637"
---
# Remove-WAPackVMSubnet

## Sammanfattning
Tar bort undernät för virtuella datorer.

## FRÅGESYNTAXEN

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
De här ämnena är föråldrade och kommer att tas bort i framtiden.
I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.
För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .

Cmdleten **Remove-WAPackVMSubnet** tar bort undernät för virtuella datorer.

## BESKRIVS

### Exempel 1: ta bort ett undernät för virtuell dator
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

Det första kommandot hämtar det virtuella dator under nätet med namnet ContosoVMSubnet01 med cmdleten **Get-WAPackVMSubnet** och lagrar sedan objektet i variabeln $VMSubnet.

Det andra kommandot tar bort det virtuella dator under nätet som lagras i $VMSubnet.
Med kommandot uppmanas du att bekräfta.

### Exempel 2: ta bort en virtuell dator utan bekräftelse
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

Det första kommandot får moln tjänsten med namnet ContosoVMSubnet02 med hjälp av cmdleten **Get-WAPackVMSubnet** och lagrar sedan objektet i variabeln $VMSubnet.

Det andra kommandot tar bort det virtuella dator under nätet som lagras i $VMSubnet.
Det här kommandot innehåller parametern *Force* .
Du uppmanas inte att bekräfta.

## MALLPARAMETRAR

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

### -PassThru
Returnerar ett objekt som representerar det objekt som du arbetar med.
Denna cmdlet genererar som standard inga utdata.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMSubnet
Anger ett undernät för virtuell dator.
Använd cmdleten **Get-WAPackVMSubnet** för att få en virtuell dator under nät.

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[New-WAPackVMSubnet](./New-WAPackVMSubnet.md)


