---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 4ceba6333d382b48e8e93ce6c63bde9e02b8f7ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586527"
---
# <span data-ttu-id="593d9-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="593d9-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="593d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="593d9-102">SYNOPSIS</span></span>
<span data-ttu-id="593d9-103">Skapar en DNS-post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="593d9-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="593d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="593d9-104">SYNTAX</span></span>

### <span data-ttu-id="593d9-105">Fält</span><span class="sxs-lookup"><span data-stu-id="593d9-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593d9-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="593d9-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="593d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="593d9-107">DESCRIPTION</span></span>
<span data-ttu-id="593d9-108">Cmdleten **New-AzureRmDnsRecordSet** skapar en ny DNS-post (Domain Name System) med det angivna namnet och typen i den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="593d9-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="593d9-109">Ett **Recordset** -objekt är en uppsättning DNS-poster med samma namn och typ.</span><span class="sxs-lookup"><span data-stu-id="593d9-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="593d9-110">Observera att namnet är relativt till zonen och inte till det fullständigt kvalificerade namnet.</span><span class="sxs-lookup"><span data-stu-id="593d9-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="593d9-111">Parametern *DnsRecords* anger posterna i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="593d9-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="593d9-112">Den här parametern tar en matris med DNS-poster, utformad med AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="593d9-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="593d9-113">Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen efter namn.</span><span class="sxs-lookup"><span data-stu-id="593d9-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="593d9-114">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="593d9-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="593d9-115">Om det redan finns en matchande **post uppsättning** (samma namn och posttyp) måste du ange den *överskrivnings* parametern, annars skapas inte en ny **post uppsättning** .</span><span class="sxs-lookup"><span data-stu-id="593d9-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="593d9-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="593d9-116">EXAMPLES</span></span>

### <span data-ttu-id="593d9-117">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="593d9-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="593d9-118">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-119">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="593d9-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-120">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="593d9-121">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="593d9-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-122">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-123">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-124">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-124">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-125">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-126">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="593d9-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-127">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-128">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-129">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-129">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-130">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-131">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="593d9-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-132">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-133">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-134">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-134">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-135">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-136">Exempel 5: skapa en post uppsättning av typen NS</span><span class="sxs-lookup"><span data-stu-id="593d9-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-137">Det här kommandot skapar en **post mängd** med namnet ns1 i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-138">Post uppsättningen är av typen NS och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-139">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-139">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-140">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-141">Exempel 6: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="593d9-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="593d9-142">Det här kommandot skapar en **post mängd** som heter 4 i zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="593d9-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="593d9-143">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="593d9-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-144">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-144">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-145">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-146">Exempel 7: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="593d9-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-147">Det här kommandot skapar en **post uppsättning** med namnet _sip. _ TCP i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-148">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-149">Den innehåller en enda DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="593d9-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="593d9-150">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="593d9-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="593d9-151">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-152">Exempel 8: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="593d9-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-153">Det här kommandot skapar en **post mängd** som heter text i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-154">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="593d9-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-155">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="593d9-155">It contains a single DNS record.</span></span>

<span data-ttu-id="593d9-156">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-157">Exempel 9: skapa en post mängd vid Zone Apex</span><span class="sxs-lookup"><span data-stu-id="593d9-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-158">Det här kommandot skapar en **post mängd** vid Apex (eller roten) för zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="593d9-159">Det här är post uppsättningens namn till "@" (inklusive dubbel citat tecken).</span><span class="sxs-lookup"><span data-stu-id="593d9-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="593d9-160">Du kan inte skapa CNAME-poster i spetsen av en zon.</span><span class="sxs-lookup"><span data-stu-id="593d9-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="593d9-161">Det här är ett villkor för DNS-standarden; Det är inte en begränsning för Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="593d9-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="593d9-162">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-163">Exempel 10: skapa en post uppsättning med jokertecken</span><span class="sxs-lookup"><span data-stu-id="593d9-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="593d9-164">Det här kommandot skapar en **post mängd** som heter \* i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-165">Det här är en post uppsättning med jokertecken.</span><span class="sxs-lookup"><span data-stu-id="593d9-165">This is a wildcard record set.</span></span>

<span data-ttu-id="593d9-166">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="593d9-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="593d9-167">Exempel 11: skapa en tom post uppsättning</span><span class="sxs-lookup"><span data-stu-id="593d9-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="593d9-168">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="593d9-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="593d9-169">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="593d9-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="593d9-170">Det här är en tom post uppsättning som fungerar som en plats hållare som du senare kan lägga till poster i.</span><span class="sxs-lookup"><span data-stu-id="593d9-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="593d9-171">Exempel 12: skapa en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="593d9-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="593d9-172">Det här kommandot skapar en **post mängd**.</span><span class="sxs-lookup"><span data-stu-id="593d9-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="593d9-173">Med parametern *Overwrite* ser du till att den här post uppsättningen skriver över en befintlig post uppsättning med samma namn och typ (befintliga poster i den post uppsättningen förloras).</span><span class="sxs-lookup"><span data-stu-id="593d9-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="593d9-174">Alternativet *Confirm* med ett värde för $false inaktiverar uppmaningen.</span><span class="sxs-lookup"><span data-stu-id="593d9-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="593d9-175">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="593d9-175">PARAMETERS</span></span>

### <span data-ttu-id="593d9-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="593d9-176">-DnsRecords</span></span>
<span data-ttu-id="593d9-177">Anger matrisen för de DNS-poster som ska ingå i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="593d9-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="593d9-178">Du kan använda New-AzureRmDnsRecordConfig cmdlet för att skapa DNS-postobjekt.</span><span class="sxs-lookup"><span data-stu-id="593d9-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="593d9-179">Se exemplen för mer information.</span><span class="sxs-lookup"><span data-stu-id="593d9-179">See the examples for more information.</span></span>

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

### <span data-ttu-id="593d9-180">-Force</span><span class="sxs-lookup"><span data-stu-id="593d9-180">-Force</span></span>
<span data-ttu-id="593d9-181">Den här parametern är föråldrad för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="593d9-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="593d9-182">Den kommer att tas bort i en senare version.</span><span class="sxs-lookup"><span data-stu-id="593d9-182">It will be removed in a future release.</span></span>

<span data-ttu-id="593d9-183">Om du vill kontrol lera om den här cmdleten frågar dig för comfirmation använder du parametern *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="593d9-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="593d9-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="593d9-184">-Metadata</span></span>
<span data-ttu-id="593d9-185">Anger en matris med metadata som ska kopplas till post mängden.</span><span class="sxs-lookup"><span data-stu-id="593d9-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="593d9-186">Metadata anges med namn-värde-par som representeras som hash-tabeller, till exempel @ (@ {"name" = "avd"; "Värde" = "shopping"}, @ {"namn" = "kuvert"; "Värde" = "produktion"}).</span><span class="sxs-lookup"><span data-stu-id="593d9-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="593d9-187">-Namn</span><span class="sxs-lookup"><span data-stu-id="593d9-187">-Name</span></span>
<span data-ttu-id="593d9-188">Anger namnet på den **post mängd** som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="593d9-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="593d9-189">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="593d9-189">-Overwrite</span></span>
<span data-ttu-id="593d9-190">Anger att denna cmdlet skriver över angiven **post mängd** om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="593d9-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="593d9-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="593d9-191">-RecordType</span></span>
<span data-ttu-id="593d9-192">Anger vilken typ av DNS-post som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="593d9-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="593d9-193">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="593d9-193">Valid values are:</span></span>

- <span data-ttu-id="593d9-194">Kallas</span><span class="sxs-lookup"><span data-stu-id="593d9-194">A</span></span>
- <span data-ttu-id="593d9-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="593d9-195">AAAA</span></span>
- <span data-ttu-id="593d9-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="593d9-196">CNAME</span></span>
- <span data-ttu-id="593d9-197">MX</span><span class="sxs-lookup"><span data-stu-id="593d9-197">MX</span></span>
- <span data-ttu-id="593d9-198">NS</span><span class="sxs-lookup"><span data-stu-id="593d9-198">NS</span></span>
- <span data-ttu-id="593d9-199">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="593d9-199">PTR</span></span>
- <span data-ttu-id="593d9-200">SRV</span><span class="sxs-lookup"><span data-stu-id="593d9-200">SRV</span></span>
- <span data-ttu-id="593d9-201">TXT</span><span class="sxs-lookup"><span data-stu-id="593d9-201">TXT</span></span>

<span data-ttu-id="593d9-202">SOA-poster skapas automatiskt när zonen skapas och kan inte skapas manuellt.</span><span class="sxs-lookup"><span data-stu-id="593d9-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593d9-203">-ResourceGroupName</span></span>
<span data-ttu-id="593d9-204">Anger den resurs grupp som innehåller DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="593d9-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="593d9-205">Du måste också ange *Zonnamn* -parametern för att ange zonnamn.</span><span class="sxs-lookup"><span data-stu-id="593d9-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="593d9-206">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="593d9-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="593d9-207">-Ttl</span></span>
<span data-ttu-id="593d9-208">Anger TTL-värdet (Time to Live) för DNS-postuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="593d9-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="593d9-209">-Zone</span></span>
<span data-ttu-id="593d9-210">Anger den DnsZone där **post mängden** ska skapas.</span><span class="sxs-lookup"><span data-stu-id="593d9-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="593d9-211">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="593d9-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-212">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="593d9-212">-ZoneName</span></span>
<span data-ttu-id="593d9-213">Anger namnet på den zon där **post mängden** ska skapas.</span><span class="sxs-lookup"><span data-stu-id="593d9-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="593d9-214">Du måste också ange resurs gruppen som innehåller zonen med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="593d9-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="593d9-215">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="593d9-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-216">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="593d9-216">-Confirm</span></span>
<span data-ttu-id="593d9-217">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="593d9-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="593d9-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="593d9-218">-WhatIf</span></span>
<span data-ttu-id="593d9-219">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="593d9-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="593d9-220">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="593d9-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="593d9-221">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593d9-221">-DefaultProfile</span></span>
<span data-ttu-id="593d9-222">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="593d9-222">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="593d9-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593d9-223">CommonParameters</span></span>
<span data-ttu-id="593d9-224">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="593d9-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593d9-225">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="593d9-225">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593d9-226">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="593d9-226">INPUTS</span></span>

### <span data-ttu-id="593d9-227">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="593d9-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="593d9-228">Du kan ha ett DnsZone-objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="593d9-228">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="593d9-229">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="593d9-229">OUTPUTS</span></span>

### <span data-ttu-id="593d9-230">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="593d9-230">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="593d9-231">Denna cmdlet returnerar ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="593d9-231">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="593d9-232">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="593d9-232">NOTES</span></span>
<span data-ttu-id="593d9-233">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="593d9-233">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="593d9-234">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="593d9-234">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="593d9-235">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="593d9-235">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="593d9-236">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="593d9-236">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="593d9-237">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="593d9-237">RELATED LINKS</span></span>

[<span data-ttu-id="593d9-238">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="593d9-238">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="593d9-239">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="593d9-239">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="593d9-240">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="593d9-240">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="593d9-241">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="593d9-241">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="593d9-242">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="593d9-242">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
