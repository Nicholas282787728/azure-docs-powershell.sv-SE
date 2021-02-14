---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235007"
---
# Get-UsageAggregates

## SYNOPSIS
Hämtar den rapporterade användningsinformationen för Azure-prenumerationer.

## SYNTAX

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-UsageAggregates** får aggregerade användningsdata för Azure-prenumerationer med följande egenskaper: 
- Start- och sluttider för när användningen rapporterades.
- Aggregeringsprecision, antingen dagligen eller varje timme.
- Instansnivåinformation för flera instanser av samma resurs.
För konsekventa resultat baseras returnerade data på när användningsinformationen rapporterades av Azure-resursen.
Mer information finns i Rest API-referens för Azure Billing https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( i Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network-biblioteket.

## EXEMPEL

### Exempel 1: Hämta prenumerationsdata
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Det här kommandot hämtar rapporterad användningsdata för prenumerationen mellan 2015-05-02 och 2015-05-05.

## PARAMETERS

### -AggregationGranularity
Anger aggregeringsprecisionen för data.
Giltiga värden är: varje dag och varje timme.
Standardvärdet är Varje dag.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
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
Anger fortsättningstoken som hämtades från svarstexten i föregående samtal.
För en stor resultatuppsättning sidoras svar med hjälp av fortsättningstoken.
Fortsättningstoken fungerar som ett bokmärke för förlopp.
Om du inte anger den här parametern hämtas data från början av den dag eller timme som anges i *ReportedStartTime.*
Vi rekommenderar att du följer nästa länk i svaret på sidan genom data.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedEndTime
Anger den rapporterade sluttiden för när resursanvändningen registrerades i Azure-faktureringssystemet.
Azure är ett distribuerat system som spänner över flera datacenter över hela världen, så det finns en fördröjning mellan när resursen faktiskt förbrukades, vilket är tiden för resursanvändning och när användningshändelsen nått faktureringssystemet, vilket är den rapporterade tiden för resursanvändning.
För att få alla användningshändelser för en prenumeration som rapporterats för en tidsperiod frågar du efter rapporterad tid.
Även om du frågar med rapporterad tid aggregerar cmdleten svarsdata efter resursanvändningstiden.
Resursanvändningsdata är den användbara pivottabellen för att analysera data.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Anger den rapporterade starttiden för när resursanvändningen registrerades i Azure-faktureringssystemet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VisaDetaljer
Anger om denna cmdlet returnerar information på instansnivå med användningsdata.
Standardvärdet är $True.
Om $False aggregerar tjänsten resultatet på serversidan och returnerar därför färre mängdgrupper.
Om du till exempel kör tre webbplatser får du som standard tre radobjekt för webbplatsanvändning.
Men när värdet $False komprimeras alla data för samma **prenumerations-ID,** **meterId,** **usageStartTime** och **usageEndTime** till ett enda radobjekt.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## ANTECKNINGAR

## RELATERADE LÄNKAR
