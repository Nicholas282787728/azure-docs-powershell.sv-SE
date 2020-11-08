---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919838"
---
# <span data-ttu-id="f40af-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f40af-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f40af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f40af-102">SYNOPSIS</span></span>
<span data-ttu-id="f40af-103">Lägger till en privat DNS-post till ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="f40af-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="f40af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f40af-104">SYNTAX</span></span>

### <span data-ttu-id="f40af-105">A (standard)</span><span class="sxs-lookup"><span data-stu-id="f40af-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f40af-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-107">MX</span><span class="sxs-lookup"><span data-stu-id="f40af-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-108">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="f40af-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-109">TXT</span><span class="sxs-lookup"><span data-stu-id="f40af-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f40af-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f40af-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="f40af-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f40af-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f40af-112">DESCRIPTION</span></span>
<span data-ttu-id="f40af-113">Add-AzPrivateDnsRecordConfig-cmdleten lägger till en privat DNS-post (Domain Name System) i ett RecordSet-objekt.</span><span class="sxs-lookup"><span data-stu-id="f40af-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="f40af-114">Objektet RecordSet är ett offlineobjekt och ändringar i det påverkar inte de privata DNS-svaren förrän du har kört Set-AzPrivateDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure Private DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f40af-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="f40af-115">SOA-poster skapas när en privat DNS-zon skapas och tas bort när den privata DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="f40af-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="f40af-116">Du kan inte lägga till eller ta bort SOA-poster, men du kan redigera dem.</span><span class="sxs-lookup"><span data-stu-id="f40af-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="f40af-117">Du kan överföra RecordSet-objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f40af-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f40af-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f40af-118">EXAMPLES</span></span>

### <span data-ttu-id="f40af-119">Exempel 1: lägga till en post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-120">I det här exemplet läggs en A-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="f40af-121">Exempel 2: lägga till en AAAA-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-122">I det här exemplet läggs en AAAAA-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="f40af-123">Exempel 3: lägga till en CNAME-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-124">I det här exemplet läggs en CNAME-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="f40af-125">Exempel 4: lägga till en MX-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-126">I det här exemplet läggs en MX-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="f40af-127">Exempel 5: lägga till en PTR-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-128">I det här exemplet läggs en PTR-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="f40af-129">Exempel 6: lägga till en SRV-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-130">I det här exemplet läggs en SRV-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="f40af-131">Exempel 7: lägga till en TXT-post i en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f40af-132">I det här exemplet läggs en TXT-post till i en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f40af-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="f40af-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f40af-133">PARAMETERS</span></span>

### <span data-ttu-id="f40af-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f40af-134">-Cname</span></span>
<span data-ttu-id="f40af-135">Det kanoniska namnet på CNAME-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="f40af-136">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f40af-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f40af-137">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f40af-137">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40af-138">-DefaultProfile</span></span>
<span data-ttu-id="f40af-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f40af-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f40af-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f40af-140">-Exchange</span></span>
<span data-ttu-id="f40af-141">E-postservern för MX-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="f40af-142">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f40af-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f40af-143">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f40af-143">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f40af-144">-Ipv4Address</span></span>
<span data-ttu-id="f40af-145">IPv4-adressen för den post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-145">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-146">-IPv6</span><span class="sxs-lookup"><span data-stu-id="f40af-146">-Ipv6Address</span></span>
<span data-ttu-id="f40af-147">IPv6-adressen för AAAA-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-147">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-148">-Port</span><span class="sxs-lookup"><span data-stu-id="f40af-148">-Port</span></span>
<span data-ttu-id="f40af-149">Port numret för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-149">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-150">-Preferens</span><span class="sxs-lookup"><span data-stu-id="f40af-150">-Preference</span></span>
<span data-ttu-id="f40af-151">Preferens svärdet för MX-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-151">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-152">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="f40af-152">-Priority</span></span>
<span data-ttu-id="f40af-153">Den prioriterade värde SRV-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-153">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f40af-154">-Ptrdname</span></span>
<span data-ttu-id="f40af-155">Mål värden för PTR-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="f40af-156">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f40af-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f40af-157">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f40af-157">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-158">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="f40af-158">-RecordSet</span></span>
<span data-ttu-id="f40af-159">Den post uppsättning där posten ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-160">-Mål</span><span class="sxs-lookup"><span data-stu-id="f40af-160">-Target</span></span>
<span data-ttu-id="f40af-161">Mål värden för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="f40af-162">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f40af-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f40af-163">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f40af-163">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-164">-Värde</span><span class="sxs-lookup"><span data-stu-id="f40af-164">-Value</span></span>
<span data-ttu-id="f40af-165">Textvärdet för TXT-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-165">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-166">-Vikt</span><span class="sxs-lookup"><span data-stu-id="f40af-166">-Weight</span></span>
<span data-ttu-id="f40af-167">Vikt svärdet för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f40af-167">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40af-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40af-168">CommonParameters</span></span>
<span data-ttu-id="f40af-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f40af-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40af-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f40af-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40af-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f40af-171">INPUTS</span></span>

### <span data-ttu-id="f40af-172">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f40af-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f40af-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f40af-173">OUTPUTS</span></span>

### <span data-ttu-id="f40af-174">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f40af-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f40af-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f40af-175">NOTES</span></span>

## <span data-ttu-id="f40af-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f40af-176">RELATED LINKS</span></span>