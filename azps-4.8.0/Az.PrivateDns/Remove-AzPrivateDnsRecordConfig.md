---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258750"
---
# <span data-ttu-id="e95f9-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e95f9-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="e95f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e95f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e95f9-103">Tar bort en privat DNS-post från ett lokalt post uppsättnings objekt.</span><span class="sxs-lookup"><span data-stu-id="e95f9-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="e95f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e95f9-104">SYNTAX</span></span>

### <span data-ttu-id="e95f9-105">A (standard)</span><span class="sxs-lookup"><span data-stu-id="e95f9-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="e95f9-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-107">MX</span><span class="sxs-lookup"><span data-stu-id="e95f9-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-108">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="e95f9-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-109">TXT</span><span class="sxs-lookup"><span data-stu-id="e95f9-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-110">SRV</span><span class="sxs-lookup"><span data-stu-id="e95f9-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95f9-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="e95f9-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95f9-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e95f9-112">DESCRIPTION</span></span>
<span data-ttu-id="e95f9-113">Remove-AzPrivateDnsRecordConfig-cmdleten tar bort en privat DNS-post (Domain Name System) från en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="e95f9-114">Objektet RecordSet är ett offlineobjekt och ändringar i det påverkar inte de privata DNS-svaren förrän du har kört Set-AzPrivateDnsRecordSet cmdlet för att bevara ändringen av Microsoft Azure Private DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e95f9-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="e95f9-115">Om du vill ta bort en post måste alla fält för den post typen matcha exakt.</span><span class="sxs-lookup"><span data-stu-id="e95f9-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="e95f9-116">Du kan inte lägga till eller ta bort SOA-poster.</span><span class="sxs-lookup"><span data-stu-id="e95f9-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="e95f9-117">SOA-poster skapas automatiskt när en privat DNS-zon skapas och tas bort automatiskt när den privata DNS-zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="e95f9-118">Du kan överföra RecordSet-objektet till denna cmdlet som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e95f9-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="e95f9-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e95f9-119">EXAMPLES</span></span>

### <span data-ttu-id="e95f9-120">Exempel 1: ta bort en post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-121">I det här exemplet tas en post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="e95f9-122">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="e95f9-123">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="e95f9-124">Exempel 2: ta bort en AAAA-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-125">I det här exemplet tas en AAAA-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="e95f9-126">Om det är den enda posten i post uppsättningen blir resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="e95f9-127">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="e95f9-128">Exempel 3: ta bort en CNAME-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-129">I det här exemplet tas en CNAME-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="e95f9-130">Eftersom en CNAME-postuppsättning kan innehålla högst en post är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="e95f9-131">Exempel 4: ta bort en MX-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-132">I det här exemplet tas en MX-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="e95f9-133">Post namnet "@" anger en post uppsättning vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="e95f9-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="e95f9-134">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="e95f9-135">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="e95f9-136">Exempel 5: ta bort en PTR-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-137">I det här exemplet tas en PTR-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="e95f9-138">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="e95f9-139">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="e95f9-140">Exempel 6: ta bort en SRV-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-141">I det här exemplet tas en SRV-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="e95f9-142">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="e95f9-143">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="e95f9-144">Exempel 7: ta bort en TXT-post från en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e95f9-145">I det här exemplet tas en TXT-post bort från en befintlig post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="e95f9-146">Om det är den enda posten i post uppsättningen är resultatet en tom post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="e95f9-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="e95f9-147">Om du bara vill ta bort en post uppsättning, se Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="e95f9-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="e95f9-148">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e95f9-148">PARAMETERS</span></span>

### <span data-ttu-id="e95f9-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="e95f9-149">-Cname</span></span>
<span data-ttu-id="e95f9-150">Kanoniskt namn på CNAME-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="e95f9-151">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="e95f9-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e95f9-152">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="e95f9-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e95f9-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95f9-153">-DefaultProfile</span></span>
<span data-ttu-id="e95f9-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e95f9-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95f9-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="e95f9-155">-Exchange</span></span>
<span data-ttu-id="e95f9-156">E-postvärdet för MX-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="e95f9-157">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="e95f9-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e95f9-158">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="e95f9-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e95f9-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="e95f9-159">-Ipv4Address</span></span>
<span data-ttu-id="e95f9-160">IPv4-adressen för den A-post som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="e95f9-161">-IPv6</span><span class="sxs-lookup"><span data-stu-id="e95f9-161">-Ipv6Address</span></span>
<span data-ttu-id="e95f9-162">IPv6-adressen för AAAA-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="e95f9-163">-Port</span><span class="sxs-lookup"><span data-stu-id="e95f9-163">-Port</span></span>
<span data-ttu-id="e95f9-164">Port numret för SRV-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="e95f9-165">-Preferens</span><span class="sxs-lookup"><span data-stu-id="e95f9-165">-Preference</span></span>
<span data-ttu-id="e95f9-166">Preferens svärdet för MX-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="e95f9-167">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="e95f9-167">-Priority</span></span>
<span data-ttu-id="e95f9-168">Prioritet svärdet för SRV-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="e95f9-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="e95f9-169">-Ptrdname</span></span>
<span data-ttu-id="e95f9-170">Mål värden för PTR-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="e95f9-171">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="e95f9-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e95f9-172">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="e95f9-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e95f9-173">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="e95f9-173">-RecordSet</span></span>
<span data-ttu-id="e95f9-174">Den post uppsättning som posten ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="e95f9-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="e95f9-175">-Mål</span><span class="sxs-lookup"><span data-stu-id="e95f9-175">-Target</span></span>
<span data-ttu-id="e95f9-176">Mål värden för SRV-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="e95f9-177">Får inte vara relativ till zonens namn.</span><span class="sxs-lookup"><span data-stu-id="e95f9-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e95f9-178">Får inte ha en avslutande punkt</span><span class="sxs-lookup"><span data-stu-id="e95f9-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e95f9-179">-Värde</span><span class="sxs-lookup"><span data-stu-id="e95f9-179">-Value</span></span>
<span data-ttu-id="e95f9-180">Textvärdet för TXT-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="e95f9-181">-Vikt</span><span class="sxs-lookup"><span data-stu-id="e95f9-181">-Weight</span></span>
<span data-ttu-id="e95f9-182">Vikt värde för SRV-posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e95f9-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="e95f9-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95f9-183">CommonParameters</span></span>
<span data-ttu-id="e95f9-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95f9-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95f9-185">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95f9-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95f9-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e95f9-186">INPUTS</span></span>

### <span data-ttu-id="e95f9-187">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e95f9-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="e95f9-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e95f9-188">OUTPUTS</span></span>

### <span data-ttu-id="e95f9-189">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e95f9-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="e95f9-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e95f9-190">NOTES</span></span>

## <span data-ttu-id="e95f9-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e95f9-191">RELATED LINKS</span></span>
