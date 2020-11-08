---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 6653491e7ee4a60b6ad9b392895454e5ee6dc3ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090687"
---
# <span data-ttu-id="f0d57-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f0d57-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f0d57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0d57-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d57-103">Skapar ett nytt lokalt DNS-postobjekt.</span><span class="sxs-lookup"><span data-stu-id="f0d57-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="f0d57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0d57-104">SYNTAX</span></span>

### <span data-ttu-id="f0d57-105">A (standard)</span><span class="sxs-lookup"><span data-stu-id="f0d57-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d57-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f0d57-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d57-107">MX</span><span class="sxs-lookup"><span data-stu-id="f0d57-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d57-108">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="f0d57-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d57-109">TXT</span><span class="sxs-lookup"><span data-stu-id="f0d57-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d57-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f0d57-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d57-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="f0d57-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d57-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0d57-112">DESCRIPTION</span></span>
<span data-ttu-id="f0d57-113">New-AzPrivateDnsRecordConfig-cmdleten skapar ett lokalt PSPrivateDnsRecord-objekt.</span><span class="sxs-lookup"><span data-stu-id="f0d57-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="f0d57-114">En matris med dessa objekt överförs till New-AzPrivateDnsRecordSet cmdlet med parametern PrivateDnsRecord för att ange vilka poster som ska skapas i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="f0d57-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="f0d57-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0d57-115">EXAMPLES</span></span>

### <span data-ttu-id="f0d57-116">Exempel 1: skapa en post mängd av typen A</span><span class="sxs-lookup"><span data-stu-id="f0d57-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="f0d57-117">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-118">Post uppsättningen är av typen A och har TTL på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="f0d57-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-119">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="f0d57-120">Exempel 2: skapa en post mängd av typen AAAA</span><span class="sxs-lookup"><span data-stu-id="f0d57-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="f0d57-121">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-122">Post uppsättningen är av typen AAAA och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="f0d57-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-123">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="f0d57-124">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f0d57-125">Exempel 3: skapa en post uppsättning av typen CNAME</span><span class="sxs-lookup"><span data-stu-id="f0d57-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="f0d57-126">I det här exemplet skapas en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-127">Post uppsättningen är av typen CNAME och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="f0d57-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-128">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="f0d57-129">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f0d57-130">Exempel 4: skapa en post mängd av typen MX</span><span class="sxs-lookup"><span data-stu-id="f0d57-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="f0d57-131">Det här kommandot skapar en post uppsättning med namnet www i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-132">Post uppsättningen är av typen MX och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="f0d57-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-133">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="f0d57-134">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f0d57-135">Exempel 5: skapa en post uppsättning av typen PTR</span><span class="sxs-lookup"><span data-stu-id="f0d57-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="f0d57-136">Det här kommandot skapar en post mängd som heter 4 i den privata zonen 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="f0d57-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="f0d57-137">Post uppsättningen är av typen PTR och har TTL-värde på 1 timme (3600 sekunder).</span><span class="sxs-lookup"><span data-stu-id="f0d57-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-138">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="f0d57-139">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f0d57-140">Exempel 6: skapa en post uppsättning av typen SRV</span><span class="sxs-lookup"><span data-stu-id="f0d57-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="f0d57-141">Det här kommandot skapar en post uppsättning med namnet _sip. _ TCP i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-142">Post uppsättningen är av typen SRV och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="f0d57-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-143">Den innehåller en enda privat DNS-post som pekar på IP-2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="f0d57-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="f0d57-144">Tjänsten (SIP) och protokollet (TCP) har angetts som en del av post uppsättningens namn, inte som en del av postens data.</span><span class="sxs-lookup"><span data-stu-id="f0d57-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="f0d57-145">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f0d57-146">Exempel 7: skapa en post uppsättning av typen TXT</span><span class="sxs-lookup"><span data-stu-id="f0d57-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="f0d57-147">Det här kommandot skapar en post mängd som heter text i den privata zonen myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f0d57-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="f0d57-148">Post uppsättningen är av typen TXT och har TTL-värde (3600 sekunder) för 1 timme.</span><span class="sxs-lookup"><span data-stu-id="f0d57-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f0d57-149">Den innehåller en enda privat DNS-post.</span><span class="sxs-lookup"><span data-stu-id="f0d57-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="f0d57-150">Om du vill skapa en post mängd med bara en rad med pn_PowerShell_short, eller om du vill skapa en post uppsättning med flera poster, se exempel 1.</span><span class="sxs-lookup"><span data-stu-id="f0d57-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="f0d57-151">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0d57-151">PARAMETERS</span></span>

### <span data-ttu-id="f0d57-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f0d57-152">-Cname</span></span>
<span data-ttu-id="f0d57-153">Det kanoniska namnet på CNAME-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="f0d57-154">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f0d57-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f0d57-155">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f0d57-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f0d57-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d57-156">-DefaultProfile</span></span>
<span data-ttu-id="f0d57-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d57-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d57-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f0d57-158">-Exchange</span></span>
<span data-ttu-id="f0d57-159">E-postservern för MX-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="f0d57-160">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f0d57-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f0d57-161">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f0d57-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f0d57-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f0d57-162">-Ipv4Address</span></span>
<span data-ttu-id="f0d57-163">IPv4-adressen för den post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="f0d57-164">-IPv6</span><span class="sxs-lookup"><span data-stu-id="f0d57-164">-Ipv6Address</span></span>
<span data-ttu-id="f0d57-165">IPv6-adressen för AAAA-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="f0d57-166">-Port</span><span class="sxs-lookup"><span data-stu-id="f0d57-166">-Port</span></span>
<span data-ttu-id="f0d57-167">Port numret för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="f0d57-168">-Preferens</span><span class="sxs-lookup"><span data-stu-id="f0d57-168">-Preference</span></span>
<span data-ttu-id="f0d57-169">Preferens svärdet för MX-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="f0d57-170">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="f0d57-170">-Priority</span></span>
<span data-ttu-id="f0d57-171">Den prioriterade värde SRV-post som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="f0d57-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f0d57-172">-Ptrdname</span></span>
<span data-ttu-id="f0d57-173">Mål värden för PTR-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="f0d57-174">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f0d57-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f0d57-175">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f0d57-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f0d57-176">-Mål</span><span class="sxs-lookup"><span data-stu-id="f0d57-176">-Target</span></span>
<span data-ttu-id="f0d57-177">Mål värden för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="f0d57-178">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="f0d57-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f0d57-179">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="f0d57-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f0d57-180">-Värde</span><span class="sxs-lookup"><span data-stu-id="f0d57-180">-Value</span></span>
<span data-ttu-id="f0d57-181">Textvärdet för TXT-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="f0d57-182">-Vikt</span><span class="sxs-lookup"><span data-stu-id="f0d57-182">-Weight</span></span>
<span data-ttu-id="f0d57-183">Vikt svärdet för SRV-posten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f0d57-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="f0d57-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d57-184">CommonParameters</span></span>
<span data-ttu-id="f0d57-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d57-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d57-186">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d57-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d57-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0d57-187">INPUTS</span></span>

### <span data-ttu-id="f0d57-188">Ingen</span><span class="sxs-lookup"><span data-stu-id="f0d57-188">None</span></span>

## <span data-ttu-id="f0d57-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0d57-189">OUTPUTS</span></span>

### <span data-ttu-id="f0d57-190">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f0d57-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f0d57-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0d57-191">NOTES</span></span>

## <span data-ttu-id="f0d57-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0d57-192">RELATED LINKS</span></span>
