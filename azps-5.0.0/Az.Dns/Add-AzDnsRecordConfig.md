---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271950"
---
# <span data-ttu-id="686d4-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="686d4-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="686d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="686d4-102">SYNOPSIS</span></span>
<span data-ttu-id="686d4-103">Lägger till en DNS-post till ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="686d4-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="686d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="686d4-104">SYNTAX</span></span>

### <span data-ttu-id="686d4-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="686d4-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686d4-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="686d4-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686d4-107">NS</span><span class="sxs-lookup"><span data-stu-id="686d4-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="686d4-108">MX</span><span class="sxs-lookup"><span data-stu-id="686d4-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686d4-109">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="686d4-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="686d4-110">TXT</span><span class="sxs-lookup"><span data-stu-id="686d4-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="686d4-111">SRV</span><span class="sxs-lookup"><span data-stu-id="686d4-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686d4-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="686d4-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="686d4-113">Caa</span><span class="sxs-lookup"><span data-stu-id="686d4-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="686d4-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="686d4-114">DESCRIPTION</span></span>
<span data-ttu-id="686d4-115">Cmdleten **Add-AzDnsRecordConfig** lägger till en DNS-post (Domain Name System) i ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="686d4-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="686d4-116">Objektet **Recordset** är ett offlineobjekt och ändringar i det påverkar inte DNS-svaren förrän efter att du kört Set-AzDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="686d4-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="686d4-117">SOA-poster skapas när en DNS-zon skapas och tas bort när DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="686d4-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="686d4-118">Du kan inte lägga till eller ta bort SOA-poster, men du kan redigera dem.</span><span class="sxs-lookup"><span data-stu-id="686d4-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="686d4-119">Du kan överföra **Recordset** -objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="686d4-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="686d4-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="686d4-120">EXAMPLES</span></span>

### <span data-ttu-id="686d4-121">Exempel 1: lägga till en post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-122">I det här exemplet läggs en A-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="686d4-123">Exempel 2: lägga till en AAAA-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-124">I det här exemplet läggs en AAAA-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="686d4-125">Exempel 3: lägga till en CNAME-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-126">I det här exemplet läggs en CNAME-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="686d4-127">Eftersom en CNAME-postuppsättning kan innehålla högst en post måste den först vara en tom post uppsättning eller befintliga poster måste tas bort med Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="686d4-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="686d4-128">Exempel 4: lägga till en MX-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-129">I det här exemplet läggs en MX-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="686d4-130">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="686d4-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="686d4-131">Exempel 5: lägga till en NS-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-132">I det här exemplet läggs en NS-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="686d4-133">Exempel 6: lägga till en PTR-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-134">I det här exemplet läggs en PTR-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="686d4-135">Exempel 7: lägga till en SRV-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-136">I det här exemplet läggs en SRV-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="686d4-137">Exempel 8: lägga till en TXT-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="686d4-138">I det här exemplet läggs en TXT-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="686d4-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="686d4-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="686d4-139">PARAMETERS</span></span>

### <span data-ttu-id="686d4-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="686d4-140">-CaaFlags</span></span>
<span data-ttu-id="686d4-141">Flaggorna för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="686d4-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="686d4-142">Måste vara ett tal mellan 0 och 255.</span><span class="sxs-lookup"><span data-stu-id="686d4-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="686d4-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="686d4-143">-CaaTag</span></span>
<span data-ttu-id="686d4-144">Taggnings fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="686d4-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="686d4-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="686d4-145">-CaaValue</span></span>
<span data-ttu-id="686d4-146">Värde fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="686d4-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="686d4-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="686d4-147">-Cname</span></span>
<span data-ttu-id="686d4-148">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="686d4-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686d4-149">-DefaultProfile</span></span>
<span data-ttu-id="686d4-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="686d4-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="686d4-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="686d4-151">-Exchange</span></span>
<span data-ttu-id="686d4-152">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="686d4-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="686d4-153">-Ipv4Address</span></span>
<span data-ttu-id="686d4-154">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="686d4-155">-IPv6</span><span class="sxs-lookup"><span data-stu-id="686d4-155">-Ipv6Address</span></span>
<span data-ttu-id="686d4-156">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="686d4-157">-Nsdname</span></span>
<span data-ttu-id="686d4-158">Anger namnet Server namn för en namnserver post (NS).</span><span class="sxs-lookup"><span data-stu-id="686d4-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-159">-Port</span><span class="sxs-lookup"><span data-stu-id="686d4-159">-Port</span></span>
<span data-ttu-id="686d4-160">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="686d4-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-161">-Preferens</span><span class="sxs-lookup"><span data-stu-id="686d4-161">-Preference</span></span>
<span data-ttu-id="686d4-162">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-163">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="686d4-163">-Priority</span></span>
<span data-ttu-id="686d4-164">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="686d4-165">-Ptrdname</span></span>
<span data-ttu-id="686d4-166">Anger mål domän namnet för en pekarresurspost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="686d4-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-167">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="686d4-167">-RecordSet</span></span>
<span data-ttu-id="686d4-168">Anger det **Recordset** -objekt som ska redige ras.</span><span class="sxs-lookup"><span data-stu-id="686d4-168">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-169">-Mål</span><span class="sxs-lookup"><span data-stu-id="686d4-169">-Target</span></span>
<span data-ttu-id="686d4-170">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-171">-Värde</span><span class="sxs-lookup"><span data-stu-id="686d4-171">-Value</span></span>
<span data-ttu-id="686d4-172">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-173">-Vikt</span><span class="sxs-lookup"><span data-stu-id="686d4-173">-Weight</span></span>
<span data-ttu-id="686d4-174">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="686d4-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="686d4-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686d4-175">CommonParameters</span></span>
<span data-ttu-id="686d4-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686d4-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686d4-177">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="686d4-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686d4-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="686d4-178">INPUTS</span></span>

### <span data-ttu-id="686d4-179">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="686d4-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="686d4-180">System. String</span><span class="sxs-lookup"><span data-stu-id="686d4-180">System.String</span></span>

### <span data-ttu-id="686d4-181">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="686d4-181">System.UInt16</span></span>

### <span data-ttu-id="686d4-182">System. byte</span><span class="sxs-lookup"><span data-stu-id="686d4-182">System.Byte</span></span>

## <span data-ttu-id="686d4-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="686d4-183">OUTPUTS</span></span>

### <span data-ttu-id="686d4-184">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="686d4-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="686d4-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="686d4-185">NOTES</span></span>

## <span data-ttu-id="686d4-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="686d4-186">RELATED LINKS</span></span>

[<span data-ttu-id="686d4-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="686d4-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="686d4-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="686d4-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="686d4-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="686d4-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
