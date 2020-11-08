---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099762"
---
# Get-AzureVMImage

## Sammanfattning
Hämtar egenskaperna för en eller flera listor med operativ system eller en virtuell dator bild i bild lagrings platsen.

## FRÅGESYNTAXEN

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureVMImage** hämtar egenskaper för en eller flera listor med operativ system eller en virtuell dator bild i bild lagrings platsen.
Cmdleten returnerar information för alla bilder i databasen, eller om en viss bild visas om bild namnet anges.

## BESKRIVS

### Exempel 1: Hämta ett specifikt bild objekt från den aktuella bild lagrings platsen.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Det här kommandot hämtar bild objekt med namnet Image001 från den aktuella bild lagrings platsen.

### Exempel 2: Hämta alla bilder från den aktuella bild databasen
```
PS C:\> Get-AzureVMImage
```

Det här kommandot hämtar alla bilder från den aktuella bild lagrings platsen.

### Exempel 3: Ange prenumerationens kontext och hämta sedan alla bilder
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Det här kommandot anger prenumerationens kontext och hämtar sedan alla bilder från bild lagrings platsen.

## MALLPARAMETRAR

### -ImageName
Anger namnet på operativ system eller virtuell dator bild i bild lagrings platsen.
Om du inte anger den här parametern returneras alla bilder.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Spara – AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


