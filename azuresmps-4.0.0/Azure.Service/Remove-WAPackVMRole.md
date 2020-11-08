---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100641"
---
# Remove-WAPackVMRole

## Sammanfattning
Tar bort roll objekt för virtuella datorer.

## FRÅGESYNTAXEN

### FromVMRoleObject (standard)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
De här ämnena är föråldrade och kommer att tas bort i framtiden.
I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.
För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .

Cmdleten **Remove-WAPackVMRole** tar bort roll objekt för virtuella datorer.

## BESKRIVS

### Exempel 1: ta bort en virtuell dator roll (som skapades med WAP-portalen)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Det första kommandot får rollen virtuell dator med namnet ContosoVMRole01 med hjälp av cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.

Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.
Med kommandot uppmanas du att bekräfta. Förutsatt att den här virtuella dator rollen skapades med WAP-portalen behöver du inte ange namnet på moln tjänsten.

### Exempel 2: ta bort en virtuell dator roll som skapades när du skapade en moln tjänst manuellt
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Det första kommandot får rollen virtuell dator med namnet "ContosoVMRole02" med cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.

Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.
Med kommandot uppmanas du att bekräfta.
Om den här rollen inte skapades med portalen måste användaren ange namnet på moln tjänsten.
I det här fallet "ContosoCloudService02".

### Exempel 3: ta bort en virtuell dator roll utan bekräftelse
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Det första kommandot får moln tjänsten med namnet ContosoVMRole03 med hjälp av cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.

Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.
Det här kommandot innehåller parametern *Force* .
Du uppmanas inte att bekräfta.

## MALLPARAMETRAR

### -CloudServiceName
Anger namnet på den virtuella datorns moln tjänst.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -VMRole
Anger en virtuell dator roll.
Använd cmdleten **Get-WAPackVMRole** för att få en virtuell dator roll.

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[New-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


