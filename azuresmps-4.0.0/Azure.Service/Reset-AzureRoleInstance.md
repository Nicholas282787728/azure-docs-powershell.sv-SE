---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093206"
---
# Reset-AzureRoleInstance

## Sammanfattning
Begär en omstart eller återbildning av en enskild roll instans eller alla roll instanser för en viss roll.

## FRÅGESYNTAXEN

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Reset-AzureRoleInstance** begär en omstart eller en bild av en roll instans som körs i en distribution.
Den här åtgärden körs synkront.
När du startar om en roll instans använder Azure instansen offline, startar om det underliggande operativ systemet för den instansen och ansluter sedan till instansen online.
Alla data som skrivs till den lokala disken fortsätter att starta om.
Alla data som finns i minnet förloras.

Om en roll instans rebildas beror olika beteende beroende på typen av roll.
När rollen ändras för en webb-eller arbets roll använder Azure rollen offline och skriver en ny installation av Azure gäst operativ systemet på den virtuella datorn.
Rollen ansluts sedan online igen.
För en virtuell dator roll använder Azure rollen offline när du har angett den för att den ska kopplas från, så återanvänds den anpassade avbildningen som du har tillhandahållit.

Azure försöker upprätthålla data från alla lokala lagrings resurser när rollen är ombildad; om det däremot inte uppstår något fel kan den lokala lagrings resursen gå förlorad.
Om ditt program kräver att data bevaras kan det vara bra att skriva till en hållbar data källa, till exempel en Azure-enhet.
Alla data som skrivs till en annan lokal katalog än den som definieras av den lokala lagrings resursen försvinner när rollen ändras.

## BESKRIVS

### Exempel 1: starta om en roll instans
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Det här kommandot startar om den roll instans som heter MyWebRole_IN_0 i den mellanliggande distributionen av MySvc01-tjänsten.

### Exempel 2: återpå en roll instans
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Det här kommandot återavbildningar roll instanser för mellanlagring av MySvc01-moln tjänsten.

### Exempel 3: återbild alla roll instanser
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Det här kommandot återavbildningar alla roll instanser i produktions distributionen av MySvc01-tjänsten.

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

### -InstanceName
Anger namnet på den roll instans som ska återbildas eller startas om.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### -Starta om
Anger att den här cmdleten startar om den angivna roll instansen eller om ingen är angiven, alla roll instanser.
Du måste ange antingen en *omstart* eller en *bild* parameter, men inte båda.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ombild
Anger att denna cmdlet ombildar den angivna roll förekomsten eller, om ingen anges, alla roll instanser.
Du måste ange antingen en *omstart* eller en *bild* parameter, men inte båda.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Anger namnet på tjänsten.

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

### -Plats
Anger distributions miljön där roll instanserna körs.
Giltiga värden är: produktion och mellanlagring.
Du kan inkludera antingen parametern *DeploymentName* eller *slot* , men inte båda.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

[Set-AzureRole](./Set-AzureRole.md)


