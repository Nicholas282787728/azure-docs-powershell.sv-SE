---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099504"
---
# Get-AzureWebsite

## Sammanfattning
Får Azure-webbplatser i det aktuella abonnemanget.

## FRÅGESYNTAXEN

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureWebsite** hämtar information om Azure-webbplatserna i det aktuella abonnemanget.

Som standard får **Get-AzureWebsite** alla Azure-webbplatser i den aktuella prenumerationen och returnerar ett objekt med grundläggande information om webbplatserna.
När du använder parametern *Name* returnerar **-AzureWebsite** ett objekt med omfattande information, inklusive konfigurations information.

Det aktuella abonnemanget är den prenumeration som är "aktuell". Använd den *aktuella* parametern för cmdleten [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) för att hitta den aktuella prenumerationen.
Använd cmdleten [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) för att ändra aktuell prenumeration.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: Hämta alla webbplatser i prenumerationen
```
PS C:\> Get-AzureWebsite
```

Det här kommandot får alla Azure-webbplatser i det aktuella abonnemanget.

### Exempel 2: Hämta en webbplats med namn
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Det här kommandot får detaljerad information om ContosoWeb Azure-webbplatsen, inklusive konfigurations information.
När du använder parametern *Name* returnerar **AzureWebsite** ett **SiteWithConfig** -objekt med utökad information om webbplatsen.

### Exempel 3: få detaljerad information om alla webbplatser
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Det här kommandot får detaljerad information om alla webbplatser i prenumerationen.
Den använder kommandot **Get-AzureWebsite** för att hämta alla webbplatser och använder sedan framenser **-Object** cmdlet för att hämta varje webbplats med namn.

### Exempel 4: få information om en distributions plats
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Det här kommandot får du mellanlagrings platsen för ContosoWeb webbplats.
Med distributions platser kan du testa olika versioner av din Azure-webbplats utan att släppa dem till allmänheten.

### Exempel 5: Hämta webbplats instanser
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

Kommandona i det här exemplet använder egenskapen instances för en Azure-webbplats för att få information om för tillfället aktiva webbplats instanser.
Egenskapen **instances** lades till i **SiteWithConfig** -objektet i version 0.8.3 i Azure-modulen.

Det första kommandot får instans-ID: na för alla instanser av en webbplats som körs för tillfället.
Det andra kommandot får antalet aktiva instanser av webbplatsen.
Du kan använda **Count** -egenskapen på vilken matris som helst.

## MALLPARAMETRAR

### -Namn
Hämtar detaljerad konfigurations information om den angivna webbplatsen.
Ange namnet på en webbplats i prenumerationen.
Som standard får **Get-AzureWebsite** alla webbplatser i det aktuella abonnemanget.
Värdet *Name* stöder inte jokertecken.

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
Hämtar den angivna distributions platsen för webbplatsen.
Ange plats namnet, till exempel "organisering" eller "produktion".
Mer information om distributions platser finns i stegvis distribution på Microsoft Azure-webbplatser https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Använd Set-AzureWebsite cmdlet för att lägga till en distributions plats på en befintlig Azure-webbplats.

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

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilities. sites. Services. webentities. webbplats
Som standard returnerar **Get-AzureWebsite** en matris med **webbplats** objekt.

### Microsoft. WindowsAzure. commands. Utilities. webentities. SiteWithConfig
När du använder parametern *Name* returnerar **AzureWebsite** ett **SiteWithConfig** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Stopp-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


