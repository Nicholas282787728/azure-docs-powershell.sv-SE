---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924577"
---
# <span data-ttu-id="6d620-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6d620-101">New-AzDnsZone</span></span>

## <span data-ttu-id="6d620-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d620-102">SYNOPSIS</span></span>
<span data-ttu-id="6d620-103">Skapar en ny DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="6d620-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="6d620-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d620-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d620-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d620-105">DESCRIPTION</span></span>
<span data-ttu-id="6d620-106">Cmdleten **New-AzDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d620-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="6d620-107">Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="6d620-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="6d620-108">När zonen har skapats kan du använda New-AzDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="6d620-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="6d620-109">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6d620-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6d620-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d620-110">EXAMPLES</span></span>

### <span data-ttu-id="6d620-111">Exempel 1: skapa en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="6d620-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6d620-112">Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="6d620-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="6d620-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d620-113">PARAMETERS</span></span>

### <span data-ttu-id="6d620-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d620-114">-Name</span></span>
<span data-ttu-id="6d620-115">Anger namnet på DNS-zonen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6d620-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d620-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d620-116">-ResourceGroupName</span></span>
<span data-ttu-id="6d620-117">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="6d620-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d620-118">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6d620-118">-Tag</span></span>
<span data-ttu-id="6d620-119">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6d620-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6d620-120">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="6d620-120">For example:</span></span>

<span data-ttu-id="6d620-121">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6d620-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d620-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d620-122">-Confirm</span></span>
<span data-ttu-id="6d620-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d620-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d620-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d620-124">-WhatIf</span></span>
<span data-ttu-id="6d620-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d620-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d620-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d620-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d620-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d620-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d620-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d620-128">CommonParameters</span></span>
<span data-ttu-id="6d620-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d620-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d620-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d620-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d620-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d620-131">INPUTS</span></span>

### <span data-ttu-id="6d620-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="6d620-132">None</span></span>

<span data-ttu-id="6d620-133">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d620-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="6d620-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d620-134">OUTPUTS</span></span>

### <span data-ttu-id="6d620-135">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="6d620-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="6d620-136">Denna cmdlet returnerar ett Microsoft. Azure. commands. DNS. DnsZone-objekt som representerar den nya DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="6d620-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="6d620-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d620-137">NOTES</span></span>
<span data-ttu-id="6d620-138">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6d620-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6d620-139">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="6d620-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6d620-140">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="6d620-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6d620-141">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6d620-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6d620-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d620-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d620-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6d620-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6d620-144">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6d620-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="6d620-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6d620-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)