---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
ms.openlocfilehash: b86ad0382fa7f87ac8aabb6b026b84d5a879f8ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930590"
---
# <span data-ttu-id="14b53-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="14b53-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="14b53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14b53-102">SYNOPSIS</span></span>
<span data-ttu-id="14b53-103">Tar bort en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="14b53-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14b53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14b53-104">SYNTAX</span></span>

### <span data-ttu-id="14b53-105">Fält</span><span class="sxs-lookup"><span data-stu-id="14b53-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b53-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="14b53-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b53-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="14b53-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14b53-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14b53-108">DESCRIPTION</span></span>
<span data-ttu-id="14b53-109">Cmdleten **Remove-AzureRmDnsRecordSet** tar bort angiven post uppsättning från den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="14b53-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="14b53-110">Du kan inte ta bort SOA-eller namnserver poster som skapas automatiskt vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="14b53-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="14b53-111">Du kan skicka ett **Recordset** -objekt till denna cmdlet med hjälp av en pipeline-operator eller som en parameter.</span><span class="sxs-lookup"><span data-stu-id="14b53-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="14b53-112">Om du vill identifiera en post uppsättning efter namn och typ utan att använda ett **Recordset** -objekt måste du överföra zonen som ett **dnsZone** -objekt till denna cmdlet genom att använda pipeline-operatorn eller som en parameter, eller också kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="14b53-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="14b53-113">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="14b53-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="14b53-114">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="14b53-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="14b53-115">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="14b53-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="14b53-116">Du kan förhindra detta genom att använda parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="14b53-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="14b53-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14b53-117">EXAMPLES</span></span>

### <span data-ttu-id="14b53-118">Exempel 1: ta bort en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="14b53-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="14b53-119">Det första kommandot får den angivna post uppsättningen och lagrar den sedan i $RecordSet variabel. Det andra kommandot tar bort post uppsättningen i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="14b53-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="14b53-120">Exempel 2: ta bort en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="14b53-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="14b53-121">Det första kommandot får den angivna post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="14b53-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="14b53-122">Det andra kommandot tar bort post uppsättningen, även om den har ändrats under tiden.</span><span class="sxs-lookup"><span data-stu-id="14b53-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="14b53-123">Bekräftelse uppmaningar ignoreras.</span><span class="sxs-lookup"><span data-stu-id="14b53-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="14b53-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14b53-124">PARAMETERS</span></span>

### <span data-ttu-id="14b53-125">-Force</span><span class="sxs-lookup"><span data-stu-id="14b53-125">-Force</span></span>
<span data-ttu-id="14b53-126">Den här parametern är föråldrad för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14b53-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="14b53-127">Den kommer att tas bort i en senare version.</span><span class="sxs-lookup"><span data-stu-id="14b53-127">It will be removed in a future release.</span></span>

<span data-ttu-id="14b53-128">Om du vill kontrol lera om den här cmdleten uppmanar dig att bekräfta kan du använda parametern *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="14b53-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="14b53-129">-Name</span></span>
<span data-ttu-id="14b53-130">Anger namnet på den **post mängd** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="14b53-131">När du anger post uppsättningen efter namn måste DNS-zonen anges med parametrarna *Zone* eller *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="14b53-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="14b53-132">Du kan också ange en post uppsättning med hjälp av ett **Recordset** -objekt som skickas med hjälp av *post mängds* parametern.</span><span class="sxs-lookup"><span data-stu-id="14b53-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-133">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="14b53-133">-Overwrite</span></span>
<span data-ttu-id="14b53-134">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="14b53-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="14b53-135">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="14b53-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="14b53-136">Det här kan utelämnas med hjälp av parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="14b53-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14b53-137">-PassThru</span></span>
<span data-ttu-id="14b53-138">passthru</span><span class="sxs-lookup"><span data-stu-id="14b53-138">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-139">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="14b53-139">-RecordSet</span></span>
<span data-ttu-id="14b53-140">Anger det **Recordset** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="14b53-141">Du kan också ange post uppsättningen med *namn* -och *zonkod* eller använda parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="14b53-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="14b53-142">-RecordType</span></span>
<span data-ttu-id="14b53-143">Anger typen av DNS-post.</span><span class="sxs-lookup"><span data-stu-id="14b53-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="14b53-144">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="14b53-144">Valid values are:</span></span>

- <span data-ttu-id="14b53-145">Kallas</span><span class="sxs-lookup"><span data-stu-id="14b53-145">A</span></span>
- <span data-ttu-id="14b53-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="14b53-146">AAAA</span></span>
- <span data-ttu-id="14b53-147">CNAME</span><span class="sxs-lookup"><span data-stu-id="14b53-147">CNAME</span></span>
- <span data-ttu-id="14b53-148">MX</span><span class="sxs-lookup"><span data-stu-id="14b53-148">MX</span></span>
- <span data-ttu-id="14b53-149">NS</span><span class="sxs-lookup"><span data-stu-id="14b53-149">NS</span></span>
- <span data-ttu-id="14b53-150">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="14b53-150">PTR</span></span>
- <span data-ttu-id="14b53-151">SRV</span><span class="sxs-lookup"><span data-stu-id="14b53-151">SRV</span></span>
- <span data-ttu-id="14b53-152">TXT</span><span class="sxs-lookup"><span data-stu-id="14b53-152">TXT</span></span>

<span data-ttu-id="14b53-153">SOA-poster tas bort automatiskt när zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="14b53-154">Du kan inte ta bort SOA-poster manuellt.</span><span class="sxs-lookup"><span data-stu-id="14b53-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b53-155">-ResourceGroupName</span></span>
<span data-ttu-id="14b53-156">Anger den resurs grupp som innehåller den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="14b53-157">Den här parametern är endast tillämpbar när post uppsättningen och DNS-zonen anges med parametrarna *namn* och *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="14b53-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="14b53-158">Alternativt kan du ange den post uppsättning som använder parametern *post uppsättning* eller *namn* - *och parameter parametrar* .</span><span class="sxs-lookup"><span data-stu-id="14b53-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="14b53-159">-Zone</span><span class="sxs-lookup"><span data-stu-id="14b53-159">-Zone</span></span>
<span data-ttu-id="14b53-160">Anger den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="14b53-161">Den här parametern används endast när du anger en post uppsättning med parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="14b53-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="14b53-162">Eller så kan du ange den post uppsättning som använder parametern *post uppsättning* eller parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="14b53-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-163">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="14b53-163">-ZoneName</span></span>
<span data-ttu-id="14b53-164">Anger namnet på den zon som innehåller **post mängden** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="14b53-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="14b53-165">Du måste också ange *namnet* och *ResourceGroupName* parametrar.</span><span class="sxs-lookup"><span data-stu-id="14b53-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="14b53-166">Du kan också ange post uppsättningen genom att använda parametern *post mängd* eller *namn* *-och parameter* parametrar.</span><span class="sxs-lookup"><span data-stu-id="14b53-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="14b53-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14b53-167">-Confirm</span></span>
<span data-ttu-id="14b53-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14b53-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b53-169">-WhatIf</span></span>
<span data-ttu-id="14b53-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14b53-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14b53-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14b53-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b53-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b53-172">CommonParameters</span></span>
<span data-ttu-id="14b53-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b53-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b53-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b53-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b53-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14b53-175">INPUTS</span></span>

### <span data-ttu-id="14b53-176">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="14b53-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="14b53-177">Du kan **göra en pipe** till den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14b53-177">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="14b53-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14b53-178">OUTPUTS</span></span>

### <span data-ttu-id="14b53-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="14b53-179">None</span></span>
<span data-ttu-id="14b53-180">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="14b53-180">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="14b53-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14b53-181">NOTES</span></span>
<span data-ttu-id="14b53-182">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="14b53-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="14b53-183">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="14b53-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="14b53-184">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="14b53-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="14b53-185">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="14b53-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="14b53-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14b53-186">RELATED LINKS</span></span>

[<span data-ttu-id="14b53-187">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="14b53-187">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="14b53-188">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="14b53-188">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="14b53-189">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="14b53-189">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
