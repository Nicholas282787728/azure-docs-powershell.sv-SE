---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263206"
---
# <span data-ttu-id="a7a9d-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="a7a9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a9d-103">Hämtar en DNS-post.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="a7a9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7a9d-104">SYNTAX</span></span>

### <span data-ttu-id="a7a9d-105">Fält</span><span class="sxs-lookup"><span data-stu-id="a7a9d-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a9d-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a9d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7a9d-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a9d-108">Cmdleten **Get-AzDnsRecordSet** hämtar DNS-postuppsättningen (Domain Name System) med det angivna namnet och typen, i den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="a7a9d-109">Om du inte anger parametrarna *Name* eller *RecordType* returnerar denna cmdlet alla post uppsättningar av angiven typ i zonen.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="a7a9d-110">Om du anger parametern *RecordType* men inte parametern *Name* returnerar denna cmdlet alla post uppsättningar av den angivna post typen.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="a7a9d-111">Du kan använda pipeline-operatorn för att skicka ett **dnsZone** -objekt till denna cmdlet, eller så kan du skicka ett **dnsZone** -objekt som parametern *Zone* , eller så kan du ange zonen och resurs gruppen efter namn.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="a7a9d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7a9d-112">EXAMPLES</span></span>

### <span data-ttu-id="a7a9d-113">Exempel 1: hämta post uppsättningar med ett angivet namn och en viss typ</span><span class="sxs-lookup"><span data-stu-id="a7a9d-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="a7a9d-114">Det här kommandot hämtar post uppsättningen med post typen en namngiven webb i den angivna resurs gruppen och zonen och lagrar den sedan i $RecordSet variabel.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="a7a9d-115">Eftersom parametrarna *Name* och *RecordType* anges returneras endast ett **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="a7a9d-116">Exempel 2: hämta post uppsättningar av en viss typ</span><span class="sxs-lookup"><span data-stu-id="a7a9d-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="a7a9d-117">Det här kommandot får en matris över alla post uppsättningar med post typen A i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a7a9d-118">Exempel 3: Hämta alla post uppsättningar i en zon</span><span class="sxs-lookup"><span data-stu-id="a7a9d-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="a7a9d-119">Det här kommandot får en matris över alla post uppsättningar i zonen med namnet myzone.com i resurs gruppen som heter MyResourceGroup och lagrar dem sedan i $RecordSets variabel.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a7a9d-120">Exempel 4: Hämta alla post uppsättningar i en zon med ett DnsZone-objekt</span><span class="sxs-lookup"><span data-stu-id="a7a9d-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="a7a9d-121">Det här exemplet motsvarar exempel 3 ovan.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="a7a9d-122">Den här gången anges zonen med ett Zone-objekt.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="a7a9d-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7a9d-123">PARAMETERS</span></span>

### <span data-ttu-id="a7a9d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a9d-124">-DefaultProfile</span></span>
<span data-ttu-id="a7a9d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a7a9d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7a9d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7a9d-126">-Name</span></span>
<span data-ttu-id="a7a9d-127">Anger namnet på den **post mängd** som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="a7a9d-128">Om du inte anger parametern *Name* returneras alla post uppsättningar av den angivna typen.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9d-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a7a9d-129">-RecordType</span></span>
<span data-ttu-id="a7a9d-130">Anger den typ av DNS-post som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="a7a9d-131">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a7a9d-131">Valid values are:</span></span> 
- <span data-ttu-id="a7a9d-132">Kallas</span><span class="sxs-lookup"><span data-stu-id="a7a9d-132">A</span></span>
- <span data-ttu-id="a7a9d-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="a7a9d-133">AAAA</span></span>
- <span data-ttu-id="a7a9d-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="a7a9d-134">CNAME</span></span>
- <span data-ttu-id="a7a9d-135">MX</span><span class="sxs-lookup"><span data-stu-id="a7a9d-135">MX</span></span>
- <span data-ttu-id="a7a9d-136">NS</span><span class="sxs-lookup"><span data-stu-id="a7a9d-136">NS</span></span>
- <span data-ttu-id="a7a9d-137">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="a7a9d-137">PTR</span></span>
- <span data-ttu-id="a7a9d-138">BEGÄRANDEN</span><span class="sxs-lookup"><span data-stu-id="a7a9d-138">SOA</span></span>
- <span data-ttu-id="a7a9d-139">SRV</span><span class="sxs-lookup"><span data-stu-id="a7a9d-139">SRV</span></span>
- <span data-ttu-id="a7a9d-140">TXT om du inte anger parametern *RecordType* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="a7a9d-141">Denna cmdlet returnerar då alla post uppsättningar i zonen (i alla namn och typer).</span><span class="sxs-lookup"><span data-stu-id="a7a9d-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a9d-142">-ResourceGroupName</span></span>
<span data-ttu-id="a7a9d-143">Anger den resurs grupp som innehåller DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a7a9d-144">Zonnamn måste också anges med parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="a7a9d-145">Alternativt kan du ange zonen och resurs gruppen genom att skicka ett **dnsZone** -objekt med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9d-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="a7a9d-146">-Zone</span></span>
<span data-ttu-id="a7a9d-147">Anger den DNS-zon som innehåller den post uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="a7a9d-148">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9d-149">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="a7a9d-149">-ZoneName</span></span>
<span data-ttu-id="a7a9d-150">Anger namnet på den DNS-zon som innehåller den post som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="a7a9d-151">Resurs gruppen som innehåller zonen måste också anges med parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a7a9d-152">Alternativt kan du ange zonen och resurs gruppen genom att överföra ett DNS-zonfiler med *zonen Zone* .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a9d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a9d-153">CommonParameters</span></span>
<span data-ttu-id="a7a9d-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a9d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a9d-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a9d-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a9d-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7a9d-156">INPUTS</span></span>

### <span data-ttu-id="a7a9d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a9d-157">System.String</span></span>

### <span data-ttu-id="a7a9d-158">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a7a9d-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="a7a9d-159">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a7a9d-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a7a9d-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7a9d-160">OUTPUTS</span></span>

### <span data-ttu-id="a7a9d-161">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="a7a9d-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7a9d-162">NOTES</span></span>

## <span data-ttu-id="a7a9d-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7a9d-163">RELATED LINKS</span></span>

[<span data-ttu-id="a7a9d-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a7a9d-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="a7a9d-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a7a9d-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


