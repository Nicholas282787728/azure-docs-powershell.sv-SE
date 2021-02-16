---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253785"
---
# New-AzDnsRecordSet

## SYNOPSIS
Skapar en DNS-postuppsättning.

## SYNTAX

### Fält (standard)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzDnsRecordSet** skapar en ny DNS-post (Domain Name System) med angivet namn och typ i den angivna zonen.
Ett **RecordSet-objekt** är en uppsättning DNS-poster med samma namn och typ.
Observera att namnet är relativt zonen och inte det fullständigt kvalificerade namnet.
Parametern *DnsRecords* anger posterna i postuppsättningen.
Den här parametern använder en matris med DNS-poster som skapas med New-AzDnsRecordConfig.
Du kan använda en pipelineoperator för att överföra ett **DnsZone-objekt** till den här cmdleten, eller så kan du överföra ett **DnsZone-objekt** som  zone-parameter, eller så kan du ange zonen med namn.
Du kan använda *parametern Confirm* och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.
Om det redan finns en matchande **RecordSet** (samma namn och posttyp) måste du ange parametern *Overwrite,* annars skapar cmdleten inte en ny **RecordSet.**

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
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

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
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen MX och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

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
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

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
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 8: Create a RecordSet of type TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot **skapas en Postuppsättning** med namnet text i myzone.com.
Postuppsättningen är av typen TXT och har en TTL på 1 timme (3 600 sekunder).
Den innehåller en enda DNS-post.
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 9: Skapa en RecordSet i zon apex
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Det här kommandot **skapar en RecordSet** med apex (eller rot) för myzone.com.
Det gör du genom att postuppsättningens namn anges som "@" (inklusive citattecken).
Du kan inte skapa CNAME-poster i en zons apex.
Det här är ett villkor av DNS-standarderna. är det inte en begränsning i Azure DNS.
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 10: Skapa en postuppsättning med jokertecken
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Med det här kommandot skapas **en RecordSet** med namnet * i myzone.com.
Det här är en postuppsättning med jokertecken.
Om du vill **skapa en recordset** med bara en rad pn_PowerShell_short, eller om du vill skapa en postuppsättning med flera poster, se exempel 1.

### Exempel 11: Skapa en tom postuppsättning
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Med det här kommandot skapas **en RecordSet** med namnet www i myzone.com.
Postuppsättningen är av typen A och har en TTL på 1 timme (3 600 sekunder).
Det här är en tom postuppsättning som fungerar som en platshållare som du senare kan lägga till poster i.

### Exempel 12: Skapa en postuppsättning och ignorera alla bekräftelser
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Med det här kommandot skapas **en RecordSet.**
Parametern *Overwrite* säkerställer att den här postuppsättningen skriver över alla befintliga postuppsättningar med samma namn och typ (befintliga poster i den postuppsättningen går förlorade).
*Bekräftelseparametern* med värdet $False utelämnar bekräftelsemeddelandet.

## PARAMETERS

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

### -DnsRecords
Anger matrisen med DNS-poster som ska ingå i postuppsättningen.
Du kan använda cmdlet New-AzDnsRecordConfig för att skapa DNS-postobjekt.
Se exemplen för mer information.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadata
Anger en matris med metadata som ska associeras med RecordSet.
Metadata anges med namnvärdepar som representeras som hashtabeller, till exempel @{"dept"="shopping";" env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på den **postuppsättning som ska** skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Anger att den här cmdleten skriver över den angivna **postuppsättningen** om den redan finns.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordType
Anger vilken typ av DNS-post som ska skapas.
Giltiga värden är:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT SOA-poster skapas automatiskt när zonen skapas och kan inte skapas manuellt.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger resursgruppen som innehåller DNS-zonen.
Du måste också ange *zoneName-parametern* för att ange zonnamnet.
Du kan också ange zon- och resursgruppen genom att skicka in ett DNS-zonobjekt med hjälp av *zonparametern.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Alias målresurs-ID.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
Anger TTL (Time to Live) för DNS RecordSet.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Anger den DNSZone där recordSet ska **skapas.**
Du kan också ange zonen med hjälp av *parametrarna ZoneName* *och ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Anger namnet på den zon där postuppsättningen ska **skapas.**
Du måste också ange den resursgrupp som innehåller zonen med *parametern ResourceGroupName.*
Du kan också ange zon- och resursgruppen genom att skicka in ett DNS-zonobjekt med hjälp av *zonparametern.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### Microsoft.Azure.Commands.DNS.DNSZone

### System.UInt32

### Microsoft.Azure.Management.DNS.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.dns.dnsRecordBase[]

## UTDATA

### Microsoft.Azure.Commands.dns.dnsRecordSet

## ANTECKNINGAR
Du kan använda *parametern Bekräfta* för att styra om den här cmdleten uppmanar dig att bekräfta.
Som standard uppmanar cmdleten dig att bekräfta om variabeln $ConfirmPreference Windows PowerShell har värdet Medel eller lägre.
Om du anger *Bekräfta* *eller Bekräfta:$True,* uppmanas du i den här cmdleten att bekräfta innan den körs.
Om du *anger Bekräfta:$False* visas ingen bekräftelse i cmdleten.

## RELATERADE LÄNKAR

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
