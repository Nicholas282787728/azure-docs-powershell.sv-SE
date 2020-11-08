---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922966"
---
# <span data-ttu-id="42251-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="42251-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="42251-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42251-102">SYNOPSIS</span></span>
<span data-ttu-id="42251-103">Tar bort en DNS-zon från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="42251-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="42251-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42251-104">SYNTAX</span></span>

### <span data-ttu-id="42251-105">Fält</span><span class="sxs-lookup"><span data-stu-id="42251-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42251-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="42251-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42251-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42251-107">DESCRIPTION</span></span>
<span data-ttu-id="42251-108">Cmdleten **Remove-AzDnsZone** tar permanent bort en DNS-zon (Domain Name System) från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="42251-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="42251-109">Alla post uppsättningar i zonen tas också bort.</span><span class="sxs-lookup"><span data-stu-id="42251-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="42251-110">Du kan skicka ett **dnsZone** -objekt med parametern *Name* eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="42251-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="42251-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="42251-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="42251-112">När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="42251-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="42251-113">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="42251-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="42251-114">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="42251-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="42251-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42251-115">EXAMPLES</span></span>

### <span data-ttu-id="42251-116">Exempel 1: ta bort en zon</span><span class="sxs-lookup"><span data-stu-id="42251-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="42251-117">Det här kommandot tar bort zonen med namnet myzone.com från resurs gruppen som heter MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42251-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="42251-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42251-118">PARAMETERS</span></span>

### <span data-ttu-id="42251-119">-Force</span><span class="sxs-lookup"><span data-stu-id="42251-119">-Force</span></span>
<span data-ttu-id="42251-120">Den här parametern är föråldrad för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42251-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="42251-121">Den kommer att tas bort i en senare version.</span><span class="sxs-lookup"><span data-stu-id="42251-121">It will be removed in a future release.</span></span>

<span data-ttu-id="42251-122">Om du vill kontrol lera om den här cmdleten uppmanar dig att bekräfta kan du använda parametern *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="42251-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="42251-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="42251-123">-Name</span></span>
<span data-ttu-id="42251-124">Anger namnet på den DNS-zon som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="42251-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="42251-125">Du måste också ange parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="42251-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="42251-126">Alternativt kan du ange DNS-zonen med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="42251-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="42251-127">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="42251-127">-Overwrite</span></span>
<span data-ttu-id="42251-128">När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="42251-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="42251-129">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="42251-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="42251-130">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="42251-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="42251-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42251-131">-PassThru</span></span>
<span data-ttu-id="42251-132">passthru</span><span class="sxs-lookup"><span data-stu-id="42251-132">passthru</span></span>

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

### <span data-ttu-id="42251-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42251-133">-ResourceGroupName</span></span>
<span data-ttu-id="42251-134">Anger namnet på den resurs grupp som innehåller den zon som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="42251-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="42251-135">Du måste också ange parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="42251-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="42251-136">Alternativt kan du ange DNS-zonen med ett **dnsZone** -objekt, som skickas via pipelinen eller parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="42251-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="42251-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="42251-137">-Zone</span></span>
<span data-ttu-id="42251-138">Anger den DNS-zon som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="42251-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="42251-139">Det **dnsZone** -objekt som skickades kan också överföras via pipeline.</span><span class="sxs-lookup"><span data-stu-id="42251-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="42251-140">Alternativt kan du ange vilken DNS-zon som ska tas bort med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="42251-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="42251-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42251-141">-Confirm</span></span>
<span data-ttu-id="42251-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42251-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42251-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42251-143">-WhatIf</span></span>
<span data-ttu-id="42251-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42251-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42251-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42251-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42251-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42251-146">CommonParameters</span></span>
<span data-ttu-id="42251-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42251-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42251-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42251-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42251-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42251-149">INPUTS</span></span>

### <span data-ttu-id="42251-150">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="42251-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="42251-151">Du kan ha ett **dnsZone** -objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42251-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="42251-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42251-152">OUTPUTS</span></span>

### <span data-ttu-id="42251-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="42251-153">None</span></span>
<span data-ttu-id="42251-154">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="42251-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="42251-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42251-155">NOTES</span></span>
<span data-ttu-id="42251-156">På grund av den potentiellt omfattande effekten av att ta bort en DNS-zon ber den här cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har något annat värde än none.</span><span class="sxs-lookup"><span data-stu-id="42251-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="42251-157">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="42251-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="42251-158">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="42251-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="42251-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42251-159">RELATED LINKS</span></span>

[<span data-ttu-id="42251-160">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="42251-160">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="42251-161">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="42251-161">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="42251-162">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="42251-162">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)