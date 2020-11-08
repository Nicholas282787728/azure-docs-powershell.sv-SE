---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099055"
---
# Set-AzureReservedIPAssociation

## Sammanfattning
Associerar en reserverad IP-adress med en befintlig virtuell dator eller moln tjänst.

## FRÅGESYNTAXEN

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureReservedIPAssociation** associerar en reserverad IP-adress med den virtuella IP-adressen (VIP) för en virtuell dator eller moln tjänst som körs.
Den reserverade IP-adressen får inte användas när denna cmdlet anropas och måste finnas i samma område som den virtuella datorn eller moln tjänsten.

Åtgärden tar ungefär 30 sekunder att slutföra och sedan kan den virtuella datorn eller tjänsten nås via den reserverade IP-adressen.

## BESKRIVS

### Exempel 1: Ange en reserverad IP-associering
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

Det här kommandot tilldelar den reserverade IP-adressen som heter ResIp14 till tjänsten PipTestWestEurope.
ResIp14 är en reserverad IP i regionen Västeuropa.

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

### -ReservedIPName
Anger namnet på den reserverade IP-adressen som ska kopplas till en virtuell dator eller tjänst.

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

### -ServiceName
Anger namnet på den tjänst som har den distribution som ska kopplas till den reserverade IP-adressen.

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

### -Plats
Anger distributions platsen.
De acceptabla värdena för den här parametern är:

- Lagring
- Produktionsoperationsföljden

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
Anger namnet på en befintlig VIP-adress som ska kopplas till en reserverad IP.
Se Add-AzureVirtualIP för att lägga till VIP i din moln tjänst.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureReservedIPAssociation](./Remove-AzureReservedIPAssociation.md)


