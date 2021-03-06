---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929217"
---
# Get-UsageAggregates

## Sammanfattning
Hämtar den rapporterade användnings informationen för Azure-prenumeration.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-UsageAggregates** hämtar den aggregerade Azure-prenumerationens användnings data genom följande egenskaper: 

- Start-och slut tider för när användning rapporterades.

- Mängd precision, antingen dagligen eller varje timme.

- Instans nivå information för flera instanser av samma resurs.

För enhetliga resultat baseras data som returneras när användnings uppgifterna rapporterades av Azure-resursen.

Mer information finns i referens för Azure Bill REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) i Microsoft Developer Network Library.

## BESKRIVS

### Exempel 1: Hämta abonnemangs data
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Det här kommandot hämtar den rapporterade användnings informationen för prenumerationen mellan 5/2/2015 och 5/5/2015.

## MALLPARAMETRAR

### -AggregationGranularity
Anger agg regerings precisionen för data.
Giltiga värden är: per dag och timme.

Standardvärdet är dagligen.

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Anger det tilläggs token som hämtades från svars texten i det föregående samtalet.
För en stor resultat mängd visas svaren med hjälp av fortsättnings-token.
Den fortsatta token fungerar som ett bok märke för status.
Om du inte anger den här parametern hämtas data från början av den dag eller timme som anges i *ReportedStartTime*.
Vi rekommenderar att du följer länken Nästa i svaret till sida med data.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -ReportedEndTime
Anger den rapporterade slut tiden för när resursförbrukning registrerades i Azure-fakturerings systemet.

Azure är ett distribuerat system som sträcker sig över flera data Center över hela världen, så det finns en fördröjning mellan när resursen faktiskt förbrukades, vilket är resursanvändnings tiden och när användnings händelsen nådde fakturerings systemet, vilket är den tid som rapporter ATS för resursanvändningen.
Om du vill få alla användar händelser för en prenumeration som rapporter ATS för en viss tids period frågar du efter rapporterings tid.
Även om du frågar efter rapporterings tid aggregerar cmdleten svars informationen efter resursanvändnings tid.
Resursanvändnings data är den användbara pivottabellen för analys av data.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Anger den rapporterade start tiden för när resursförbrukning registrerades i Azure-fakturerings systemet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Anger om den här cmdleten returnerar information om förekomst nivå med användnings data.

Standardvärdet är $True.

Om $False, aggregerar tjänsten resultaten på Server sidan och returnerar därför färre mängd grupper.
Om du till exempel kör tre webbplatser får du tre linje objekt som standard för webbplats förbrukning.
Men när värdet är $False döljs alla data för samma **subscriptionId** , **meterId** , **usageStartTime** och **usageEndTime** i ett enda objekt.

```yaml
Type: Boolean
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

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

