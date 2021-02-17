---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234439"
---
# New-AzDnsRecordConfig

## SYNOPSIS
Skapar ett nytt lokalt DNS-objekt.

## SYNTAX

### A
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Aaaa
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NS
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Ptr
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Txt
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Srv
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzDnsRecordConfig** skapar ett lokalt **DnsRecord-objekt.**
En matris med dessa objekt skickas till cmdleten New-AzDnsRecordSet med parametern *DnsRecords* för att ange vilka poster som ska skapas i postuppsättningen.

## EXEMPEL

### Exempel 1: Skapa en postuppsättning av typen A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen A och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.

### Exempel 2: Create a RecordSet of type AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen AAAA och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 3: Create a RecordSet of type CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

I det här exemplet skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen CNAME och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 4: Create a RecordSet of type MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen MX och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 5: Skapa en postuppsättning av typen NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot **skapas en RecordSet** med namnet ns1 i myzone.com.
Postuppsättningen är av typen NS och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 6: Skapa en postuppsättning av typen PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Det här kommandot skapar **en RecordSet** med namnet 4 i 3.2.1.in-addr.arpa.
Postuppsättningen är av typen PTR och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 7: Create a RecordSet of type SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot **skapas en RecordSet** _sip._tcp i zonen myzone.com.
Postuppsättningen är av typen SRV och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post som pekar på IP-adressen 2001.2.3.4.
Tjänsten (sip) och protokollet (tcp) anges som en del av postuppsättningsnamnet, inte som en del av postdata.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 8: Create a RecordSet of type TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot **skapas en postuppsättning** med namnet text i myzone.com.
Postuppsättningen är av typen TXT och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en RecordSet** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

## PARAMETERS

### -CaaFlags
Flaggor för CAA-posten som ska läggas till. Måste vara ett tal mellan 0 och 255.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
Kodfältet för DEN CAA-post som ska läggas till.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Värdefältet för den CAA-post som ska läggas till.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cname
Anger domännamnet för en kanonisk namnpost (CNAME).

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -Exchange
Anger exchange-servernamnet för en MX-post (Mail Exchange).

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Anger en IPv6-adress för en AAAA-post.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Anger namnservernamnet för en namnserverpost (NS).

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
Anger porten för en tjänstpost (SRV).

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preference
Anger inställningen för en MX-post.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Anger prioriteten för en SRV-post.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Anger måldomännamnet för en pekarresurspost (PTR).

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target
Anger målet för en SRV-post.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Anger vikt för en SRV-post.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.UInt16

### System.Byte

## UTDATA

### Microsoft.Azure.Commands.dns.dnsRecordBase

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordConfig](./Remove-AzDnsRecordConfig.md)
