---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924589"
---
# <span data-ttu-id="9d14b-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d14b-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9d14b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d14b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d14b-103">Tar bort en DNS-post från ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="9d14b-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="9d14b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d14b-104">SYNTAX</span></span>

### <span data-ttu-id="9d14b-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="9d14b-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9d14b-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-107">NS</span><span class="sxs-lookup"><span data-stu-id="9d14b-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-108">MX</span><span class="sxs-lookup"><span data-stu-id="9d14b-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="9d14b-109">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="9d14b-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-110">TXT</span><span class="sxs-lookup"><span data-stu-id="9d14b-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="9d14b-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="9d14b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="9d14b-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="9d14b-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d14b-113">DESCRIPTION</span></span>
<span data-ttu-id="9d14b-114">Cmdleten **Remove-AzDnsRecordConfig** tar bort en DNS-post (Domain Name System) från en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="9d14b-115">Objektet **Recordset** är ett offlineobjekt och ändringar i det påverkar inte DNS-svaren förrän efter att du kört Set-AzDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9d14b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="9d14b-116">Om du vill ta bort en post måste alla fält för den post typen matcha exakt.</span><span class="sxs-lookup"><span data-stu-id="9d14b-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="9d14b-117">Du kan inte lägga till eller ta bort SOA-poster.</span><span class="sxs-lookup"><span data-stu-id="9d14b-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="9d14b-118">SOA-poster skapas automatiskt när en DNS-zon skapas och tas bort automatiskt när DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="9d14b-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="9d14b-119">Du kan överföra **Recordset** -objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="9d14b-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="9d14b-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d14b-120">EXAMPLES</span></span>

### <span data-ttu-id="9d14b-121">Exempel 1: ta bort en post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-122">I det här exemplet tas en post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="9d14b-123">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9d14b-124">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-125">Exempel 2: ta bort en AAAA-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-126">I det här exemplet tas en AAAA-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="9d14b-127">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9d14b-128">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-129">Exempel 3: ta bort en CNAME-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-130">I det här exemplet tas en CNAME-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="9d14b-131">Eftersom en CNAME-postuppsättning kan innehålla högst en post är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="9d14b-132">Exempel 4: ta bort en MX-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-133">I det här exemplet tas en MX-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="9d14b-134">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="9d14b-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="9d14b-135">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9d14b-136">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-137">Exempel 5: ta bort en NS-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-138">I det här exemplet tas en NS-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="9d14b-139">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9d14b-140">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-141">Exempel 6: ta bort en PTR-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-142">I det här exemplet tas en PTR-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="9d14b-143">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9d14b-144">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-145">Exempel 7: ta bort en SRV-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-146">I det här exemplet tas en SRV-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="9d14b-147">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9d14b-148">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9d14b-149">Exempel 8: ta bort en TXT-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="9d14b-150">I det här exemplet tas en TXT-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="9d14b-151">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9d14b-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9d14b-152">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="9d14b-153">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d14b-153">PARAMETERS</span></span>

### <span data-ttu-id="9d14b-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="9d14b-154">-Cname</span></span>
<span data-ttu-id="9d14b-155">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="9d14b-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="9d14b-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9d14b-156">-Exchange</span></span>
<span data-ttu-id="9d14b-157">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="9d14b-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="9d14b-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9d14b-158">-Ipv4Address</span></span>
<span data-ttu-id="9d14b-159">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9d14b-160">-IPv6</span><span class="sxs-lookup"><span data-stu-id="9d14b-160">-Ipv6Address</span></span>
<span data-ttu-id="9d14b-161">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="9d14b-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="9d14b-162">-Nsdname</span></span>
<span data-ttu-id="9d14b-163">Anger namnserver posten för namnserver (NS).</span><span class="sxs-lookup"><span data-stu-id="9d14b-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="9d14b-164">-Port</span><span class="sxs-lookup"><span data-stu-id="9d14b-164">-Port</span></span>
<span data-ttu-id="9d14b-165">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="9d14b-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="9d14b-166">-Preferens</span><span class="sxs-lookup"><span data-stu-id="9d14b-166">-Preference</span></span>
<span data-ttu-id="9d14b-167">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="9d14b-168">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="9d14b-168">-Priority</span></span>
<span data-ttu-id="9d14b-169">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="9d14b-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9d14b-170">-Ptrdname</span></span>
<span data-ttu-id="9d14b-171">Anger mål domän namnet för en pekarpost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="9d14b-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="9d14b-172">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d14b-172">-RecordSet</span></span>
<span data-ttu-id="9d14b-173">Anger det **Recordset** -objekt som innehåller posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9d14b-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="9d14b-174">-Mål</span><span class="sxs-lookup"><span data-stu-id="9d14b-174">-Target</span></span>
<span data-ttu-id="9d14b-175">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="9d14b-176">-Värde</span><span class="sxs-lookup"><span data-stu-id="9d14b-176">-Value</span></span>
<span data-ttu-id="9d14b-177">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="9d14b-178">-Vikt</span><span class="sxs-lookup"><span data-stu-id="9d14b-178">-Weight</span></span>
<span data-ttu-id="9d14b-179">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="9d14b-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="9d14b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d14b-180">CommonParameters</span></span>
<span data-ttu-id="9d14b-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d14b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d14b-182">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d14b-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d14b-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d14b-183">INPUTS</span></span>

### <span data-ttu-id="9d14b-184">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9d14b-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9d14b-185">Du kan ha ett **DnsRecordSet** -objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="9d14b-186">Det här är en frånkopplad post uppsättning och uppdateringar som inte ändras när du kör Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="9d14b-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d14b-187">OUTPUTS</span></span>

### <span data-ttu-id="9d14b-188">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9d14b-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9d14b-189">Denna cmdlet returnerar det ändrade **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="9d14b-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="9d14b-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d14b-190">NOTES</span></span>

## <span data-ttu-id="9d14b-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d14b-191">RELATED LINKS</span></span>

[<span data-ttu-id="9d14b-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d14b-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="9d14b-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9d14b-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="9d14b-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9d14b-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
