---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924613"
---
# Get-AzDnsRecordSet

## Sammanfattning
Hämtar en DNS-post.

## FRÅGESYNTAXEN

### Fält
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### Serverobjektet
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDnsRecordSet** hämtar DNS-postuppsättningen (Domain Name System) med det angivna namnet och typen, i den angivna zonen.

Om du inte anger parametrarna *Name* eller *RecordType* returnerar denna cmdlet alla post uppsättningar av angiven typ i zonen.
Om du anger parametern *RecordType* men inte parametern *Name* returnerar denna cmdlet alla post uppsättningar av den angivna post typen.

Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen och resurs gruppen efter namn.

## BESKRIVS

### Exempel 1: hämta post uppsättningar med ett angivet namn och en viss typ
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Det här kommandot hämtar post uppsättningen med post typen en namngiven webb i den angivna resurs gruppen och zonen och lagrar den sedan i $RecordSet variabel.
Eftersom parametrarna *Name* och *RecordType* anges returneras endast ett **Recordset** -objekt.

### Exempel 2: hämta post uppsättningar av en viss typ
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Det här kommandot får en matris över alla post uppsättningar med post typen A i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.

### Exempel 3: Hämta alla post uppsättningar i en zon
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Det här kommandot får en matris över alla post uppsättningar i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.

### Exempel 4: Hämta alla post uppsättningar i en zon med ett DnsZone-objekt
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Det här exemplet motsvarar exempel 3 ovan.
Den här gången anges zonen med ett Zone-objekt.

## MALLPARAMETRAR

### -Namn
Anger namnet på den **post mängd** som ska visas.
Om du inte anger parametern *Name* returneras alla post uppsättningar av den angivna typen.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Anger den typ av DNS-post som den här cmdleten får.

Giltiga värden är: 

- Kallas
- AAAA
- CNAME
- MX
- NS
- RESURSPOST
- BEGÄRANDEN
- SRV
- TXT

Om du inte anger parametern *RecordType* måste du också utelämna parametern *Name* . Denna cmdlet returnerar då alla post uppsättningar i zonen (i alla namn och typer).

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger den resurs grupp som innehåller DNS-zonen.
Zonnamn måste också anges med parametern *Zonnamn* .

Alternativt kan du ange zonen och resurs gruppen genom att skicka ett **dnsZone** -objekt med parametern *Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Anger den DNS-zon som innehåller den post uppsättning som denna cmdlet får.
Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zonnamn
Anger namnet på den DNS-zon som innehåller den post som ska visas.
Resurs gruppen som innehåller zonen måste också anges med parametern *ResourceGroupName* .

Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. DNS. DnsZone
Du kan ha ett **dnsZone** -objekt i denna cmdlet.
**DnsZone** -objektet representerar den zon där du vill söka efter **Recordset** -objektet.

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsRecordSet
Denna cmdlet returnerar ett eller flera objekt som representerar de post uppsättningar som hittas.
Det kommer att finnas högst en **post uppsättning** som returneras om parametern *Name* och *RecordType* har angetts, annars returneras flera **Recordset** -objekt som en matris.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


