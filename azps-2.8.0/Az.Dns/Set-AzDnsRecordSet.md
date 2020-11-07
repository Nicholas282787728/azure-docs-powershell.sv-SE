---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: c57377156acbf908825638e13f139114fa5d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744271"
---
# <span data-ttu-id="d59d5-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="d59d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d59d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d59d5-103">Uppdaterar en DNS-post.</span><span class="sxs-lookup"><span data-stu-id="d59d5-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="d59d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d59d5-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d59d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d59d5-105">DESCRIPTION</span></span>
<span data-ttu-id="d59d5-106">Cmdleten **set-AzDnsRecordSet** uppdaterar en post uppsättning i Azure DNS-tjänsten från ett lokalt **Recordset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d59d5-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="d59d5-107">Du kan skicka ett **Recordset** -objekt som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d59d5-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="d59d5-108">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d59d5-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d59d5-109">Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="d59d5-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d59d5-110">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="d59d5-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d59d5-111">Du kan dölja den här funktionen med hjälp av parametern *Overwrite* , som uppdaterar post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="d59d5-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d59d5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d59d5-112">EXAMPLES</span></span>

### <span data-ttu-id="d59d5-113">Exempel 1: uppdatera en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="d59d5-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="d59d5-114">Det första kommandot använder cmdleten Get-AzDnsRecordSet för att hämta angiven post uppsättning och lagrar den sedan i $RecordSet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d59d5-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d59d5-115">De andra och tredje kommandona är offline-operationer för att lägga till två poster i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d59d5-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="d59d5-116">I det sista kommandot används cmdleten **set-AzDnsRecordSet** för att bekräfta uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="d59d5-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="d59d5-117">Exempel 2: uppdatera en SOA-post</span><span class="sxs-lookup"><span data-stu-id="d59d5-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="d59d5-118">Det första kommandot använder cmdleten **Get-AzDnsRecordset** för att hämta angiven post uppsättning och lagrar den sedan i $Recordset variabel.</span><span class="sxs-lookup"><span data-stu-id="d59d5-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d59d5-119">Det andra kommandot uppdaterar den angivna SOA-posten i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d59d5-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="d59d5-120">Det sista kommandot använder cmdleten **set-AzDnsRecordSet** för att sprida uppdateringen i $Recordset.</span><span class="sxs-lookup"><span data-stu-id="d59d5-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d59d5-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d59d5-121">PARAMETERS</span></span>

### <span data-ttu-id="d59d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59d5-122">-DefaultProfile</span></span>
<span data-ttu-id="d59d5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d59d5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d59d5-124">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="d59d5-124">-Overwrite</span></span>
<span data-ttu-id="d59d5-125">Anger att post uppsättningen ska uppdateras oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="d59d5-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="d59d5-126">Post uppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="d59d5-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d59d5-127">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="d59d5-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d59d5-128">För att förhindra att det här beteendet visas kan du använda parametern *Overwrite* , som leder till att post uppsättningen uppdateras oberoende av de ändringar du gör.</span><span class="sxs-lookup"><span data-stu-id="d59d5-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d59d5-129">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="d59d5-129">-RecordSet</span></span>
<span data-ttu-id="d59d5-130">Anger den **post mängd** som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d59d5-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d59d5-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d59d5-131">-Confirm</span></span>
<span data-ttu-id="d59d5-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d59d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d59d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d59d5-133">-WhatIf</span></span>
<span data-ttu-id="d59d5-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d59d5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d59d5-135">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d59d5-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d59d5-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d59d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d59d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59d5-137">CommonParameters</span></span>
<span data-ttu-id="d59d5-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59d5-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59d5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59d5-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d59d5-140">INPUTS</span></span>

### <span data-ttu-id="d59d5-141">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="d59d5-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d59d5-142">OUTPUTS</span></span>

### <span data-ttu-id="d59d5-143">Microsoft. Azure. commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="d59d5-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d59d5-144">NOTES</span></span>
<span data-ttu-id="d59d5-145">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d59d5-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d59d5-146">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="d59d5-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="d59d5-147">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="d59d5-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d59d5-148">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d59d5-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="d59d5-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d59d5-149">RELATED LINKS</span></span>

[<span data-ttu-id="d59d5-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="d59d5-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="d59d5-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d59d5-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)