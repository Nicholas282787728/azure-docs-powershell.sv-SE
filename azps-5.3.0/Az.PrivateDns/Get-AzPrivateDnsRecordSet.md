---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523101"
---
# <span data-ttu-id="dec50-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dec50-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="dec50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dec50-102">SYNOPSIS</span></span>
<span data-ttu-id="dec50-103">Hämtar en post uppsättning från en privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="dec50-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="dec50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dec50-104">SYNTAX</span></span>

### <span data-ttu-id="dec50-105">FieldsWithNoName (standard)</span><span class="sxs-lookup"><span data-stu-id="dec50-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec50-106">Fält</span><span class="sxs-lookup"><span data-stu-id="dec50-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec50-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="dec50-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec50-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="dec50-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec50-109">ID</span><span class="sxs-lookup"><span data-stu-id="dec50-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dec50-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="dec50-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dec50-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dec50-111">DESCRIPTION</span></span>
<span data-ttu-id="dec50-112">Den privata DNS-postuppsättningen (Domain Name System) med det angivna namnet och typen i den angivna privata zonen hämtas av Get-AzPrivateDnsRecordSet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dec50-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="dec50-113">Om du inte anger parametrarna Name eller RecordType returnerar denna cmdlet alla post uppsättningar av den angivna typen i den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="dec50-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="dec50-114">Om du anger parametern RecordType men inte parametern name returnerar denna cmdlet alla post uppsättningar av den angivna post typen.</span><span class="sxs-lookup"><span data-stu-id="dec50-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="dec50-115">Du kan använda pipeline-operatorn för att skicka ett PSPrivateDnsZone-objekt till denna cmdlet, eller så kan du skicka ett PSPrivateDnsZone-objekt som parametern Zone, eller så kan du ange zonen och resurs gruppen efter namn.</span><span class="sxs-lookup"><span data-stu-id="dec50-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="dec50-116">Du kan också ange den privata zonen med resurs-ID för den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="dec50-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="dec50-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dec50-117">EXAMPLES</span></span>

### <span data-ttu-id="dec50-118">Exempel 1: hämta post uppsättningar med ett angivet namn och en viss typ</span><span class="sxs-lookup"><span data-stu-id="dec50-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="dec50-119">Det här kommandot hämtar post uppsättningen med post typen en namngiven webb i den angivna resurs gruppen och den privata zonen och lagrar den sedan i $RecordSet variabel.</span><span class="sxs-lookup"><span data-stu-id="dec50-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="dec50-120">Eftersom parametrarna Name och RecordType anges returneras endast ett RecordSet-objekt.</span><span class="sxs-lookup"><span data-stu-id="dec50-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="dec50-121">Exempel 2: hämta post uppsättningar av en viss typ</span><span class="sxs-lookup"><span data-stu-id="dec50-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dec50-122">Det här kommandot får en matris över alla post uppsättningar med post typen A i den privata zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="dec50-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="dec50-123">Exempel 3: Hämta alla post uppsättningar i en privat zon</span><span class="sxs-lookup"><span data-stu-id="dec50-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dec50-124">Det här kommandot får en matris över alla post uppsättningar i den privata zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="dec50-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="dec50-125">Exempel 4: Hämta alla post uppsättningar i en privat zon med ett PSPrivateDnsZone-objekt</span><span class="sxs-lookup"><span data-stu-id="dec50-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dec50-126">Det här exemplet motsvarar exempel 3 ovan.</span><span class="sxs-lookup"><span data-stu-id="dec50-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="dec50-127">Den här gången anges den privata zonen med ett objekt i den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="dec50-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="dec50-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dec50-128">PARAMETERS</span></span>

### <span data-ttu-id="dec50-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec50-129">-DefaultProfile</span></span>
<span data-ttu-id="dec50-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dec50-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dec50-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="dec50-131">-Name</span></span>
<span data-ttu-id="dec50-132">Namnet på posterna i den här post uppsättningen (i förhållande till namnet på zonen och utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="dec50-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dec50-133">-ParentResourceId</span></span>
<span data-ttu-id="dec50-134">Privat DNS-zon ResourceID.</span><span class="sxs-lookup"><span data-stu-id="dec50-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="dec50-135">-RecordType</span></span>
<span data-ttu-id="dec50-136">Typen av DNS-poster i den här post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="dec50-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec50-137">-ResourceGroupName</span></span>
<span data-ttu-id="dec50-138">Den resurs grupp som zonen tillhör.</span><span class="sxs-lookup"><span data-stu-id="dec50-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="dec50-139">-Zone</span></span>
<span data-ttu-id="dec50-140">DnsZone-objektet som representerar den zon där du vill skapa post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="dec50-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-141">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="dec50-141">-ZoneName</span></span>
<span data-ttu-id="dec50-142">Den zon där du vill skapa post uppsättningen (utan att avsluta punkter).</span><span class="sxs-lookup"><span data-stu-id="dec50-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec50-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec50-143">CommonParameters</span></span>
<span data-ttu-id="dec50-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dec50-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec50-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec50-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec50-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dec50-146">INPUTS</span></span>

### <span data-ttu-id="dec50-147">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="dec50-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="dec50-148">System. String</span><span class="sxs-lookup"><span data-stu-id="dec50-148">System.String</span></span>

## <span data-ttu-id="dec50-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dec50-149">OUTPUTS</span></span>

### <span data-ttu-id="dec50-150">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dec50-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="dec50-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dec50-151">NOTES</span></span>

## <span data-ttu-id="dec50-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dec50-152">RELATED LINKS</span></span>
