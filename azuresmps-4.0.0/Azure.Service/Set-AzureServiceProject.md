---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099049"
---
# Set-AzureServiceProject

## Sammanfattning
Anger standard plats, prenumeration, plats och lagrings konto för den aktuella tjänsten.

## FRÅGESYNTAXEN

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureServiceProject** anger distributions plats, plats, lagrings konto och abonnemang för den aktuella tjänsten.
Dessa värden används när tjänsten publiceras till molnet.

## BESKRIVS

### Exempel 1: grundläggande inställningar
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Anger distributions platsen för tjänsten till Nord Central USA-regionen.
Ställer in distributions platsen för produktion. Anger det lagrings konto som ska användas för att mellanlagra tjänst definitionen på myStorageAccount.
Anger den prenumeration som ska vara värd för tjänsten för prenumeration.
När tjänsten publiceras i molnet kommer den att finnas i ett Data Center i Nord Central USA-regionen, den uppdaterar distributions platsen och använder det angivna abonnemangs-och lagrings konto.

## MALLPARAMETRAR

### -Plats
Den region där tjänsten hanteras.
Det här värdet används när tjänsten publiceras till molnet.
Möjliga värden är: överallt, överallt, världen, USA, Östasien, öst, Nord Central USA, Nord Europa, södra Central USA, Sydostasien, Västeuropa, västra USA.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.
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

### -Plats
Den plats (produktion eller mellanlagring) som tjänsten finns i.
Det här värdet används när tjänsten publiceras till molnet.
Möjliga värden är: produktion, mellanlagring.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lagring
Det lagrings konto som ska användas när tjänste paketet laddas upp till molnet.
Om lagrings kontot inte finns skapas det när tjänsten publiceras till molnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
* nod-dev, php-dev, python-dev

## RELATERADE LÄNKAR

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Publicera – AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


