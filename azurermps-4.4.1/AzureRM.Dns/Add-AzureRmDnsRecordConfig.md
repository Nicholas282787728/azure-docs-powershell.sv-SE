---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 65ab77c7ad94224e3ab2c72072834c43ef1434a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757298"
---
# <span data-ttu-id="e359c-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e359c-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="e359c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e359c-102">SYNOPSIS</span></span>
<span data-ttu-id="e359c-103">Lägger till en DNS-post till ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="e359c-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e359c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e359c-104">SYNTAX</span></span>

### <span data-ttu-id="e359c-105">Kallas</span><span class="sxs-lookup"><span data-stu-id="e359c-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="e359c-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-107">NS</span><span class="sxs-lookup"><span data-stu-id="e359c-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-108">MX</span><span class="sxs-lookup"><span data-stu-id="e359c-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-109">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="e359c-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-110">TXT</span><span class="sxs-lookup"><span data-stu-id="e359c-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e359c-111">SRV</span><span class="sxs-lookup"><span data-stu-id="e359c-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e359c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="e359c-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e359c-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e359c-113">DESCRIPTION</span></span>
<span data-ttu-id="e359c-114">Cmdleten **Add-AzureRmDnsRecordConfig** lägger till en DNS-post (Domain Name System) i ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e359c-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="e359c-115">Objektet **Recordset** är ett offlineobjekt och ändringar i det påverkar inte DNS-svaren förrän efter att du kört Set-AzureRmDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e359c-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="e359c-116">SOA-poster skapas när en DNS-zon skapas och tas bort när DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="e359c-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="e359c-117">Du kan inte lägga till eller ta bort SOA-poster, men du kan redigera dem.</span><span class="sxs-lookup"><span data-stu-id="e359c-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="e359c-118">Du kan överföra **Recordset** -objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e359c-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="e359c-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e359c-119">EXAMPLES</span></span>

### <span data-ttu-id="e359c-120">Exempel 1: lägga till en post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-121">I det här exemplet läggs en A-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="e359c-122">Exempel 2: lägga till en AAAA-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-123">I det här exemplet läggs en AAAA-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="e359c-124">Exempel 3: lägga till en CNAME-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-125">I det här exemplet läggs en CNAME-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="e359c-126">Eftersom en CNAME-postuppsättning kan innehålla högst en post måste den först vara en tom post uppsättning eller befintliga poster måste tas bort med Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="e359c-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="e359c-127">Exempel 4: lägga till en MX-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-128">I det här exemplet läggs en MX-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="e359c-129">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="e359c-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="e359c-130">Exempel 5: lägga till en NS-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-131">I det här exemplet läggs en NS-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="e359c-132">Exempel 6: lägga till en PTR-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-133">I det här exemplet läggs en PTR-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="e359c-134">Exempel 7: lägga till en SRV-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-135">I det här exemplet läggs en SRV-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="e359c-136">Exempel 8: lägga till en TXT-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="e359c-137">I det här exemplet läggs en TXT-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e359c-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="e359c-138">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e359c-138">PARAMETERS</span></span>

### <span data-ttu-id="e359c-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="e359c-139">-Cname</span></span>
<span data-ttu-id="e359c-140">Anger domän namnet för en CNAME-post (kanoniskt namn).</span><span class="sxs-lookup"><span data-stu-id="e359c-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="e359c-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="e359c-141">-Exchange</span></span>
<span data-ttu-id="e359c-142">Anger namnet på e-postservern för en e-postpost (MX).</span><span class="sxs-lookup"><span data-stu-id="e359c-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="e359c-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="e359c-143">-Ipv4Address</span></span>
<span data-ttu-id="e359c-144">Anger en IPv4-adress för en A-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="e359c-145">-IPv6</span><span class="sxs-lookup"><span data-stu-id="e359c-145">-Ipv6Address</span></span>
<span data-ttu-id="e359c-146">Anger en IPv6-adress för en AAAA-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="e359c-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="e359c-147">-Nsdname</span></span>
<span data-ttu-id="e359c-148">Anger namnet Server namn för en namnserver post (NS).</span><span class="sxs-lookup"><span data-stu-id="e359c-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="e359c-149">-Port</span><span class="sxs-lookup"><span data-stu-id="e359c-149">-Port</span></span>
<span data-ttu-id="e359c-150">Anger en SRV-post (service port).</span><span class="sxs-lookup"><span data-stu-id="e359c-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="e359c-151">-Preferens</span><span class="sxs-lookup"><span data-stu-id="e359c-151">-Preference</span></span>
<span data-ttu-id="e359c-152">Anger preferensen för en MX-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="e359c-153">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="e359c-153">-Priority</span></span>
<span data-ttu-id="e359c-154">Anger prioriteten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="e359c-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="e359c-155">-Ptrdname</span></span>
<span data-ttu-id="e359c-156">Anger mål domän namnet för en pekarresurspost (PTR-post).</span><span class="sxs-lookup"><span data-stu-id="e359c-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="e359c-157">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e359c-157">-RecordSet</span></span>
<span data-ttu-id="e359c-158">Anger det **Recordset** -objekt som ska redige ras.</span><span class="sxs-lookup"><span data-stu-id="e359c-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="e359c-159">-Mål</span><span class="sxs-lookup"><span data-stu-id="e359c-159">-Target</span></span>
<span data-ttu-id="e359c-160">Anger målet för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="e359c-161">-Värde</span><span class="sxs-lookup"><span data-stu-id="e359c-161">-Value</span></span>
<span data-ttu-id="e359c-162">Anger värdet för en TXT-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="e359c-163">-Vikt</span><span class="sxs-lookup"><span data-stu-id="e359c-163">-Weight</span></span>
<span data-ttu-id="e359c-164">Anger vikten för en SRV-post.</span><span class="sxs-lookup"><span data-stu-id="e359c-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="e359c-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e359c-165">-DefaultProfile</span></span>
<span data-ttu-id="e359c-166">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e359c-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e359c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e359c-167">CommonParameters</span></span>
<span data-ttu-id="e359c-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e359c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e359c-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e359c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e359c-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e359c-170">INPUTS</span></span>

### <span data-ttu-id="e359c-171">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e359c-171">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="e359c-172">Du kan **göra en pipe** till den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e359c-172">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="e359c-173">Det här är en frånkopplad **post uppsättning** och ändringar i den ändrar inte DNS-svar förrän efter att du kört Set-AzureRmDnsRecordSet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e359c-173">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="e359c-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e359c-174">OUTPUTS</span></span>

### <span data-ttu-id="e359c-175">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e359c-175">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="e359c-176">Denna cmdlet returnerar det ändrade **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="e359c-176">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="e359c-177">Dessutom ändras objektet som skickades direkt.</span><span class="sxs-lookup"><span data-stu-id="e359c-177">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="e359c-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e359c-178">NOTES</span></span>

## <span data-ttu-id="e359c-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e359c-179">RELATED LINKS</span></span>

[<span data-ttu-id="e359c-180">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e359c-180">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="e359c-181">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e359c-181">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="e359c-182">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e359c-182">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
