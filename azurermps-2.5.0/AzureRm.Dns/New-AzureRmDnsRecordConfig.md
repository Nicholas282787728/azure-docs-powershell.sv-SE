---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6368cffa168772a384deb99f5a8388aef84f85b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930597"
---
# New-AzureRmDnsRecordConfig

## Sammanfattning
Skapar ett nytt lokalt DNS-postobjekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Kallas
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### Ns
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### MX
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### Resurspost
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### Txt
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### SRV
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### CName
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmDnsRecordConfig** skapar ett lokalt **DnsRecord** -objekt.
En matris med dessa objekt överförs till New-AzureRmDnsRecordSet cmdlet med parametern *DnsRecords* för att ange vilka poster som ska skapas i post uppsättningen.

## BESKRIVS

### Exempel 1: skapa en post mängd av typen A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.
Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).
Den innehåller en enda DNS-post.

### Exempel 2: skapa en post mängd av typen AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.
Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 3: skapa en post uppsättning av typen CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.
Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 4: skapa en post mängd av typen MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.
Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 5: skapa en post uppsättning av typen NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Det här kommandot skapar en **post mängd** med namnet ns1 i zonen myzone.com.
Post uppsättningen är av typen NS och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 6: skapa en post uppsättning av typen PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Det här kommandot skapar en **post mängd** som heter 4 i zonen 3.2.1.in-addr. arpa.
Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 7: skapa en post uppsättning av typen SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Det här kommandot skapar en **post uppsättning** med namnet _sip. _ TCP i zonen myzone.com.
Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post som pekar på IP-2001.2.3.4.

Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

### Exempel 8: skapa en post uppsättning av typen TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Det här kommandot skapar en **post mängd** som heter text i zonen myzone.com.
Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.
Den innehåller en enda DNS-post.

Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.

## MALLPARAMETRAR

### -CNAME
Anger domän namnet för en CNAME-post (kanoniskt namn).

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exchange
Anger namnet på e-postservern för en e-postpost (MX).

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Anger en IPv4-adress för en A-post.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IPv6
Anger en IPv6-adress för en AAAA-post.

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Anger namnet Server namn för en namnserver post (NS).

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
Anger en SRV-post (service port).

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preferens
Anger preferensen för en MX-post.

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Prioritet
Anger prioriteten för en SRV-post.

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Anger mål domän namnet för en pekarresurspost (PTR-post).

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Mål
Anger målet för en SRV-post.

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Värde
Anger värdet för en TXT-post.

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vikt
Anger vikten för en SRV-post.

```yaml
Type: UInt16
Parameter Sets: Srv
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

### Ingen.

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsRecordBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordConfig](./Remove-AzureRmDnsRecordConfig.md)
