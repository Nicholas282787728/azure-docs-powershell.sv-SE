---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270705"
---
# <span data-ttu-id="af59f-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af59f-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="af59f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af59f-102">SYNOPSIS</span></span>
<span data-ttu-id="af59f-103">Skapar en DNS-post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="af59f-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="af59f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af59f-104">SYNTAX</span></span>

### <span data-ttu-id="af59f-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="af59f-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af59f-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="af59f-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af59f-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="af59f-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af59f-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="af59f-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af59f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af59f-109">DESCRIPTION</span></span>
<span data-ttu-id="af59f-110">Cmdleten **New-AzDnsRecordSet** skapar en ny DNS-post (Domain Name System) med det angivna namnet och typen i den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="af59f-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="af59f-111">Ett **Recordset** -objekt är en uppsättning DNS-poster med samma namn och typ.</span><span class="sxs-lookup"><span data-stu-id="af59f-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="af59f-112">Observera att namnet är relativt till zonen och inte till det fullständigt kvalificerade namnet.</span><span class="sxs-lookup"><span data-stu-id="af59f-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="af59f-113">Parametern *DnsRecords* anger posterna i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="af59f-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="af59f-114">Den här parametern tar en matris med DNS-poster, utformad med AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="af59f-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="af59f-115">Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen efter namn.</span><span class="sxs-lookup"><span data-stu-id="af59f-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="af59f-116">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af59f-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="af59f-117">Om det redan finns en matchande **post uppsättning** (samma namn och posttyp) måste du ange den *överskrivnings* parametern, annars skapas inte en ny **post uppsättning** .</span><span class="sxs-lookup"><span data-stu-id="af59f-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="af59f-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af59f-118">EXAMPLES</span></span>

### <span data-ttu-id="af59f-119">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="af59f-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="af59f-120">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-121">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="af59f-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-122">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="af59f-123">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="af59f-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-124">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-125">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-126">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-126">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-127">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-128">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="af59f-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-129">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-130">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-131">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-131">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-132">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-133">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="af59f-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-134">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-135">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-136">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-136">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-137">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-138">Exempel 5: skapa en post uppsättning av typen NS</span><span class="sxs-lookup"><span data-stu-id="af59f-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-139">Det här kommandot skapar en **post mängd** med namnet ns1 i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-140">Post uppsättningen är av typen NS och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-141">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-141">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-142">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-143">Exempel 6: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="af59f-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="af59f-144">Det här kommandot skapar en **post mängd** som heter 4 i zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="af59f-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="af59f-145">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="af59f-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-146">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-146">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-147">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-148">Exempel 7: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="af59f-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-149">Det här kommandot skapar en **post uppsättning** med namnet _sip. _ TCP i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-150">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-151">Den innehåller en enda DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="af59f-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="af59f-152">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="af59f-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="af59f-153">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-154">Exempel 8: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="af59f-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-155">Det här kommandot skapar en **post mängd** som heter text i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-156">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="af59f-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-157">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="af59f-157">It contains a single DNS record.</span></span>
<span data-ttu-id="af59f-158">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-159">Exempel 9: skapa en post mängd vid Zone Apex</span><span class="sxs-lookup"><span data-stu-id="af59f-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-160">Det här kommandot skapar en **post mängd** vid Apex (eller roten) för zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="af59f-161">Det här är post uppsättningens namn till "@" (inklusive dubbel citat tecken).</span><span class="sxs-lookup"><span data-stu-id="af59f-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="af59f-162">Du kan inte skapa CNAME-poster i spetsen av en zon.</span><span class="sxs-lookup"><span data-stu-id="af59f-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="af59f-163">Det här är ett villkor för DNS-standarden; Det är inte en begränsning för Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="af59f-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="af59f-164">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-165">Exempel 10: skapa en post uppsättning med jokertecken</span><span class="sxs-lookup"><span data-stu-id="af59f-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af59f-166">Det här kommandot skapar en **post mängd** som heter \* i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-167">Det här är en post uppsättning med jokertecken.</span><span class="sxs-lookup"><span data-stu-id="af59f-167">This is a wildcard record set.</span></span>
<span data-ttu-id="af59f-168">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="af59f-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af59f-169">Exempel 11: skapa en tom post uppsättning</span><span class="sxs-lookup"><span data-stu-id="af59f-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="af59f-170">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="af59f-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af59f-171">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="af59f-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af59f-172">Det här är en tom post uppsättning som fungerar som en plats hållare som du senare kan lägga till poster i.</span><span class="sxs-lookup"><span data-stu-id="af59f-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="af59f-173">Exempel 12: skapa en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="af59f-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="af59f-174">Det här kommandot skapar en **post mängd**.</span><span class="sxs-lookup"><span data-stu-id="af59f-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="af59f-175">Med parametern *Overwrite* ser du till att den här post uppsättningen skriver över en befintlig post uppsättning med samma namn och typ (befintliga poster i den post uppsättningen förloras).</span><span class="sxs-lookup"><span data-stu-id="af59f-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="af59f-176">Alternativet *Confirm* med ett värde för $false inaktiverar uppmaningen.</span><span class="sxs-lookup"><span data-stu-id="af59f-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="af59f-177">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af59f-177">PARAMETERS</span></span>

### <span data-ttu-id="af59f-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af59f-178">-DefaultProfile</span></span>
<span data-ttu-id="af59f-179">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af59f-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af59f-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="af59f-180">-DnsRecords</span></span>
<span data-ttu-id="af59f-181">Anger matrisen för de DNS-poster som ska ingå i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="af59f-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="af59f-182">Du kan använda New-AzDnsRecordConfig cmdlet för att skapa DNS-postobjekt.</span><span class="sxs-lookup"><span data-stu-id="af59f-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="af59f-183">Se exemplen för mer information.</span><span class="sxs-lookup"><span data-stu-id="af59f-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="af59f-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="af59f-184">-Metadata</span></span>
<span data-ttu-id="af59f-185">Anger en matris med metadata som ska kopplas till post mängden.</span><span class="sxs-lookup"><span data-stu-id="af59f-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="af59f-186">Metadata anges med namn-värde-par som representeras som hash-tabeller, till exempel @ {"avd" = "shopping"; " kuvert "=" produktion "}.</span><span class="sxs-lookup"><span data-stu-id="af59f-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="af59f-187">-Namn</span><span class="sxs-lookup"><span data-stu-id="af59f-187">-Name</span></span>
<span data-ttu-id="af59f-188">Anger namnet på den **post mängd** som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="af59f-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="af59f-189">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="af59f-189">-Overwrite</span></span>
<span data-ttu-id="af59f-190">Anger att denna cmdlet skriver över angiven **post mängd** om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="af59f-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="af59f-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="af59f-191">-RecordType</span></span>
<span data-ttu-id="af59f-192">Anger vilken typ av DNS-post som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="af59f-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="af59f-193">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="af59f-193">Valid values are:</span></span>
- <span data-ttu-id="af59f-194">Kallas</span><span class="sxs-lookup"><span data-stu-id="af59f-194">A</span></span>
- <span data-ttu-id="af59f-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="af59f-195">AAAA</span></span>
- <span data-ttu-id="af59f-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="af59f-196">CNAME</span></span>
- <span data-ttu-id="af59f-197">MX</span><span class="sxs-lookup"><span data-stu-id="af59f-197">MX</span></span>
- <span data-ttu-id="af59f-198">NS</span><span class="sxs-lookup"><span data-stu-id="af59f-198">NS</span></span>
- <span data-ttu-id="af59f-199">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="af59f-199">PTR</span></span>
- <span data-ttu-id="af59f-200">SRV</span><span class="sxs-lookup"><span data-stu-id="af59f-200">SRV</span></span>
- <span data-ttu-id="af59f-201">TXT SOA-poster skapas automatiskt när zonen skapas och kan inte skapas manuellt.</span><span class="sxs-lookup"><span data-stu-id="af59f-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="af59f-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af59f-202">-ResourceGroupName</span></span>
<span data-ttu-id="af59f-203">Anger den resurs grupp som innehåller DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="af59f-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="af59f-204">Du måste också ange *Zonnamn* -parametern för att ange zonnamn.</span><span class="sxs-lookup"><span data-stu-id="af59f-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="af59f-205">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="af59f-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af59f-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="af59f-206">-TargetResourceId</span></span>
<span data-ttu-id="af59f-207">Resurs-ID för alias</span><span class="sxs-lookup"><span data-stu-id="af59f-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="af59f-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="af59f-208">-Ttl</span></span>
<span data-ttu-id="af59f-209">Anger TTL-värdet (Time to Live) för DNS-postuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="af59f-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="af59f-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="af59f-210">-Zone</span></span>
<span data-ttu-id="af59f-211">Anger den DnsZone där **post mängden** ska skapas.</span><span class="sxs-lookup"><span data-stu-id="af59f-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="af59f-212">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="af59f-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="af59f-213">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="af59f-213">-ZoneName</span></span>
<span data-ttu-id="af59f-214">Anger namnet på den zon där **post mängden** ska skapas.</span><span class="sxs-lookup"><span data-stu-id="af59f-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="af59f-215">Du måste också ange resurs gruppen som innehåller zonen med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="af59f-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="af59f-216">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="af59f-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af59f-217">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af59f-217">-Confirm</span></span>
<span data-ttu-id="af59f-218">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af59f-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af59f-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af59f-219">-WhatIf</span></span>
<span data-ttu-id="af59f-220">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af59f-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af59f-221">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af59f-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af59f-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af59f-222">CommonParameters</span></span>
<span data-ttu-id="af59f-223">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af59f-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af59f-224">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af59f-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af59f-225">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af59f-225">INPUTS</span></span>

### <span data-ttu-id="af59f-226">System. String</span><span class="sxs-lookup"><span data-stu-id="af59f-226">System.String</span></span>

### <span data-ttu-id="af59f-227">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="af59f-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="af59f-228">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="af59f-228">System.UInt32</span></span>

### <span data-ttu-id="af59f-229">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="af59f-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="af59f-230">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="af59f-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="af59f-231">Microsoft. Azure. kommando. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="af59f-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="af59f-232">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af59f-232">OUTPUTS</span></span>

### <span data-ttu-id="af59f-233">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af59f-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="af59f-234">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af59f-234">NOTES</span></span>
<span data-ttu-id="af59f-235">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af59f-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="af59f-236">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="af59f-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="af59f-237">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="af59f-237">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="af59f-238">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af59f-238">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="af59f-239">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af59f-239">RELATED LINKS</span></span>

[<span data-ttu-id="af59f-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="af59f-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="af59f-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af59f-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="af59f-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="af59f-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="af59f-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af59f-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="af59f-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af59f-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
