---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c6479f9358322ae76eeb2fdf3cb9f2bb922e462
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929430"
---
# Set-AzureRmDnsRecordSet

## Sammanfattning
Uppdaterar en DNS-post.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmDnsRecordSet** uppdaterar en post uppsättning i Azure DNS-tjänsten från ett lokalt **Recordset** -objekt.

Du kan skicka ett **Recordset** -objekt som en parameter eller med hjälp av pipeline-operatorn.

Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.

Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.
Det skyddar mot samtidig ändringar.
Du kan dölja den här funktionen med hjälp av parametern *Overwrite* , som uppdaterar post uppsättningen oavsett samtidig ändring.

## BESKRIVS

### Exempel 1: uppdatera en post uppsättning
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

Det första kommandot använder cmdleten Get-AzureRmDnsRecordSet för att hämta angiven post uppsättning och lagrar den sedan i $RecordSet-variabeln.

De andra och tredje kommandona är offline-operationer för att lägga till två poster i post uppsättningen.

I det sista kommandot används cmdleten **set-AzureRmDnsRecordSet** för att bekräfta uppdateringen.

### Exempel 2: uppdatera en SOA-post
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

Det första kommandot använder cmdleten **Get-AzureRmDnsRecordset** för att hämta angiven post uppsättning och lagrar den sedan i $Recordset variabel.

Det andra kommandot uppdaterar den angivna SOA-posten i $RecordSet.

Det sista kommandot använder cmdleten **set-AzureRmDnsRecordSet** för att sprida uppdateringen i $Recordset.

## MALLPARAMETRAR

### -Skriver över
Anger att post uppsättningen ska uppdateras oavsett samtidig ändring.

Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.
Det skyddar mot samtidig ändringar.
För att förhindra att det här beteendet visas kan du använda parametern *Overwrite* , som leder till att post uppsättningen uppdateras oberoende av de ändringar du gör.

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

### -Post uppsättning
Anger den **post mängd** som ska uppdateras.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte. Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. DNS. DnsRecordSet
Du kan skicka ett **Recordset** -objekt till denna cmdlet.

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsRecordSet
Denna cmdlet returnerar ett objekt som representerar det uppdaterade **Recordset** -objektet.

## ANMÄRKNINGAR
Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.
Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.

Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.
Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta. 

## RELATERADE LÄNKAR

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)
