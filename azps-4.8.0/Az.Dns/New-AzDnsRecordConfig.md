---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260516"
---
# <span data-ttu-id="542f2-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="542f2-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="542f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="542f2-102">SYNOPSIS</span></span>
<span data-ttu-id="542f2-103">Skapar ett nytt lokalt DNS-postobjekt.</span><span class="sxs-lookup"><span data-stu-id="542f2-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="542f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="542f2-104">SYNTAX</span></span>

### <span data-ttu-id="542f2-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="542f2-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="542f2-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-107">Ns</span><span class="sxs-lookup"><span data-stu-id="542f2-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-108">MX</span><span class="sxs-lookup"><span data-stu-id="542f2-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="542f2-109">Resurspost</span><span class="sxs-lookup"><span data-stu-id="542f2-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-110">Txt</span><span class="sxs-lookup"><span data-stu-id="542f2-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-111">SRV</span><span class="sxs-lookup"><span data-stu-id="542f2-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-112">CName</span><span class="sxs-lookup"><span data-stu-id="542f2-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542f2-113">Caa</span><span class="sxs-lookup"><span data-stu-id="542f2-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542f2-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="542f2-114">DESCRIPTION</span></span>
<span data-ttu-id="542f2-115">Cmdleten **New-AzDnsRecordConfig** skapar ett lokalt **DnsRecord** -objekt.</span><span class="sxs-lookup"><span data-stu-id="542f2-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="542f2-116">En matris med dessa objekt överförs till New-AzDnsRecordSet cmdlet med parametern *DnsRecords* för att ange vilka poster som ska skapas i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="542f2-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="542f2-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="542f2-117">EXAMPLES</span></span>

### <span data-ttu-id="542f2-118">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="542f2-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="542f2-119">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-120">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="542f2-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-121">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="542f2-122">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="542f2-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-123">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-124">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-125">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-125">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-126">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-127">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="542f2-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-128">I det här exemplet skapas en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-129">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-130">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-130">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-131">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-132">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="542f2-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-133">Det här kommandot skapar en **post uppsättning** med namnet www i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-134">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-135">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-135">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-136">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-137">Exempel 5: skapa en post uppsättning av typen NS</span><span class="sxs-lookup"><span data-stu-id="542f2-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-138">Det här kommandot skapar en **post mängd** med namnet ns1 i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-139">Post uppsättningen är av typen NS och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-140">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-140">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-141">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-142">Exempel 6: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="542f2-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="542f2-143">Det här kommandot skapar en **post mängd** som heter 4 i zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="542f2-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="542f2-144">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="542f2-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-145">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-145">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-146">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-147">Exempel 7: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="542f2-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-148">Det här kommandot skapar en **post uppsättning** med namnet _sip. _ TCP i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-149">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-150">Den innehåller en enda DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="542f2-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="542f2-151">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="542f2-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="542f2-152">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="542f2-153">Exempel 8: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="542f2-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="542f2-154">Det här kommandot skapar en **post mängd** som heter text i zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="542f2-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="542f2-155">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="542f2-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="542f2-156">Den innehåller en enda DNS-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-156">It contains a single DNS record.</span></span>
<span data-ttu-id="542f2-157">Om du vill skapa en **post mängd** med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="542f2-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="542f2-158">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="542f2-158">PARAMETERS</span></span>

### <span data-ttu-id="542f2-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="542f2-159">-CaaFlags</span></span>
<span data-ttu-id="542f2-160">Flaggorna för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="542f2-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="542f2-161">Måste vara ett tal mellan 0 och 255.</span><span class="sxs-lookup"><span data-stu-id="542f2-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="542f2-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="542f2-162">-CaaTag</span></span>
<span data-ttu-id="542f2-163">Taggnings fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="542f2-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="542f2-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="542f2-164">-CaaValue</span></span>
<span data-ttu-id="542f2-165">Värde fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="542f2-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="542f2-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="542f2-166">-Cname</span></span>
<span data-ttu-id="542f2-167">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="542f2-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="542f2-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542f2-168">-DefaultProfile</span></span>
<span data-ttu-id="542f2-169">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="542f2-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="542f2-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="542f2-170">-Exchange</span></span>
<span data-ttu-id="542f2-171">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="542f2-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="542f2-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="542f2-172">-Ipv4Address</span></span>
<span data-ttu-id="542f2-173">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="542f2-174">-IPv6</span><span class="sxs-lookup"><span data-stu-id="542f2-174">-Ipv6Address</span></span>
<span data-ttu-id="542f2-175">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="542f2-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="542f2-176">-Nsdname</span></span>
<span data-ttu-id="542f2-177">Anger namnet Server namn för en namnserver post (NS).</span><span class="sxs-lookup"><span data-stu-id="542f2-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="542f2-178">-Port</span><span class="sxs-lookup"><span data-stu-id="542f2-178">-Port</span></span>
<span data-ttu-id="542f2-179">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="542f2-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="542f2-180">-Preferens</span><span class="sxs-lookup"><span data-stu-id="542f2-180">-Preference</span></span>
<span data-ttu-id="542f2-181">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="542f2-182">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="542f2-182">-Priority</span></span>
<span data-ttu-id="542f2-183">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="542f2-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="542f2-184">-Ptrdname</span></span>
<span data-ttu-id="542f2-185">Anger mål domän namnet för en pekarresurspost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="542f2-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="542f2-186">-Mål</span><span class="sxs-lookup"><span data-stu-id="542f2-186">-Target</span></span>
<span data-ttu-id="542f2-187">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="542f2-188">-Värde</span><span class="sxs-lookup"><span data-stu-id="542f2-188">-Value</span></span>
<span data-ttu-id="542f2-189">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="542f2-190">-Vikt</span><span class="sxs-lookup"><span data-stu-id="542f2-190">-Weight</span></span>
<span data-ttu-id="542f2-191">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="542f2-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="542f2-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542f2-192">CommonParameters</span></span>
<span data-ttu-id="542f2-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542f2-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542f2-194">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542f2-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542f2-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="542f2-195">INPUTS</span></span>

### <span data-ttu-id="542f2-196">System. String</span><span class="sxs-lookup"><span data-stu-id="542f2-196">System.String</span></span>

### <span data-ttu-id="542f2-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="542f2-197">System.UInt16</span></span>

### <span data-ttu-id="542f2-198">System. byte</span><span class="sxs-lookup"><span data-stu-id="542f2-198">System.Byte</span></span>

## <span data-ttu-id="542f2-199">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="542f2-199">OUTPUTS</span></span>

### <span data-ttu-id="542f2-200">Microsoft. Azure. commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="542f2-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="542f2-201">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="542f2-201">NOTES</span></span>

## <span data-ttu-id="542f2-202">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="542f2-202">RELATED LINKS</span></span>

[<span data-ttu-id="542f2-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="542f2-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="542f2-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="542f2-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="542f2-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="542f2-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
