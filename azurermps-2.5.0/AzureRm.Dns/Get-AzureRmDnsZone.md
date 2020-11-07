---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930602"
---
# <span data-ttu-id="95ace-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="95ace-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="95ace-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95ace-102">SYNOPSIS</span></span>
<span data-ttu-id="95ace-103">Hämtar en DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="95ace-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ace-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95ace-104">SYNTAX</span></span>

### <span data-ttu-id="95ace-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="95ace-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="95ace-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95ace-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="95ace-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95ace-107">DESCRIPTION</span></span>
<span data-ttu-id="95ace-108">Cmdleten **Get-AzureRmDnsZone** hämtar en DNS-zon (Domain Name System) från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95ace-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="95ace-109">Om du anger parametern *Name* returneras ett enskilt **dnsZone** -objekt.</span><span class="sxs-lookup"><span data-stu-id="95ace-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="95ace-110">Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95ace-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="95ace-111">Du kan använda **dnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.</span><span class="sxs-lookup"><span data-stu-id="95ace-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="95ace-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95ace-112">EXAMPLES</span></span>

### <span data-ttu-id="95ace-113">Exempel 1: Hämta en zon</span><span class="sxs-lookup"><span data-stu-id="95ace-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="95ace-114">Det här exemplet hämtar DNS-zonen som heter myzone.com från den angivna resurs gruppen och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="95ace-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="95ace-115">Exempel 2: Hämta alla zoner i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="95ace-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="95ace-116">Det här exemplet får alla DNS-zoner i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="95ace-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="95ace-117">Exempel 3: Hämta alla zoner i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="95ace-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="95ace-118">I det här exemplet får du alla DNS-zoner i den aktuella Azure-prenumerationen och lagrar dem i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="95ace-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="95ace-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95ace-119">PARAMETERS</span></span>

### <span data-ttu-id="95ace-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="95ace-120">-Name</span></span>
<span data-ttu-id="95ace-121">Anger namnet på den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="95ace-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="95ace-122">Om du inte anger ett värde för parametern *Name* får denna cmdlet alla DNS-zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95ace-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="95ace-123">Om du också utelämnar parametern *ResourceGroupName* får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="95ace-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ace-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ace-124">-ResourceGroupName</span></span>
<span data-ttu-id="95ace-125">Anger namnet på den resurs grupp som innehåller den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="95ace-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="95ace-126">Om du inte anger *ResourceGroupName* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="95ace-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="95ace-127">I det här fallet får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="95ace-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ace-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ace-128">CommonParameters</span></span>
<span data-ttu-id="95ace-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ace-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ace-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ace-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ace-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95ace-131">INPUTS</span></span>

### <span data-ttu-id="95ace-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="95ace-132">None</span></span>
<span data-ttu-id="95ace-133">Denna cmdlet tillåter inte pipe-inmatning.</span><span class="sxs-lookup"><span data-stu-id="95ace-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="95ace-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95ace-134">OUTPUTS</span></span>

### <span data-ttu-id="95ace-135">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="95ace-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="95ace-136">Denna cmdlet returnerar ett objekt som representerar DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="95ace-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="95ace-137">Om inget zonnamn anges returneras en matris med zon objekt.</span><span class="sxs-lookup"><span data-stu-id="95ace-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="95ace-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95ace-138">NOTES</span></span>

## <span data-ttu-id="95ace-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95ace-139">RELATED LINKS</span></span>

[<span data-ttu-id="95ace-140">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="95ace-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="95ace-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="95ace-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="95ace-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="95ace-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
