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
# <span data-ttu-id="431b7-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="431b7-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="431b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="431b7-102">SYNOPSIS</span></span>
<span data-ttu-id="431b7-103">Skapar ett nytt lokalt DNS-postobjekt.</span><span class="sxs-lookup"><span data-stu-id="431b7-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="431b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="431b7-104">SYNTAX</span></span>

### <span data-ttu-id="431b7-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="431b7-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="431b7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="431b7-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="431b7-107">Ns</span><span class="sxs-lookup"><span data-stu-id="431b7-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="431b7-108">MX</span><span class="sxs-lookup"><span data-stu-id="431b7-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="431b7-109">Resurspost</span><span class="sxs-lookup"><span data-stu-id="431b7-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="431b7-110">Txt</span><span class="sxs-lookup"><span data-stu-id="431b7-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="431b7-111">SRV</span><span class="sxs-lookup"><span data-stu-id="431b7-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="431b7-112">CName</span><span class="sxs-lookup"><span data-stu-id="431b7-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="431b7-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="431b7-113">DESCRIPTION</span></span>
<span data-ttu-id="431b7-114">Cmdleten **New-AzureRmDnsRecordConfig** skapar ett lokalt **DnsRecord** -objekt.</span><span class="sxs-lookup"><span data-stu-id="431b7-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="431b7-115">En matris med dessa objekt överförs till New-AzureRmDnsRecordSet cmdlet med parametern *DnsRecords* för att ange vilka poster som ska skapas i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="431b7-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="431b7-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="431b7-116">EXAMPLES</span></span>

### <span data-ttu-id="431b7-117">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="431b7-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="431b7-118">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-119">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="431b7-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-120">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="431b7-121">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="431b7-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-122">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-123">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-124">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-124">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-125">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-126">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="431b7-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-127">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-128">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-129">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-129">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-130">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-131">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="431b7-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-132">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-133">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-134">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-134">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-135">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-136">Exempel 5: skapa en post uppsättning av typen NS</span><span class="sxs-lookup"><span data-stu-id="431b7-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-137">Det här kommandot skapar en **post mängd** med namnet ns1 i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-138">Post uppsättningen är av typen NS och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-139">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-139">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-140">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-141">Exempel 6: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="431b7-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="431b7-142">Det här kommandot skapar en **post mängd** som heter 4 i zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="431b7-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="431b7-143">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="431b7-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-144">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-144">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-145">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-146">Exempel 7: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="431b7-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-147">Det här kommandot skapar en **post uppsättning** med namnet _sip. _ TCP i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-148">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-149">Den innehåller en enda DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="431b7-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="431b7-150">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="431b7-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="431b7-151">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="431b7-152">Exempel 8: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="431b7-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="431b7-153">Det här kommandot skapar en **post mängd** som heter text i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="431b7-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="431b7-154">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="431b7-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="431b7-155">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-155">It contains a single DNS record.</span></span>

<span data-ttu-id="431b7-156">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="431b7-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="431b7-157">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="431b7-157">PARAMETERS</span></span>

### <span data-ttu-id="431b7-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="431b7-158">-Cname</span></span>
<span data-ttu-id="431b7-159">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="431b7-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="431b7-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="431b7-160">-Exchange</span></span>
<span data-ttu-id="431b7-161">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="431b7-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="431b7-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="431b7-162">-Ipv4Address</span></span>
<span data-ttu-id="431b7-163">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="431b7-164">-IPv6</span><span class="sxs-lookup"><span data-stu-id="431b7-164">-Ipv6Address</span></span>
<span data-ttu-id="431b7-165">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-165">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="431b7-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="431b7-166">-Nsdname</span></span>
<span data-ttu-id="431b7-167">Anger namnet Server namn för en namnserver post (NS).</span><span class="sxs-lookup"><span data-stu-id="431b7-167">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="431b7-168">-Port</span><span class="sxs-lookup"><span data-stu-id="431b7-168">-Port</span></span>
<span data-ttu-id="431b7-169">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="431b7-169">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="431b7-170">-Preferens</span><span class="sxs-lookup"><span data-stu-id="431b7-170">-Preference</span></span>
<span data-ttu-id="431b7-171">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-171">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="431b7-172">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="431b7-172">-Priority</span></span>
<span data-ttu-id="431b7-173">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-173">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="431b7-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="431b7-174">-Ptrdname</span></span>
<span data-ttu-id="431b7-175">Anger mål domän namnet för en pekarresurspost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="431b7-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="431b7-176">-Mål</span><span class="sxs-lookup"><span data-stu-id="431b7-176">-Target</span></span>
<span data-ttu-id="431b7-177">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-177">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="431b7-178">-Värde</span><span class="sxs-lookup"><span data-stu-id="431b7-178">-Value</span></span>
<span data-ttu-id="431b7-179">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-179">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="431b7-180">-Vikt</span><span class="sxs-lookup"><span data-stu-id="431b7-180">-Weight</span></span>
<span data-ttu-id="431b7-181">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="431b7-181">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="431b7-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431b7-182">CommonParameters</span></span>
<span data-ttu-id="431b7-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="431b7-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431b7-184">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="431b7-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431b7-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="431b7-185">INPUTS</span></span>

### <span data-ttu-id="431b7-186">Ingen.</span><span class="sxs-lookup"><span data-stu-id="431b7-186">None.</span></span>

## <span data-ttu-id="431b7-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="431b7-187">OUTPUTS</span></span>

### <span data-ttu-id="431b7-188">Microsoft. Azure. commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="431b7-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="431b7-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="431b7-189">NOTES</span></span>

## <span data-ttu-id="431b7-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="431b7-190">RELATED LINKS</span></span>

[<span data-ttu-id="431b7-191">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="431b7-191">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="431b7-192">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="431b7-192">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="431b7-193">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="431b7-193">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
