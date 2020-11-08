---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093377"
---
# Get-AzureDataDisk

## Sammanfattning
Hämtar Azure data-diskar.

## FRÅGESYNTAXEN

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureDataDisk** hämtar ett objekt som representerar data diskarna på en virtuell Azure-dator.
Om du vill hämta ett specifikt data disk objekt anger du diskens logiska enhets nummer (LUN).

## BESKRIVS

### Exempel 1: Hämta alla data diskar för en virtuell dator
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

Det här kommandot får den virtuella datorn som heter VirtualMachine07 i tjänsten ContosoService med hjälp av cmdleten **Get-AzureVM** .
Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.
Den aktuella cmdleten får alla data diskar för den här virtuella datorn.

### Exempel 2: Hämta en särskild data disk för en vituralvirtual machinevirtual
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

Det här kommandot får den virtuella datorn med namnet VirtualMachine07 i tjänsten som heter ContosoService.
Kommandot skickar den virtuella datorn till den aktuella cmdleten.
Den aktuella cmdleten får den data disk som har LUN 2.

## MALLPARAMETRAR

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LUN
Anger LUN för data enheten på den virtuella datorn.
Giltiga värden är: 0 till 15.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

### -VM
Anger det virtuella datorobjektet för vilket denna cmdlet hämtar data diskar.
Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)


