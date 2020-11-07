---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4027b13fb398d69bee09be5c0a939ff86a099e39
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930606"
---
# <span data-ttu-id="17bb6-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="17bb6-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="17bb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="17bb6-103">Hämtar en DNS-post.</span><span class="sxs-lookup"><span data-stu-id="17bb6-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17bb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17bb6-104">SYNTAX</span></span>

### <span data-ttu-id="17bb6-105">Fält</span><span class="sxs-lookup"><span data-stu-id="17bb6-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="17bb6-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="17bb6-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="17bb6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17bb6-107">DESCRIPTION</span></span>
<span data-ttu-id="17bb6-108">Cmdleten **Get-AzureRmDnsRecordSet** hämtar DNS-postuppsättningen (Domain Name System) med det angivna namnet och typen, i den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="17bb6-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="17bb6-109">Om du inte anger parametrarna *Name* eller *RecordType* returnerar denna cmdlet alla post uppsättningar av angiven typ i zonen.</span><span class="sxs-lookup"><span data-stu-id="17bb6-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="17bb6-110">Om du anger parametern *RecordType* men inte parametern *Name* returnerar denna cmdlet alla post uppsättningar av den angivna post typen.</span><span class="sxs-lookup"><span data-stu-id="17bb6-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="17bb6-111">Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen och resurs gruppen efter namn.</span><span class="sxs-lookup"><span data-stu-id="17bb6-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="17bb6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17bb6-112">EXAMPLES</span></span>

### <span data-ttu-id="17bb6-113">Exempel 1: hämta post uppsättningar med ett angivet namn och en viss typ</span><span class="sxs-lookup"><span data-stu-id="17bb6-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="17bb6-114">Det här kommandot hämtar post uppsättningen med post typen en namngiven webb i den angivna resurs gruppen och zonen och lagrar den sedan i $RecordSet variabel.</span><span class="sxs-lookup"><span data-stu-id="17bb6-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="17bb6-115">Eftersom parametrarna *Name* och *RecordType* anges returneras endast ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="17bb6-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="17bb6-116">Exempel 2: hämta post uppsättningar av en viss typ</span><span class="sxs-lookup"><span data-stu-id="17bb6-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="17bb6-117">Det här kommandot får en matris över alla post uppsättningar med post typen A i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="17bb6-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="17bb6-118">Exempel 3: Hämta alla post uppsättningar i en zon</span><span class="sxs-lookup"><span data-stu-id="17bb6-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="17bb6-119">Det här kommandot får en matris över alla post uppsättningar i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="17bb6-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="17bb6-120">Exempel 4: Hämta alla post uppsättningar i en zon med ett DnsZone-objekt</span><span class="sxs-lookup"><span data-stu-id="17bb6-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="17bb6-121">Det här exemplet motsvarar exempel 3 ovan.</span><span class="sxs-lookup"><span data-stu-id="17bb6-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="17bb6-122">Den här gången anges zonen med ett Zone-objekt.</span><span class="sxs-lookup"><span data-stu-id="17bb6-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="17bb6-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17bb6-123">PARAMETERS</span></span>

### <span data-ttu-id="17bb6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="17bb6-124">-Name</span></span>
<span data-ttu-id="17bb6-125">Anger namnet på den **post mängd** som ska visas.</span><span class="sxs-lookup"><span data-stu-id="17bb6-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="17bb6-126">Om du inte anger parametern *Name* returneras alla post uppsättningar av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="17bb6-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="17bb6-127">-RecordType</span></span>
<span data-ttu-id="17bb6-128">Anger den typ av DNS-post som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="17bb6-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="17bb6-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="17bb6-129">Valid values are:</span></span> 

- <span data-ttu-id="17bb6-130">Kallas</span><span class="sxs-lookup"><span data-stu-id="17bb6-130">A</span></span>
- <span data-ttu-id="17bb6-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="17bb6-131">AAAA</span></span>
- <span data-ttu-id="17bb6-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="17bb6-132">CNAME</span></span>
- <span data-ttu-id="17bb6-133">MX</span><span class="sxs-lookup"><span data-stu-id="17bb6-133">MX</span></span>
- <span data-ttu-id="17bb6-134">NS</span><span class="sxs-lookup"><span data-stu-id="17bb6-134">NS</span></span>
- <span data-ttu-id="17bb6-135">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="17bb6-135">PTR</span></span>
- <span data-ttu-id="17bb6-136">BEGÄRANDEN</span><span class="sxs-lookup"><span data-stu-id="17bb6-136">SOA</span></span>
- <span data-ttu-id="17bb6-137">SRV</span><span class="sxs-lookup"><span data-stu-id="17bb6-137">SRV</span></span>
- <span data-ttu-id="17bb6-138">TXT</span><span class="sxs-lookup"><span data-stu-id="17bb6-138">TXT</span></span>

<span data-ttu-id="17bb6-139">Om du inte anger parametern *RecordType* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="17bb6-140">Denna cmdlet returnerar då alla post uppsättningar i zonen (i alla namn och typer).</span><span class="sxs-lookup"><span data-stu-id="17bb6-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bb6-141">-ResourceGroupName</span></span>
<span data-ttu-id="17bb6-142">Anger den resurs grupp som innehåller DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="17bb6-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="17bb6-143">Zonnamn måste också anges med parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="17bb6-144">Alternativt kan du ange zonen och resurs gruppen genom att skicka ett **dnsZone** -objekt med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="17bb6-145">-Zone</span></span>
<span data-ttu-id="17bb6-146">Anger den DNS-zon som innehåller den post uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="17bb6-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="17bb6-147">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-148">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="17bb6-148">-ZoneName</span></span>
<span data-ttu-id="17bb6-149">Anger namnet på den DNS-zon som innehåller den post som ska visas.</span><span class="sxs-lookup"><span data-stu-id="17bb6-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="17bb6-150">Resurs gruppen som innehåller zonen måste också anges med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="17bb6-151">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="17bb6-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bb6-152">CommonParameters</span></span>
<span data-ttu-id="17bb6-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bb6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bb6-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17bb6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bb6-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17bb6-155">INPUTS</span></span>

### <span data-ttu-id="17bb6-156">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="17bb6-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="17bb6-157">Du kan ha ett **dnsZone** -objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17bb6-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="17bb6-158">**DnsZone** -objektet representerar den zon där du vill söka efter **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="17bb6-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="17bb6-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17bb6-159">OUTPUTS</span></span>

### <span data-ttu-id="17bb6-160">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="17bb6-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="17bb6-161">Denna cmdlet returnerar ett eller flera objekt som representerar de post uppsättningar som hittas.</span><span class="sxs-lookup"><span data-stu-id="17bb6-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="17bb6-162">Det kommer att finnas högst en **post uppsättning** som returneras om parametern *Name* och *RecordType* har angetts, annars returneras flera **Recordset** -objekt som en matris.</span><span class="sxs-lookup"><span data-stu-id="17bb6-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="17bb6-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17bb6-163">NOTES</span></span>

## <span data-ttu-id="17bb6-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17bb6-164">RELATED LINKS</span></span>

[<span data-ttu-id="17bb6-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="17bb6-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="17bb6-166">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="17bb6-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="17bb6-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="17bb6-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


