---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093467"
---
# Stop-AzureVM

## Sammanfattning
Stänger av en virtuell Azure-dator.

## FRÅGESYNTAXEN

### ByName (standard)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Flöde
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureVM** stänger en virtuell dator.

## BESKRIVS

### Exempel 1: avsluta en virtuell dator
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller.

### Exempel 2: avsluta en virtuell dator med hjälp av ett virtuellt dator objekt
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller, med hjälp av det virtuella dator objekt som returnerar **-AzureVM** .

### Exempel 3: avsluta en virtuell dator och låta den virtuella datorn vara etablerad
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller och behåller den etablerad.

### Exempel 4: avsluta en virtuell dator och Tillåt avtilldelning av den senaste VM i distributionen
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Det här kommandot stänger av en virtuell dator som den angivna tjänsten innehåller och tillåter avtilldelning av den senaste virtuella datorn i distributionen.

### Exempel 5: avsluta flera virtuella datorer
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Det här kommandot stänger av flera virtuella datorer som den angivna tjänsten innehåller.

## MALLPARAMETRAR

### -Force
Anger om avtilldelning av den senaste virtuella datorn ska tillåtas i en distribution.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Namn
Anger namnet på den virtuella datorn som ska avslutas.

Använd jokertecknet för att stoppa flera virtuella datorer asynkront.
Med ett jokertecken anropar den här cmdlet åtgärden avsluta https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) i stället för rollen avsluta https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx åtgärd ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ServiceName
Anger namnet på den Azure-tjänst som innehåller den virtuella datorn som ska stängas av.

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

### -StayProvisioned
Anger att denna cmdlet håller den virtuella datorn etablerad.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Anger ett objekt för virtuell dator som identifierar den virtuella datorn för avstängning.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)


