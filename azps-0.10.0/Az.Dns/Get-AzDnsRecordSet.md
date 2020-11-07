---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924613"
---
# <span data-ttu-id="892b3-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="892b3-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="892b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="892b3-102">SYNOPSIS</span></span>
<span data-ttu-id="892b3-103">Hämtar en DNS-post.</span><span class="sxs-lookup"><span data-stu-id="892b3-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="892b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="892b3-104">SYNTAX</span></span>

### <span data-ttu-id="892b3-105">Fält</span><span class="sxs-lookup"><span data-stu-id="892b3-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="892b3-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="892b3-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="892b3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="892b3-107">DESCRIPTION</span></span>
<span data-ttu-id="892b3-108">Cmdleten **Get-AzDnsRecordSet** hämtar DNS-postuppsättningen (Domain Name System) med det angivna namnet och typen, i den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="892b3-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="892b3-109">Om du inte anger parametrarna *Name* eller *RecordType* returnerar denna cmdlet alla post uppsättningar av angiven typ i zonen.</span><span class="sxs-lookup"><span data-stu-id="892b3-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="892b3-110">Om du anger parametern *RecordType* men inte parametern *Name* returnerar denna cmdlet alla post uppsättningar av den angivna post typen.</span><span class="sxs-lookup"><span data-stu-id="892b3-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="892b3-111">Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen och resurs gruppen efter namn.</span><span class="sxs-lookup"><span data-stu-id="892b3-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="892b3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="892b3-112">EXAMPLES</span></span>

### <span data-ttu-id="892b3-113">Exempel 1: hämta post uppsättningar med ett angivet namn och en viss typ</span><span class="sxs-lookup"><span data-stu-id="892b3-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="892b3-114">Det här kommandot hämtar post uppsättningen med post typen en namngiven webb i den angivna resurs gruppen och zonen och lagrar den sedan i $RecordSet variabel.</span><span class="sxs-lookup"><span data-stu-id="892b3-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="892b3-115">Eftersom parametrarna *Name* och *RecordType* anges returneras endast ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="892b3-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="892b3-116">Exempel 2: hämta post uppsättningar av en viss typ</span><span class="sxs-lookup"><span data-stu-id="892b3-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="892b3-117">Det här kommandot får en matris över alla post uppsättningar med post typen A i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="892b3-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="892b3-118">Exempel 3: Hämta alla post uppsättningar i en zon</span><span class="sxs-lookup"><span data-stu-id="892b3-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="892b3-119">Det här kommandot får en matris över alla post uppsättningar i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="892b3-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="892b3-120">Exempel 4: Hämta alla post uppsättningar i en zon med ett DnsZone-objekt</span><span class="sxs-lookup"><span data-stu-id="892b3-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="892b3-121">Det här exemplet motsvarar exempel 3 ovan.</span><span class="sxs-lookup"><span data-stu-id="892b3-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="892b3-122">Den här gången anges zonen med ett Zone-objekt.</span><span class="sxs-lookup"><span data-stu-id="892b3-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="892b3-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="892b3-123">PARAMETERS</span></span>

### <span data-ttu-id="892b3-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="892b3-124">-Name</span></span>
<span data-ttu-id="892b3-125">Anger namnet på den **post mängd** som ska visas.</span><span class="sxs-lookup"><span data-stu-id="892b3-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="892b3-126">Om du inte anger parametern *Name* returneras alla post uppsättningar av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="892b3-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="892b3-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="892b3-127">-RecordType</span></span>
<span data-ttu-id="892b3-128">Anger den typ av DNS-post som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="892b3-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="892b3-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="892b3-129">Valid values are:</span></span> 

- <span data-ttu-id="892b3-130">Kallas</span><span class="sxs-lookup"><span data-stu-id="892b3-130">A</span></span>
- <span data-ttu-id="892b3-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="892b3-131">AAAA</span></span>
- <span data-ttu-id="892b3-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="892b3-132">CNAME</span></span>
- <span data-ttu-id="892b3-133">MX</span><span class="sxs-lookup"><span data-stu-id="892b3-133">MX</span></span>
- <span data-ttu-id="892b3-134">NS</span><span class="sxs-lookup"><span data-stu-id="892b3-134">NS</span></span>
- <span data-ttu-id="892b3-135">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="892b3-135">PTR</span></span>
- <span data-ttu-id="892b3-136">BEGÄRANDEN</span><span class="sxs-lookup"><span data-stu-id="892b3-136">SOA</span></span>
- <span data-ttu-id="892b3-137">SRV</span><span class="sxs-lookup"><span data-stu-id="892b3-137">SRV</span></span>
- <span data-ttu-id="892b3-138">TXT</span><span class="sxs-lookup"><span data-stu-id="892b3-138">TXT</span></span>

<span data-ttu-id="892b3-139">Om du inte anger parametern *RecordType* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="892b3-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="892b3-140">Denna cmdlet returnerar då alla post uppsättningar i zonen (i alla namn och typer).</span><span class="sxs-lookup"><span data-stu-id="892b3-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="892b3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892b3-141">-ResourceGroupName</span></span>
<span data-ttu-id="892b3-142">Anger den resurs grupp som innehåller DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="892b3-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="892b3-143">Zonnamn måste också anges med parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="892b3-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="892b3-144">Alternativt kan du ange zonen och resurs gruppen genom att skicka ett **dnsZone** -objekt med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="892b3-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="892b3-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="892b3-145">-Zone</span></span>
<span data-ttu-id="892b3-146">Anger den DNS-zon som innehåller den post uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="892b3-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="892b3-147">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="892b3-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="892b3-148">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="892b3-148">-ZoneName</span></span>
<span data-ttu-id="892b3-149">Anger namnet på den DNS-zon som innehåller den post som ska visas.</span><span class="sxs-lookup"><span data-stu-id="892b3-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="892b3-150">Resurs gruppen som innehåller zonen måste också anges med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="892b3-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="892b3-151">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="892b3-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="892b3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892b3-152">CommonParameters</span></span>
<span data-ttu-id="892b3-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892b3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892b3-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892b3-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892b3-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="892b3-155">INPUTS</span></span>

### <span data-ttu-id="892b3-156">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="892b3-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="892b3-157">Du kan ha ett **dnsZone** -objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="892b3-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="892b3-158">**DnsZone** -objektet representerar den zon där du vill söka efter **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="892b3-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="892b3-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="892b3-159">OUTPUTS</span></span>

### <span data-ttu-id="892b3-160">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="892b3-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="892b3-161">Denna cmdlet returnerar ett eller flera objekt som representerar de post uppsättningar som hittas.</span><span class="sxs-lookup"><span data-stu-id="892b3-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="892b3-162">Det kommer att finnas högst en **post uppsättning** som returneras om parametern *Name* och *RecordType* har angetts, annars returneras flera **Recordset** -objekt som en matris.</span><span class="sxs-lookup"><span data-stu-id="892b3-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="892b3-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="892b3-163">NOTES</span></span>

## <span data-ttu-id="892b3-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="892b3-164">RELATED LINKS</span></span>

[<span data-ttu-id="892b3-165">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="892b3-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="892b3-166">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="892b3-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="892b3-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="892b3-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


