---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930602"
---
# Get-AzureRmDnsZone

## Sammanfattning
Hämtar en DNS-zon.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Standard (standard)
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### ResourceGroup
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmDnsZone** hämtar en DNS-zon (Domain Name System) från den angivna resurs gruppen.
Om du anger parametern *Name* returneras ett enskilt **dnsZone** -objekt.
Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.
Du kan använda **dnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.

## BESKRIVS

### Exempel 1: Hämta en zon
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Det här exemplet hämtar DNS-zonen som heter myzone.com från den angivna resurs gruppen och lagrar den sedan i $Zone variabel.

### Exempel 2: Hämta alla zoner i en resurs grupp
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

Det här exemplet får alla DNS-zoner i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.

### Exempel 3: Hämta alla zoner i ett abonnemang
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

I det här exemplet får du alla DNS-zoner i den aktuella Azure-prenumerationen och lagrar dem i $Zones variabel.

## MALLPARAMETRAR

### -Namn
Anger namnet på den DNS-zon som ska visas.

Om du inte anger ett värde för parametern *Name* får denna cmdlet alla DNS-zoner i den angivna resurs gruppen.
Om du också utelämnar parametern *ResourceGroupName* får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller den DNS-zon som ska visas.

Om du inte anger *ResourceGroupName* måste du också utelämna parametern *Name* .
I det här fallet får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.

```yaml
Type: String
Parameter Sets: ResourceGroup
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

### Ingen
Denna cmdlet tillåter inte pipe-inmatning.

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsZone
Denna cmdlet returnerar ett objekt som representerar DNS-zonen.
Om inget zonnamn anges returneras en matris med zon objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
