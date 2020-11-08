---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271723"
---
# <span data-ttu-id="d7313-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d7313-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d7313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7313-102">SYNOPSIS</span></span>
<span data-ttu-id="d7313-103">Skapar en post uppsättning i en privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="d7313-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="d7313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7313-104">SYNTAX</span></span>

### <span data-ttu-id="d7313-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="d7313-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7313-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="d7313-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7313-107">ID</span><span class="sxs-lookup"><span data-stu-id="d7313-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7313-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7313-108">DESCRIPTION</span></span>
<span data-ttu-id="d7313-109">New-AzPrivateDnsRecordSet-cmdleten skapar en ny DNS-post uppsättning med det angivna namnet och typen i den angivna privata zonen.</span><span class="sxs-lookup"><span data-stu-id="d7313-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="d7313-110">Ett RecordSet-objekt är en uppsättning privata DNS-poster med samma namn och typ.</span><span class="sxs-lookup"><span data-stu-id="d7313-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="d7313-111">Observera att namnet är relativt till den privata zonen och inte till det fullständigt kvalificerade namnet.</span><span class="sxs-lookup"><span data-stu-id="d7313-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="d7313-112">Parametern PrivateDnsRecord anger posterna i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="d7313-113">Denna parameter tar en matris med privata DNS-poster, byggda med New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="d7313-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="d7313-114">Du kan använda pipeline-operatorn för att skicka ett PSPrivateDnsZone-objekt till denna cmdlet, eller så kan du skicka ett PSPrivateDnsZone-objekt som parametern Zone, eller så kan du ange zonen med dess ResourceId, eller så kan du ange zonen efter namn.</span><span class="sxs-lookup"><span data-stu-id="d7313-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="d7313-115">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d7313-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d7313-116">Om det redan finns en matchande post uppsättning (samma namn och posttyp) måste du ange den överskrivnings parametern, annars skapas inte en ny post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d7313-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="d7313-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7313-117">EXAMPLES</span></span>

### <span data-ttu-id="d7313-118">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="d7313-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d7313-119">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-120">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="d7313-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-121">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="d7313-122">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="d7313-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d7313-123">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-124">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="d7313-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-125">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="d7313-126">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-127">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="d7313-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="d7313-128">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-129">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="d7313-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-130">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="d7313-131">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-132">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="d7313-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="d7313-133">Det här kommandot skapar en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-134">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="d7313-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-135">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="d7313-136">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-137">Exempel 5: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="d7313-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

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

<span data-ttu-id="d7313-138">Det här kommandot skapar en post mängd som heter 4 i den privata zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="d7313-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="d7313-139">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="d7313-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-140">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="d7313-141">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-142">Exempel 6: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="d7313-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="d7313-143">Det här kommandot skapar en post uppsättning med namnet _sip. _ TCP i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-144">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="d7313-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-145">Den innehåller en enda privat DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="d7313-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="d7313-146">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="d7313-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="d7313-147">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-148">Exempel 7: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="d7313-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="d7313-149">Det här kommandot skapar en post mängd som heter text i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-150">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="d7313-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-151">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d7313-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="d7313-152">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-153">Exempel 8: skapa en post mängd vid Zone Apex</span><span class="sxs-lookup"><span data-stu-id="d7313-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d7313-154">Det här kommandot skapar en post mängd vid Apex (eller roten) för den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="d7313-155">Det här är post uppsättningens namn till "@" (inklusive dubbel citat tecken).</span><span class="sxs-lookup"><span data-stu-id="d7313-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="d7313-156">Du kan inte skapa CNAME-poster i spetsen av en zon.</span><span class="sxs-lookup"><span data-stu-id="d7313-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="d7313-157">Det här är ett villkor för DNS-standarden; Det är inte en begränsning för Azure Private DNS.</span><span class="sxs-lookup"><span data-stu-id="d7313-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="d7313-158">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-159">Exempel 9: skapa en post uppsättning med jokertecken</span><span class="sxs-lookup"><span data-stu-id="d7313-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d7313-160">Det här kommandot skapar en post mängd som heter \* i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-161">Det här är en post uppsättning med jokertecken.</span><span class="sxs-lookup"><span data-stu-id="d7313-161">This is a wildcard record set.</span></span> <span data-ttu-id="d7313-162">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="d7313-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7313-163">Exempel 10: skapa en tom post uppsättning</span><span class="sxs-lookup"><span data-stu-id="d7313-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d7313-164">Det här kommandot skapar en post mängd som heter \* i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d7313-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="d7313-165">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="d7313-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d7313-166">Det här är en tom post uppsättning som fungerar som en plats hållare som du senare kan lägga till poster i.</span><span class="sxs-lookup"><span data-stu-id="d7313-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="d7313-167">Exempel 11: skapa en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="d7313-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="d7313-168">Det här kommandot skapar en post mängd.</span><span class="sxs-lookup"><span data-stu-id="d7313-168">This command creates a RecordSet.</span></span> <span data-ttu-id="d7313-169">Med parametern overwrite ser du till att den här post uppsättningen skriver över en befintlig post uppsättning med samma namn och typ (befintliga poster i den post uppsättningen förloras).</span><span class="sxs-lookup"><span data-stu-id="d7313-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="d7313-170">Alternativet Confirm med ett värde för $False inaktiverar uppmaningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="d7313-171">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7313-171">PARAMETERS</span></span>

### <span data-ttu-id="d7313-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7313-172">-DefaultProfile</span></span>
<span data-ttu-id="d7313-173">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7313-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7313-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d7313-174">-Metadata</span></span>
<span data-ttu-id="d7313-175">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d7313-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-176">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7313-176">-Name</span></span>
<span data-ttu-id="d7313-177">Namnet på posterna i den här post uppsättningen (i förhållande till namnet på zonen och utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="d7313-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-178">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="d7313-178">-Overwrite</span></span>
<span data-ttu-id="d7313-179">Rapportera inte om posten redan finns.</span><span class="sxs-lookup"><span data-stu-id="d7313-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="d7313-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d7313-180">-ParentResourceId</span></span>
<span data-ttu-id="d7313-181">Privat DNS-zon ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d7313-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="d7313-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="d7313-183">De privata DNS-posterna som ingår i den här post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="d7313-184">-RecordType</span></span>
<span data-ttu-id="d7313-185">Typen för privata DNS-poster i den här post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7313-186">-ResourceGroupName</span></span>
<span data-ttu-id="d7313-187">Den resurs grupp som zonen tillhör.</span><span class="sxs-lookup"><span data-stu-id="d7313-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="d7313-188">-Ttl</span></span>
<span data-ttu-id="d7313-189">TTL-värdet för alla poster i den här post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="d7313-190">-Zone</span></span>
<span data-ttu-id="d7313-191">PrivateDnsZone-objektet som representerar den zon där du vill skapa post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d7313-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-192">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="d7313-192">-ZoneName</span></span>
<span data-ttu-id="d7313-193">Den zon där du vill skapa post uppsättningen (utan att avsluta punkter).</span><span class="sxs-lookup"><span data-stu-id="d7313-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-194">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7313-194">-Confirm</span></span>
<span data-ttu-id="d7313-195">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7313-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7313-196">-WhatIf</span></span>
<span data-ttu-id="d7313-197">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7313-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7313-198">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7313-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7313-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7313-199">CommonParameters</span></span>
<span data-ttu-id="d7313-200">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7313-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7313-201">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7313-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7313-202">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7313-202">INPUTS</span></span>

### <span data-ttu-id="d7313-203">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="d7313-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="d7313-204">System. String</span><span class="sxs-lookup"><span data-stu-id="d7313-204">System.String</span></span>

## <span data-ttu-id="d7313-205">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7313-205">OUTPUTS</span></span>

### <span data-ttu-id="d7313-206">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d7313-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d7313-207">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7313-207">NOTES</span></span>

## <span data-ttu-id="d7313-208">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7313-208">RELATED LINKS</span></span>
