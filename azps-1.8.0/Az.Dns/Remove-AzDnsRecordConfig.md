---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: acf81459fd62e3f86c8e4ad02bfdefd0055db270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754120"
---
# <span data-ttu-id="20da5-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="20da5-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="20da5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20da5-102">SYNOPSIS</span></span>
<span data-ttu-id="20da5-103">Tar bort en DNS-post från ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="20da5-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="20da5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20da5-104">SYNTAX</span></span>

### <span data-ttu-id="20da5-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="20da5-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20da5-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="20da5-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20da5-107">NS</span><span class="sxs-lookup"><span data-stu-id="20da5-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20da5-108">MX</span><span class="sxs-lookup"><span data-stu-id="20da5-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20da5-109">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="20da5-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20da5-110">TXT</span><span class="sxs-lookup"><span data-stu-id="20da5-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20da5-111">SRV</span><span class="sxs-lookup"><span data-stu-id="20da5-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20da5-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="20da5-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20da5-113">Caa</span><span class="sxs-lookup"><span data-stu-id="20da5-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20da5-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20da5-114">DESCRIPTION</span></span>
<span data-ttu-id="20da5-115">Cmdleten **Remove-AzDnsRecordConfig** tar bort en DNS-post (Domain Name System) från en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="20da5-116">Objektet **Recordset** är ett offlineobjekt och ändringar i det påverkar inte DNS-svaren förrän efter att du kört Set-AzDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20da5-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="20da5-117">Om du vill ta bort en post måste alla fält för den post typen matcha exakt.</span><span class="sxs-lookup"><span data-stu-id="20da5-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="20da5-118">Du kan inte lägga till eller ta bort SOA-poster.</span><span class="sxs-lookup"><span data-stu-id="20da5-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="20da5-119">SOA-poster skapas automatiskt när en DNS-zon skapas och tas bort automatiskt när DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="20da5-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="20da5-120">Du kan överföra **Recordset** -objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="20da5-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="20da5-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20da5-121">EXAMPLES</span></span>

### <span data-ttu-id="20da5-122">Exempel 1: ta bort en post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-123">I det här exemplet tas en post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="20da5-124">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="20da5-125">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-126">Exempel 2: ta bort en AAAA-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-127">I det här exemplet tas en AAAA-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="20da5-128">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="20da5-129">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-130">Exempel 3: ta bort en CNAME-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-131">I det här exemplet tas en CNAME-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="20da5-132">Eftersom en CNAME-postuppsättning kan innehålla högst en post är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="20da5-133">Exempel 4: ta bort en MX-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-134">I det här exemplet tas en MX-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="20da5-135">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="20da5-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="20da5-136">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="20da5-137">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-138">Exempel 5: ta bort en NS-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-139">I det här exemplet tas en NS-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="20da5-140">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="20da5-141">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-142">Exempel 6: ta bort en PTR-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-143">I det här exemplet tas en PTR-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="20da5-144">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="20da5-145">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-146">Exempel 7: ta bort en SRV-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-147">I det här exemplet tas en SRV-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="20da5-148">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="20da5-149">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="20da5-150">Exempel 8: ta bort en TXT-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="20da5-151">I det här exemplet tas en TXT-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="20da5-152">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="20da5-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="20da5-153">Om du bara vill ta bort en post uppsättning, se Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="20da5-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="20da5-154">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20da5-154">PARAMETERS</span></span>

### <span data-ttu-id="20da5-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="20da5-155">-CaaFlags</span></span>
<span data-ttu-id="20da5-156">Flaggorna för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="20da5-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="20da5-157">Måste vara ett tal mellan 0 och 255.</span><span class="sxs-lookup"><span data-stu-id="20da5-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="20da5-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="20da5-158">-CaaTag</span></span>
<span data-ttu-id="20da5-159">Taggnings fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="20da5-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="20da5-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="20da5-160">-CaaValue</span></span>
<span data-ttu-id="20da5-161">Värde fältet för den CAA-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="20da5-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="20da5-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="20da5-162">-Cname</span></span>
<span data-ttu-id="20da5-163">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="20da5-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="20da5-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20da5-164">-DefaultProfile</span></span>
<span data-ttu-id="20da5-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20da5-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20da5-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="20da5-166">-Exchange</span></span>
<span data-ttu-id="20da5-167">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="20da5-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="20da5-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="20da5-168">-Ipv4Address</span></span>
<span data-ttu-id="20da5-169">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="20da5-170">-IPv6</span><span class="sxs-lookup"><span data-stu-id="20da5-170">-Ipv6Address</span></span>
<span data-ttu-id="20da5-171">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="20da5-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="20da5-172">-Nsdname</span></span>
<span data-ttu-id="20da5-173">Anger namnserver posten för namnserver (NS).</span><span class="sxs-lookup"><span data-stu-id="20da5-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="20da5-174">-Port</span><span class="sxs-lookup"><span data-stu-id="20da5-174">-Port</span></span>
<span data-ttu-id="20da5-175">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="20da5-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="20da5-176">-Preferens</span><span class="sxs-lookup"><span data-stu-id="20da5-176">-Preference</span></span>
<span data-ttu-id="20da5-177">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="20da5-178">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="20da5-178">-Priority</span></span>
<span data-ttu-id="20da5-179">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="20da5-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="20da5-180">-Ptrdname</span></span>
<span data-ttu-id="20da5-181">Anger mål domän namnet för en pekarpost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="20da5-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="20da5-182">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="20da5-182">-RecordSet</span></span>
<span data-ttu-id="20da5-183">Anger det **Recordset** -objekt som innehåller posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="20da5-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="20da5-184">-Mål</span><span class="sxs-lookup"><span data-stu-id="20da5-184">-Target</span></span>
<span data-ttu-id="20da5-185">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="20da5-186">-Värde</span><span class="sxs-lookup"><span data-stu-id="20da5-186">-Value</span></span>
<span data-ttu-id="20da5-187">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="20da5-188">-Vikt</span><span class="sxs-lookup"><span data-stu-id="20da5-188">-Weight</span></span>
<span data-ttu-id="20da5-189">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="20da5-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="20da5-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20da5-190">CommonParameters</span></span>
<span data-ttu-id="20da5-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20da5-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20da5-192">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20da5-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20da5-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20da5-193">INPUTS</span></span>

### <span data-ttu-id="20da5-194">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="20da5-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="20da5-195">System. String</span><span class="sxs-lookup"><span data-stu-id="20da5-195">System.String</span></span>

### <span data-ttu-id="20da5-196">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="20da5-196">System.UInt16</span></span>

### <span data-ttu-id="20da5-197">System. byte</span><span class="sxs-lookup"><span data-stu-id="20da5-197">System.Byte</span></span>

## <span data-ttu-id="20da5-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20da5-198">OUTPUTS</span></span>

### <span data-ttu-id="20da5-199">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="20da5-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="20da5-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20da5-200">NOTES</span></span>

## <span data-ttu-id="20da5-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20da5-201">RELATED LINKS</span></span>

[<span data-ttu-id="20da5-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="20da5-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="20da5-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="20da5-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="20da5-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="20da5-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
