---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: 129177c93d48b55cf8dfe5675d7ffc30ec7f46ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583520"
---
# <span data-ttu-id="7acba-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7acba-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="7acba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7acba-102">SYNOPSIS</span></span>
<span data-ttu-id="7acba-103">Tar bort en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="7acba-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7acba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7acba-104">SYNTAX</span></span>

### <span data-ttu-id="7acba-105">Fält</span><span class="sxs-lookup"><span data-stu-id="7acba-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7acba-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="7acba-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acba-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="7acba-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7acba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7acba-108">DESCRIPTION</span></span>
<span data-ttu-id="7acba-109">Cmdleten **Remove-AzureRmDnsRecordSet** tar bort angiven post uppsättning från den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="7acba-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="7acba-110">Du kan inte ta bort SOA-eller namnserver poster som skapas automatiskt vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="7acba-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="7acba-111">Du kan skicka ett **Recordset** -objekt till denna cmdlet med hjälp av en pipeline-operator eller som en parameter.</span><span class="sxs-lookup"><span data-stu-id="7acba-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="7acba-112">Om du vill identifiera en post uppsättning efter namn och typ utan att använda ett **Recordset** -objekt måste du överföra zonen som ett **dnsZone** -objekt till denna cmdlet genom att använda pipeline-operatorn eller som en parameter, eller också kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acba-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7acba-113">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7acba-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7acba-114">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="7acba-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="7acba-115">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="7acba-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="7acba-116">Du kan förhindra detta genom att använda parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="7acba-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="7acba-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7acba-117">EXAMPLES</span></span>

### <span data-ttu-id="7acba-118">Exempel 1: ta bort en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="7acba-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="7acba-119">Det första kommandot får den angivna post uppsättningen och lagrar den sedan i $RecordSet variabel. Det andra kommandot tar bort post uppsättningen i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="7acba-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="7acba-120">Exempel 2: ta bort en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="7acba-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="7acba-121">Det första kommandot får den angivna post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7acba-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="7acba-122">Det andra kommandot tar bort post uppsättningen, även om den har ändrats under tiden.</span><span class="sxs-lookup"><span data-stu-id="7acba-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="7acba-123">Bekräftelse uppmaningar ignoreras.</span><span class="sxs-lookup"><span data-stu-id="7acba-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="7acba-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7acba-124">PARAMETERS</span></span>

### <span data-ttu-id="7acba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acba-125">-DefaultProfile</span></span>
<span data-ttu-id="7acba-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7acba-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7acba-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="7acba-127">-Name</span></span>
<span data-ttu-id="7acba-128">Anger namnet på den **post mängd** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="7acba-129">När du anger post uppsättningen efter namn måste DNS-zonen anges med parametrarna *Zone* eller *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acba-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7acba-130">Du kan också ange en post uppsättning med hjälp av ett **Recordset** -objekt som skickas med hjälp av *post mängds* parametern.</span><span class="sxs-lookup"><span data-stu-id="7acba-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-131">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="7acba-131">-Overwrite</span></span>
<span data-ttu-id="7acba-132">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="7acba-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="7acba-133">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="7acba-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="7acba-134">Det här kan utelämnas med hjälp av parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="7acba-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7acba-135">-PassThru</span></span>
<span data-ttu-id="7acba-136">passthru</span><span class="sxs-lookup"><span data-stu-id="7acba-136">passthru</span></span>

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

### <span data-ttu-id="7acba-137">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="7acba-137">-RecordSet</span></span>
<span data-ttu-id="7acba-138">Anger det **Recordset** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="7acba-139">Du kan också ange post uppsättningen med *namn* -och *zonkod* eller använda parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acba-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="7acba-140">-RecordType</span></span>
<span data-ttu-id="7acba-141">Anger typen av DNS-post.</span><span class="sxs-lookup"><span data-stu-id="7acba-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="7acba-142">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7acba-142">Valid values are:</span></span>
- <span data-ttu-id="7acba-143">Kallas</span><span class="sxs-lookup"><span data-stu-id="7acba-143">A</span></span>
- <span data-ttu-id="7acba-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="7acba-144">AAAA</span></span>
- <span data-ttu-id="7acba-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="7acba-145">CNAME</span></span>
- <span data-ttu-id="7acba-146">MX</span><span class="sxs-lookup"><span data-stu-id="7acba-146">MX</span></span>
- <span data-ttu-id="7acba-147">NS</span><span class="sxs-lookup"><span data-stu-id="7acba-147">NS</span></span>
- <span data-ttu-id="7acba-148">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="7acba-148">PTR</span></span>
- <span data-ttu-id="7acba-149">SRV</span><span class="sxs-lookup"><span data-stu-id="7acba-149">SRV</span></span>
- <span data-ttu-id="7acba-150">TXT SOA-poster tas bort automatiskt när zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="7acba-151">Du kan inte ta bort SOA-poster manuellt.</span><span class="sxs-lookup"><span data-stu-id="7acba-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7acba-152">-ResourceGroupName</span></span>
<span data-ttu-id="7acba-153">Anger den resurs grupp som innehåller den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="7acba-154">Den här parametern är endast tillämpbar när post uppsättningen och DNS-zonen anges med parametrarna *namn* och *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="7acba-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="7acba-155">Alternativt kan du ange den post uppsättning som använder parametern *post uppsättning* eller *namn* - *och parameter parametrar* .</span><span class="sxs-lookup"><span data-stu-id="7acba-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="7acba-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="7acba-156">-Zone</span></span>
<span data-ttu-id="7acba-157">Anger den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="7acba-158">Den här parametern används endast när du anger en post uppsättning med parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="7acba-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="7acba-159">Eller så kan du ange den post uppsättning som använder parametern *post uppsättning* eller parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acba-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-160">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="7acba-160">-ZoneName</span></span>
<span data-ttu-id="7acba-161">Anger namnet på den zon som innehåller **post mängden** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7acba-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="7acba-162">Du måste också ange *namnet* och *ResourceGroupName* parametrar.</span><span class="sxs-lookup"><span data-stu-id="7acba-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7acba-163">Du kan också ange post uppsättningen genom att använda parametern *post mängd* eller *namn* *-och parameter* parametrar.</span><span class="sxs-lookup"><span data-stu-id="7acba-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="7acba-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7acba-164">-Confirm</span></span>
<span data-ttu-id="7acba-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7acba-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acba-166">-WhatIf</span></span>
<span data-ttu-id="7acba-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7acba-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7acba-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7acba-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acba-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acba-169">CommonParameters</span></span>
<span data-ttu-id="7acba-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acba-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acba-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7acba-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acba-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7acba-172">INPUTS</span></span>

### <span data-ttu-id="7acba-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="7acba-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="7acba-174">System. String</span><span class="sxs-lookup"><span data-stu-id="7acba-174">System.String</span></span>

### <span data-ttu-id="7acba-175">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="7acba-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="7acba-176">Parametrar: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7acba-176">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="7acba-177">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7acba-177">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="7acba-178">Parametrar: RecordSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7acba-178">Parameters: RecordSet (ByValue)</span></span>

## <span data-ttu-id="7acba-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7acba-179">OUTPUTS</span></span>

### <span data-ttu-id="7acba-180">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7acba-180">System.Boolean</span></span>

## <span data-ttu-id="7acba-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7acba-181">NOTES</span></span>
<span data-ttu-id="7acba-182">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7acba-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7acba-183">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="7acba-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="7acba-184">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="7acba-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="7acba-185">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7acba-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7acba-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7acba-186">RELATED LINKS</span></span>

[<span data-ttu-id="7acba-187">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7acba-187">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="7acba-188">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7acba-188">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="7acba-189">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7acba-189">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
