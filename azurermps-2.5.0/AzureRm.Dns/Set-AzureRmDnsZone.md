---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 347f590ecd6e2825264e6bb0b980dd94450b0f06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929917"
---
# <span data-ttu-id="be5c2-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="be5c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="be5c2-103">Uppdaterar egenskaperna för en DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="be5c2-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be5c2-104">SYNTAX</span></span>

### <span data-ttu-id="be5c2-105">Fält</span><span class="sxs-lookup"><span data-stu-id="be5c2-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be5c2-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="be5c2-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be5c2-107">DESCRIPTION</span></span>
<span data-ttu-id="be5c2-108">Cmdleten **set-AzureRmDnsZone** uppdaterar den angivna DNS-zonen i Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="be5c2-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="be5c2-109">Denna cmdlet uppdaterar inte post uppsättningarna i zonen.</span><span class="sxs-lookup"><span data-stu-id="be5c2-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="be5c2-110">Du kan skicka ett **dnsZone** -objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="be5c2-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="be5c2-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="be5c2-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="be5c2-112">När du skickar en DNS-zon som ett objekt (med målobjektet eller pipeline) uppdateras den inte om den har ändrats i Azure DNS sedan det lokala DnsZone-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="be5c2-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="be5c2-113">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="be5c2-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="be5c2-114">Du kan förhindra detta med den *överskrivnings* parameter som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="be5c2-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="be5c2-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be5c2-115">EXAMPLES</span></span>

### <span data-ttu-id="be5c2-116">Exempel 1: uppdatera en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="be5c2-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="be5c2-117">Det första kommandot får zonen som heter myzone.com från angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="be5c2-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="be5c2-118">Det andra kommandot uppdaterar taggarna för $Zone.</span><span class="sxs-lookup"><span data-stu-id="be5c2-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="be5c2-119">Det slutliga kommandot utför ändringen.</span><span class="sxs-lookup"><span data-stu-id="be5c2-119">The final command commits the change.</span></span>

### <span data-ttu-id="be5c2-120">Exempel 2: uppdatera taggar för en zon</span><span class="sxs-lookup"><span data-stu-id="be5c2-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="be5c2-121">Det här kommandot uppdaterar taggarna för zonen med namnet myzone.com utan att först explicit komma åt zonen.</span><span class="sxs-lookup"><span data-stu-id="be5c2-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="be5c2-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be5c2-122">PARAMETERS</span></span>

### <span data-ttu-id="be5c2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="be5c2-123">-Name</span></span>
<span data-ttu-id="be5c2-124">Anger namnet på den DNS-zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="be5c2-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="be5c2-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="be5c2-125">-Overwrite</span></span>
<span data-ttu-id="be5c2-126">När du skickar en DNS-zon som ett objekt (med målobjektet eller pipeline) uppdateras den inte om den har ändrats i Azure DNS sedan det lokala DnsZone-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="be5c2-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="be5c2-127">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="be5c2-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="be5c2-128">Du kan förhindra detta med den *överskrivnings* parameter som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="be5c2-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="be5c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="be5c2-130">Anger namnet på den resurs grupp som innehåller den zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="be5c2-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="be5c2-131">Du måste också ange parametern zonnamn.</span><span class="sxs-lookup"><span data-stu-id="be5c2-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="be5c2-132">Alternativt kan du ange zonen med hjälp av ett DnsZone-objekt med parametern *Zone* eller pipeline.</span><span class="sxs-lookup"><span data-stu-id="be5c2-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="be5c2-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="be5c2-133">-Tag</span></span>
<span data-ttu-id="be5c2-134">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="be5c2-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="be5c2-135">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="be5c2-135">For example:</span></span>

<span data-ttu-id="be5c2-136">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="be5c2-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5c2-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="be5c2-137">-Zone</span></span>
<span data-ttu-id="be5c2-138">Anger den DNS-zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="be5c2-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="be5c2-139">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="be5c2-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="be5c2-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be5c2-140">-Confirm</span></span>
<span data-ttu-id="be5c2-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be5c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be5c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5c2-142">-WhatIf</span></span>
<span data-ttu-id="be5c2-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be5c2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be5c2-144">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be5c2-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be5c2-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be5c2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be5c2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5c2-146">CommonParameters</span></span>
<span data-ttu-id="be5c2-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5c2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5c2-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5c2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5c2-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be5c2-149">INPUTS</span></span>

### <span data-ttu-id="be5c2-150">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="be5c2-151">Du kan ha ett DnsZone-objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be5c2-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="be5c2-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be5c2-152">OUTPUTS</span></span>

### <span data-ttu-id="be5c2-153">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="be5c2-154">Denna cmdlet returnerar ett DnsZone-objekt som representerar den uppdaterade DNS-zonen med en ny etag.</span><span class="sxs-lookup"><span data-stu-id="be5c2-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="be5c2-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be5c2-155">NOTES</span></span>
<span data-ttu-id="be5c2-156">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="be5c2-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="be5c2-157">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="be5c2-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="be5c2-158">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="be5c2-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="be5c2-159">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="be5c2-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="be5c2-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be5c2-160">RELATED LINKS</span></span>

[<span data-ttu-id="be5c2-161">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-161">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="be5c2-162">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-162">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="be5c2-163">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="be5c2-163">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
