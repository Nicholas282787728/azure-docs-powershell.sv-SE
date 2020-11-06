---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581432"
---
# <span data-ttu-id="72c76-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="72c76-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="72c76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72c76-102">SYNOPSIS</span></span>
<span data-ttu-id="72c76-103">Skapar en ny DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="72c76-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72c76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72c76-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72c76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72c76-105">DESCRIPTION</span></span>
<span data-ttu-id="72c76-106">Cmdleten **New-AzureRmDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72c76-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="72c76-107">Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="72c76-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="72c76-108">När zonen har skapats kan du använda New-AzureRmDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="72c76-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="72c76-109">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="72c76-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="72c76-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72c76-110">EXAMPLES</span></span>

### <span data-ttu-id="72c76-111">Exempel 1: skapa en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="72c76-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="72c76-112">Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="72c76-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="72c76-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72c76-113">PARAMETERS</span></span>

### <span data-ttu-id="72c76-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="72c76-114">-Name</span></span>
<span data-ttu-id="72c76-115">Anger namnet på DNS-zonen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="72c76-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c76-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c76-116">-ResourceGroupName</span></span>
<span data-ttu-id="72c76-117">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="72c76-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c76-118">-Tagg</span><span class="sxs-lookup"><span data-stu-id="72c76-118">-Tag</span></span>
<span data-ttu-id="72c76-119">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="72c76-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72c76-120">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="72c76-120">For example:</span></span>

<span data-ttu-id="72c76-121">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="72c76-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c76-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72c76-122">-Confirm</span></span>
<span data-ttu-id="72c76-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72c76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c76-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c76-124">-WhatIf</span></span>
<span data-ttu-id="72c76-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72c76-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72c76-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72c76-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72c76-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72c76-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c76-128">-DefaultProfile</span></span>
<span data-ttu-id="72c76-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72c76-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c76-130">CommonParameters</span></span>
<span data-ttu-id="72c76-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c76-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c76-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c76-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72c76-133">INPUTS</span></span>

### <span data-ttu-id="72c76-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="72c76-134">None</span></span>
<span data-ttu-id="72c76-135">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c76-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="72c76-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72c76-136">OUTPUTS</span></span>

### <span data-ttu-id="72c76-137">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="72c76-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="72c76-138">Denna cmdlet returnerar ett Microsoft. Azure. commands. DNS. DnsZone-objekt som representerar den nya DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="72c76-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="72c76-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72c76-139">NOTES</span></span>
<span data-ttu-id="72c76-140">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="72c76-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="72c76-141">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="72c76-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="72c76-142">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="72c76-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="72c76-143">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="72c76-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="72c76-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72c76-144">RELATED LINKS</span></span>

[<span data-ttu-id="72c76-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="72c76-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="72c76-146">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72c76-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="72c76-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="72c76-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
