---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585136"
---
# Add-AzureRmLogProfile

## Sammanfattning
Skapar en ny aktivitets logg profil. Denna profil används till att antingen arkivera aktivitets loggen på ett Azure Storage-konto eller strömma den till en Azure Event Hub i samma prenumeration. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmLogProfile** skapar en logg profil.

- **Lagrings konto** – det finns inget standard lagrings konto (Premium Storage-konto stöds inte). Det kan antingen vara av typen ARM eller klassiskt. Om den är inloggad på ett lagrings konto debiteras kostnaden för att lagra aktivitets loggen med normal standard lagrings taxa. Det kan bara finnas en enda logg profil per prenumeration som bara är ett lagrings konto per prenumeration som kan användas för att exportera aktivitets loggen. 

- **Händelsehubben-det** kan bara finnas en enda logg profil per prenumeration som bara en händelse gren per prenumeration kan användas för att exportera aktivitets loggen. Om aktivitets loggen strömmas till en händelsehubben tillämpas standard Event Hub-priser. 

I aktivitets loggen kan händelser gälla en region eller kan vara "globalt". Global innebär detta att dessa händelser är region agnostics och att de är oberoende av regionen, i de flesta händelser hamnar i den kategorin. Om aktivitets loggnings profilen är inställd från portalen lägger den implicit till "global" tillsammans med alla andra regioner som är markerade i användar gränssnittet. När du använder en cmdlet måste platsen som "global" anges explicit från valfri annan region. 

**Obs!** **om du inte anger "globalt" i platserna kommer det att leda till att huvud aktivitets loggen inte exporteras.** 

Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.

## BESKRIVS

### Exempel 1: lägga till en ny logg profil för att exportera aktivitets loggen som matchar plats tillståndet till ett lagrings konto
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## MALLPARAMETRAR

### -Kategori
Anger listan över kategorier.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen för logg profilen.
Giltiga värden: kör nedan cmdlet för att få den senaste listan över platser. 

Get-AzureLocation | Välj DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på profilen.

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

### -RetentionInDays
Anger bevarande principen i dagar. Det här är antalet dagar som loggar bevaras i det angivna lagrings kontot. För att behålla data förinställd på **0** för alltid Om det inte anges blir standardvärdet **0**. Vanliga fakturerings avgifter för standard lagring eller Event Hub gäller för data lagring.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Anger ID för Service Bus-regeln.

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

### -StorageAccountId
Anger ID för lagrings kontot. ID är det fullt kvalificerade resurs-ID: t för lagrings kontot, till exempel  

/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

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
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmLogProfile](./Get-AzureRmLogProfile.md)

[Remove-AzureRmLogProfile](./Remove-AzureRmLogProfile.md)


