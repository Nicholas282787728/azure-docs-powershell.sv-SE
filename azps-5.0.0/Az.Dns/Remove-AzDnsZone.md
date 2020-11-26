---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270698"
---
# <span data-ttu-id="d5841-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d5841-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="d5841-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5841-102">SYNOPSIS</span></span>
<span data-ttu-id="d5841-103">Tar bort en DNS-zon från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d5841-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="d5841-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5841-104">SYNTAX</span></span>

### <span data-ttu-id="d5841-105">Fält</span><span class="sxs-lookup"><span data-stu-id="d5841-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5841-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="d5841-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5841-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5841-107">DESCRIPTION</span></span>
<span data-ttu-id="d5841-108">Cmdleten **Remove-AzDnsZone** tar permanent bort en DNS-zon (Domain Name System) från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d5841-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="d5841-109">Alla post uppsättningar i zonen tas också bort.</span><span class="sxs-lookup"><span data-stu-id="d5841-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="d5841-110">Du kan skicka ett **dnsZone** -objekt med parametern *Name* eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d5841-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d5841-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d5841-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d5841-112">När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="d5841-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="d5841-113">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="d5841-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="d5841-114">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="d5841-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="d5841-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5841-115">EXAMPLES</span></span>

### <span data-ttu-id="d5841-116">Exempel 1: ta bort en zon</span><span class="sxs-lookup"><span data-stu-id="d5841-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d5841-117">Det här kommandot tar bort zonen med namnet myzone.com från resurs gruppen som heter MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d5841-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d5841-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5841-118">PARAMETERS</span></span>

### <span data-ttu-id="d5841-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5841-119">-DefaultProfile</span></span>
<span data-ttu-id="d5841-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d5841-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5841-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5841-121">-Name</span></span>
<span data-ttu-id="d5841-122">Anger namnet på den DNS-zon som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d5841-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="d5841-123">Du måste också ange parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d5841-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="d5841-124">Alternativt kan du ange DNS-zonen med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="d5841-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d5841-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="d5841-125">-Overwrite</span></span>
<span data-ttu-id="d5841-126">När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="d5841-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="d5841-127">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="d5841-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="d5841-128">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="d5841-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d5841-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5841-129">-PassThru</span></span>
<span data-ttu-id="d5841-130">passthru</span><span class="sxs-lookup"><span data-stu-id="d5841-130">passthru</span></span>

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

### <span data-ttu-id="d5841-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5841-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5841-132">Anger namnet på den resurs grupp som innehåller den zon som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d5841-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="d5841-133">Du måste också ange parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="d5841-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="d5841-134">Alternativt kan du ange DNS-zonen med ett **dnsZone** -objekt, som skickas via pipelinen eller parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="d5841-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d5841-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="d5841-135">-Zone</span></span>
<span data-ttu-id="d5841-136">Anger den DNS-zon som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d5841-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="d5841-137">Det **dnsZone** -objekt som skickades kan också överföras via pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5841-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="d5841-138">Alternativt kan du ange vilken DNS-zon som ska tas bort med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d5841-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="d5841-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5841-139">-Confirm</span></span>
<span data-ttu-id="d5841-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5841-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5841-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5841-141">-WhatIf</span></span>
<span data-ttu-id="d5841-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5841-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5841-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5841-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5841-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5841-144">CommonParameters</span></span>
<span data-ttu-id="d5841-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5841-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5841-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5841-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5841-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5841-147">INPUTS</span></span>

### <span data-ttu-id="d5841-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d5841-148">System.String</span></span>

### <span data-ttu-id="d5841-149">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="d5841-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="d5841-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5841-150">OUTPUTS</span></span>

### <span data-ttu-id="d5841-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5841-151">System.Boolean</span></span>

## <span data-ttu-id="d5841-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5841-152">NOTES</span></span>
<span data-ttu-id="d5841-153">På grund av den potentiellt omfattande effekten av att ta bort en DNS-zon ber den här cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har något annat värde än none.</span><span class="sxs-lookup"><span data-stu-id="d5841-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="d5841-154">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="d5841-154">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d5841-155">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d5841-155">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="d5841-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5841-156">RELATED LINKS</span></span>

[<span data-ttu-id="d5841-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d5841-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="d5841-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d5841-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="d5841-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="d5841-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)