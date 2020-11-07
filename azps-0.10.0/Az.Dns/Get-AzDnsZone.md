---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924598"
---
# Get-AzDnsZone

## Sammanfattning
Hämtar en DNS-zon.

## FRÅGESYNTAXEN

### Standard (standard)
```
Get-AzDnsZone [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDnsZone** hämtar en DNS-zon (Domain Name System) från den angivna resurs gruppen.
Om du anger parametern *Name* returneras ett enskilt **dnsZone** -objekt.
Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.
Du kan använda **dnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.

## BESKRIVS

### Exempel 1: Hämta en zon
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Det här exemplet hämtar DNS-zonen som heter myzone.com från den angivna resurs gruppen och lagrar den sedan i $Zone variabel.

### Exempel 2: Hämta alla zoner i en resurs grupp
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Det här exemplet får alla DNS-zoner i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.

### Exempel 3: Hämta alla zoner i ett abonnemang
```
PS C:\> $Zones = Get-AzDnsZone
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet tillåter inte pipe-inmatning.

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsZone
Denna cmdlet returnerar ett objekt som representerar DNS-zonen.
Om inget zonnamn anges returneras en matris med zon objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
