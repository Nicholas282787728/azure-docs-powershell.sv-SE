---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: e009eea8276bbfe9653c506864604ca955a6367f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574673"
---
# <span data-ttu-id="aeb16-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="aeb16-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="aeb16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aeb16-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb16-103">Tar bort en post uppsättning.</span><span class="sxs-lookup"><span data-stu-id="aeb16-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aeb16-104">SYNTAX</span></span>

### <span data-ttu-id="aeb16-105">Fält</span><span class="sxs-lookup"><span data-stu-id="aeb16-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeb16-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="aeb16-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeb16-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="aeb16-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb16-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aeb16-108">DESCRIPTION</span></span>
<span data-ttu-id="aeb16-109">Cmdleten **Remove-AzureRmDnsRecordSet** tar bort angiven post uppsättning från den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="aeb16-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="aeb16-110">Du kan inte ta bort SOA-eller namnserver poster som skapas automatiskt vid Zone Apex.</span><span class="sxs-lookup"><span data-stu-id="aeb16-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="aeb16-111">Du kan skicka ett **Recordset** -objekt till denna cmdlet med hjälp av en pipeline-operator eller som en parameter.</span><span class="sxs-lookup"><span data-stu-id="aeb16-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="aeb16-112">Om du vill identifiera en post uppsättning efter namn och typ utan att använda ett **Recordset** -objekt måste du överföra zonen som ett **dnsZone** -objekt till denna cmdlet genom att använda pipeline-operatorn eller som en parameter, eller också kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="aeb16-113">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="aeb16-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="aeb16-114">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="aeb16-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="aeb16-115">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="aeb16-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="aeb16-116">Du kan förhindra detta genom att använda parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="aeb16-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="aeb16-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aeb16-117">EXAMPLES</span></span>

### <span data-ttu-id="aeb16-118">Exempel 1: ta bort en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="aeb16-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="aeb16-119">Det första kommandot får den angivna post uppsättningen och lagrar den sedan i $RecordSet variabel. Det andra kommandot tar bort post uppsättningen i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="aeb16-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="aeb16-120">Exempel 2: ta bort en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="aeb16-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="aeb16-121">Det första kommandot får den angivna post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="aeb16-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="aeb16-122">Det andra kommandot tar bort post uppsättningen, även om den har ändrats under tiden.</span><span class="sxs-lookup"><span data-stu-id="aeb16-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="aeb16-123">Bekräftelse uppmaningar ignoreras.</span><span class="sxs-lookup"><span data-stu-id="aeb16-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="aeb16-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aeb16-124">PARAMETERS</span></span>

### <span data-ttu-id="aeb16-125">-Force</span><span class="sxs-lookup"><span data-stu-id="aeb16-125">-Force</span></span>
<span data-ttu-id="aeb16-126">Den här parametern är föråldrad för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeb16-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="aeb16-127">Den kommer att tas bort i en senare version.</span><span class="sxs-lookup"><span data-stu-id="aeb16-127">It will be removed in a future release.</span></span>

<span data-ttu-id="aeb16-128">Om du vill kontrol lera om den här cmdleten uppmanar dig att bekräfta kan du använda parametern *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="aeb16-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="aeb16-129">-Name</span></span>
<span data-ttu-id="aeb16-130">Anger namnet på den **post mängd** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="aeb16-131">När du anger post uppsättningen efter namn måste DNS-zonen anges med parametrarna *Zone* eller *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="aeb16-132">Du kan också ange en post uppsättning med hjälp av ett **Recordset** -objekt som skickas med hjälp av *post mängds* parametern.</span><span class="sxs-lookup"><span data-stu-id="aeb16-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="aeb16-133">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="aeb16-133">-Overwrite</span></span>
<span data-ttu-id="aeb16-134">När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="aeb16-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="aeb16-135">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="aeb16-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="aeb16-136">Det här kan utelämnas med hjälp av parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="aeb16-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="aeb16-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aeb16-137">-PassThru</span></span>
<span data-ttu-id="aeb16-138">passthru</span><span class="sxs-lookup"><span data-stu-id="aeb16-138">passthru</span></span>

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

### <span data-ttu-id="aeb16-139">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="aeb16-139">-RecordSet</span></span>
<span data-ttu-id="aeb16-140">Anger det **Recordset** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="aeb16-141">Du kan också ange post uppsättningen med *namn* -och *zonkod* eller använda parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="aeb16-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="aeb16-142">-RecordType</span></span>
<span data-ttu-id="aeb16-143">Anger typen av DNS-post.</span><span class="sxs-lookup"><span data-stu-id="aeb16-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="aeb16-144">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="aeb16-144">Valid values are:</span></span>

- <span data-ttu-id="aeb16-145">Kallas</span><span class="sxs-lookup"><span data-stu-id="aeb16-145">A</span></span>
- <span data-ttu-id="aeb16-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="aeb16-146">AAAA</span></span>
- <span data-ttu-id="aeb16-147">CNAME</span><span class="sxs-lookup"><span data-stu-id="aeb16-147">CNAME</span></span>
- <span data-ttu-id="aeb16-148">MX</span><span class="sxs-lookup"><span data-stu-id="aeb16-148">MX</span></span>
- <span data-ttu-id="aeb16-149">NS</span><span class="sxs-lookup"><span data-stu-id="aeb16-149">NS</span></span>
- <span data-ttu-id="aeb16-150">RESURSPOST</span><span class="sxs-lookup"><span data-stu-id="aeb16-150">PTR</span></span>
- <span data-ttu-id="aeb16-151">SRV</span><span class="sxs-lookup"><span data-stu-id="aeb16-151">SRV</span></span>
- <span data-ttu-id="aeb16-152">TXT</span><span class="sxs-lookup"><span data-stu-id="aeb16-152">TXT</span></span>

<span data-ttu-id="aeb16-153">SOA-poster tas bort automatiskt när zonen tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="aeb16-154">Du kan inte ta bort SOA-poster manuellt.</span><span class="sxs-lookup"><span data-stu-id="aeb16-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb16-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb16-155">-ResourceGroupName</span></span>
<span data-ttu-id="aeb16-156">Anger den resurs grupp som innehåller den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="aeb16-157">Den här parametern är endast tillämpbar när post uppsättningen och DNS-zonen anges med parametrarna *namn* och *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="aeb16-158">Alternativt kan du ange den post uppsättning som använder parametern *post uppsättning* eller *namn* - *och parameter parametrar* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="aeb16-159">-Zone</span><span class="sxs-lookup"><span data-stu-id="aeb16-159">-Zone</span></span>
<span data-ttu-id="aeb16-160">Anger den DNS-zon som innehåller den **post uppsättning** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="aeb16-161">Den här parametern används endast när du anger en post uppsättning med parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="aeb16-162">Eller så kan du ange den post uppsättning som använder parametern *post uppsättning* eller parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="aeb16-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="aeb16-163">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="aeb16-163">-ZoneName</span></span>
<span data-ttu-id="aeb16-164">Anger namnet på den zon som innehåller **post mängden** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aeb16-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="aeb16-165">Du måste också ange *namnet* och *ResourceGroupName* parametrar.</span><span class="sxs-lookup"><span data-stu-id="aeb16-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="aeb16-166">Du kan också ange post uppsättningen genom att använda parametern *post mängd* eller *namn* *-och parameter* parametrar.</span><span class="sxs-lookup"><span data-stu-id="aeb16-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="aeb16-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aeb16-167">-Confirm</span></span>
<span data-ttu-id="aeb16-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aeb16-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb16-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb16-169">-WhatIf</span></span>
<span data-ttu-id="aeb16-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aeb16-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeb16-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aeb16-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb16-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb16-172">-DefaultProfile</span></span>
<span data-ttu-id="aeb16-173">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb16-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb16-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb16-174">CommonParameters</span></span>
<span data-ttu-id="aeb16-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeb16-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb16-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb16-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb16-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aeb16-177">INPUTS</span></span>

### <span data-ttu-id="aeb16-178">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="aeb16-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="aeb16-179">Du kan **göra en pipe** till den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aeb16-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="aeb16-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aeb16-180">OUTPUTS</span></span>

### <span data-ttu-id="aeb16-181">Ingen</span><span class="sxs-lookup"><span data-stu-id="aeb16-181">None</span></span>
<span data-ttu-id="aeb16-182">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="aeb16-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aeb16-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aeb16-183">NOTES</span></span>
<span data-ttu-id="aeb16-184">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="aeb16-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="aeb16-185">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="aeb16-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="aeb16-186">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="aeb16-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="aeb16-187">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="aeb16-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="aeb16-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aeb16-188">RELATED LINKS</span></span>

[<span data-ttu-id="aeb16-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="aeb16-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="aeb16-190">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="aeb16-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="aeb16-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="aeb16-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
