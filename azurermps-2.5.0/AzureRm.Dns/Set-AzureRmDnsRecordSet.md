---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c6479f9358322ae76eeb2fdf3cb9f2bb922e462
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929430"
---
# <span data-ttu-id="9418b-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="9418b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9418b-102">SYNOPSIS</span></span>
<span data-ttu-id="9418b-103">Uppdaterar en DNS-post.</span><span class="sxs-lookup"><span data-stu-id="9418b-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9418b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9418b-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9418b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9418b-105">DESCRIPTION</span></span>
<span data-ttu-id="9418b-106">Cmdleten **set-AzureRmDnsRecordSet** uppdaterar en post uppsättning i Azure DNS-tjänsten från ett lokalt **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9418b-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="9418b-107">Du kan skicka ett **Recordset** -objekt som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="9418b-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="9418b-108">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9418b-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="9418b-109">Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="9418b-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="9418b-110">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="9418b-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="9418b-111">Du kan dölja den här funktionen med hjälp av parametern *Overwrite* , som uppdaterar post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="9418b-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="9418b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9418b-112">EXAMPLES</span></span>

### <span data-ttu-id="9418b-113">Exempel 1: uppdatera en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9418b-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="9418b-114">Det första kommandot använder cmdleten Get-AzureRmDnsRecordSet för att hämta angiven post uppsättning och lagrar den sedan i $RecordSet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="9418b-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="9418b-115">De andra och tredje kommandona är offline-operationer för att lägga till två poster i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="9418b-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="9418b-116">I det sista kommandot används cmdleten **set-AzureRmDnsRecordSet** för att bekräfta uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="9418b-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="9418b-117">Exempel 2: uppdatera en SOA-post</span><span class="sxs-lookup"><span data-stu-id="9418b-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="9418b-118">Det första kommandot använder cmdleten **Get-AzureRmDnsRecordset** för att hämta angiven post uppsättning och lagrar den sedan i $Recordset variabel.</span><span class="sxs-lookup"><span data-stu-id="9418b-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="9418b-119">Det andra kommandot uppdaterar den angivna SOA-posten i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="9418b-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="9418b-120">Det sista kommandot använder cmdleten **set-AzureRmDnsRecordSet** för att sprida uppdateringen i $Recordset.</span><span class="sxs-lookup"><span data-stu-id="9418b-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="9418b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9418b-121">PARAMETERS</span></span>

### <span data-ttu-id="9418b-122">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="9418b-122">-Overwrite</span></span>
<span data-ttu-id="9418b-123">Anger att post uppsättningen ska uppdateras oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="9418b-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="9418b-124">Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="9418b-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="9418b-125">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="9418b-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="9418b-126">För att förhindra att det här beteendet visas kan du använda parametern *Overwrite* , som leder till att post uppsättningen uppdateras oberoende av de ändringar du gör.</span><span class="sxs-lookup"><span data-stu-id="9418b-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="9418b-127">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="9418b-127">-RecordSet</span></span>
<span data-ttu-id="9418b-128">Anger den **post mängd** som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="9418b-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9418b-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9418b-129">-Confirm</span></span>
<span data-ttu-id="9418b-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9418b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9418b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9418b-131">-WhatIf</span></span>
<span data-ttu-id="9418b-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9418b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9418b-133">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9418b-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9418b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9418b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9418b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9418b-135">CommonParameters</span></span>
<span data-ttu-id="9418b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9418b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9418b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9418b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9418b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9418b-138">INPUTS</span></span>

### <span data-ttu-id="9418b-139">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9418b-140">Du kan skicka ett **Recordset** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9418b-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="9418b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9418b-141">OUTPUTS</span></span>

### <span data-ttu-id="9418b-142">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9418b-143">Denna cmdlet returnerar ett objekt som representerar det uppdaterade **Recordset** -objektet.</span><span class="sxs-lookup"><span data-stu-id="9418b-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="9418b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9418b-144">NOTES</span></span>
<span data-ttu-id="9418b-145">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9418b-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9418b-146">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="9418b-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="9418b-147">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="9418b-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="9418b-148">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9418b-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="9418b-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9418b-149">RELATED LINKS</span></span>

[<span data-ttu-id="9418b-150">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-150">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="9418b-151">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-151">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="9418b-152">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9418b-152">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
