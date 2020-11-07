---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922970"
---
# <span data-ttu-id="9926b-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9926b-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9926b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9926b-102">SYNOPSIS</span></span>
<span data-ttu-id="9926b-103">Lägger till en DNS-post till ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="9926b-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="9926b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9926b-104">SYNTAX</span></span>

### <span data-ttu-id="9926b-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="9926b-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="9926b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9926b-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="9926b-107">NS</span><span class="sxs-lookup"><span data-stu-id="9926b-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="9926b-108">MX</span><span class="sxs-lookup"><span data-stu-id="9926b-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="9926b-109">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="9926b-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="9926b-110">TXT</span><span class="sxs-lookup"><span data-stu-id="9926b-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="9926b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="9926b-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="9926b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="9926b-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="9926b-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9926b-113">DESCRIPTION</span></span>
<span data-ttu-id="9926b-114">Cmdleten **Add-AzDnsRecordConfig** lägger till en DNS-post (Domain Name System) i ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9926b-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="9926b-115">Objektet **Recordset** är ett offlineobjekt och ändringar i det påverkar inte DNS-svaren förrän efter att du kört Set-AzDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9926b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="9926b-116">SOA-poster skapas när en DNS-zon skapas och tas bort när DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="9926b-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="9926b-117">Du kan inte lägga till eller ta bort SOA-poster, men du kan redigera dem.</span><span class="sxs-lookup"><span data-stu-id="9926b-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="9926b-118">Du kan överföra **Recordset** -objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="9926b-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="9926b-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9926b-119">EXAMPLES</span></span>

### <span data-ttu-id="9926b-120">Exempel 1: lägga till en post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-121">I det här exemplet läggs en A-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="9926b-122">Exempel 2: lägga till en AAAA-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-123">I det här exemplet läggs en AAAA-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="9926b-124">Exempel 3: lägga till en CNAME-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-125">I det här exemplet läggs en CNAME-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="9926b-126">Eftersom en CNAME-postuppsättning kan innehålla högst en post måste den först vara en tom post uppsättning eller befintliga poster måste tas bort med Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="9926b-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="9926b-127">Exempel 4: lägga till en MX-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-128">I det här exemplet läggs en MX-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="9926b-129">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="9926b-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="9926b-130">Exempel 5: lägga till en NS-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-131">I det här exemplet läggs en NS-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="9926b-132">Exempel 6: lägga till en PTR-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-133">I det här exemplet läggs en PTR-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="9926b-134">Exempel 7: lägga till en SRV-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-135">I det här exemplet läggs en SRV-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="9926b-136">Exempel 8: lägga till en TXT-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="9926b-137">I det här exemplet läggs en TXT-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9926b-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="9926b-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9926b-138">PARAMETERS</span></span>

### <span data-ttu-id="9926b-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="9926b-139">-Cname</span></span>
<span data-ttu-id="9926b-140">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="9926b-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9926b-141">-Exchange</span></span>
<span data-ttu-id="9926b-142">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="9926b-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9926b-143">-Ipv4Address</span></span>
<span data-ttu-id="9926b-144">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9926b-145">-IPv6</span><span class="sxs-lookup"><span data-stu-id="9926b-145">-Ipv6Address</span></span>
<span data-ttu-id="9926b-146">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="9926b-147">-Nsdname</span></span>
<span data-ttu-id="9926b-148">Anger namnet Server namn för en namnserver post (NS).</span><span class="sxs-lookup"><span data-stu-id="9926b-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-149">-Port</span><span class="sxs-lookup"><span data-stu-id="9926b-149">-Port</span></span>
<span data-ttu-id="9926b-150">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="9926b-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-151">-Preferens</span><span class="sxs-lookup"><span data-stu-id="9926b-151">-Preference</span></span>
<span data-ttu-id="9926b-152">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-153">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="9926b-153">-Priority</span></span>
<span data-ttu-id="9926b-154">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9926b-155">-Ptrdname</span></span>
<span data-ttu-id="9926b-156">Anger mål domän namnet för en pekarresurspost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="9926b-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-157">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9926b-157">-RecordSet</span></span>
<span data-ttu-id="9926b-158">Anger det **Recordset** -objekt som ska redige ras.</span><span class="sxs-lookup"><span data-stu-id="9926b-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-159">-Mål</span><span class="sxs-lookup"><span data-stu-id="9926b-159">-Target</span></span>
<span data-ttu-id="9926b-160">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-161">-Värde</span><span class="sxs-lookup"><span data-stu-id="9926b-161">-Value</span></span>
<span data-ttu-id="9926b-162">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-163">-Vikt</span><span class="sxs-lookup"><span data-stu-id="9926b-163">-Weight</span></span>
<span data-ttu-id="9926b-164">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9926b-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9926b-165">CommonParameters</span></span>
<span data-ttu-id="9926b-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9926b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9926b-167">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9926b-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9926b-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9926b-168">INPUTS</span></span>

### <span data-ttu-id="9926b-169">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9926b-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9926b-170">Du kan **göra en pipe** till den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9926b-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="9926b-171">Det här är en frånkopplad **post uppsättning** och ändringar i den ändrar inte DNS-svar förrän efter att du kört Set-AzDnsRecordSet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9926b-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="9926b-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9926b-172">OUTPUTS</span></span>

### <span data-ttu-id="9926b-173">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9926b-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9926b-174">Denna cmdlet returnerar det ändrade **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="9926b-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="9926b-175">Dessutom ändras objektet som skickades direkt.</span><span class="sxs-lookup"><span data-stu-id="9926b-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="9926b-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9926b-176">NOTES</span></span>

## <span data-ttu-id="9926b-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9926b-177">RELATED LINKS</span></span>

[<span data-ttu-id="9926b-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9926b-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="9926b-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9926b-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="9926b-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9926b-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
