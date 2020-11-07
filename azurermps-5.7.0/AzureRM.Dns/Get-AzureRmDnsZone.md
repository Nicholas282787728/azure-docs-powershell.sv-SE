---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756512"
---
# <span data-ttu-id="0073f-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0073f-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="0073f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0073f-102">SYNOPSIS</span></span>
<span data-ttu-id="0073f-103">Hämtar en DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="0073f-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0073f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0073f-104">SYNTAX</span></span>

### <span data-ttu-id="0073f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="0073f-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0073f-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0073f-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0073f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0073f-107">DESCRIPTION</span></span>
<span data-ttu-id="0073f-108">Cmdleten **Get-AzureRmDnsZone** hämtar en DNS-zon (Domain Name System) från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0073f-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="0073f-109">Om du anger parametern *Name* returneras ett enskilt **dnsZone** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0073f-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="0073f-110">Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0073f-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="0073f-111">Du kan använda **dnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.</span><span class="sxs-lookup"><span data-stu-id="0073f-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="0073f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0073f-112">EXAMPLES</span></span>

### <span data-ttu-id="0073f-113">Exempel 1: Hämta en zon</span><span class="sxs-lookup"><span data-stu-id="0073f-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="0073f-114">Det här exemplet hämtar DNS-zonen som heter myzone.com från den angivna resurs gruppen och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="0073f-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="0073f-115">Exempel 2: Hämta alla zoner i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0073f-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0073f-116">Det här exemplet får alla DNS-zoner i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="0073f-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="0073f-117">Exempel 3: Hämta alla zoner i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="0073f-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="0073f-118">I det här exemplet får du alla DNS-zoner i den aktuella Azure-prenumerationen och lagrar dem i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="0073f-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="0073f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0073f-119">PARAMETERS</span></span>

### <span data-ttu-id="0073f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0073f-120">-DefaultProfile</span></span>
<span data-ttu-id="0073f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0073f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0073f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0073f-122">-Name</span></span>
<span data-ttu-id="0073f-123">Anger namnet på den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0073f-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="0073f-124">Om du inte anger ett värde för parametern *Name* får denna cmdlet alla DNS-zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0073f-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="0073f-125">Om du också utelämnar parametern *ResourceGroupName* får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0073f-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="0073f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0073f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0073f-127">Anger namnet på den resurs grupp som innehåller den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0073f-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="0073f-128">Om du inte anger *ResourceGroupName* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="0073f-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="0073f-129">I det här fallet får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0073f-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="0073f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0073f-130">CommonParameters</span></span>
<span data-ttu-id="0073f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0073f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0073f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0073f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0073f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0073f-133">INPUTS</span></span>

### <span data-ttu-id="0073f-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="0073f-134">None</span></span>
<span data-ttu-id="0073f-135">Denna cmdlet tillåter inte pipe-inmatning.</span><span class="sxs-lookup"><span data-stu-id="0073f-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="0073f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0073f-136">OUTPUTS</span></span>

### <span data-ttu-id="0073f-137">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0073f-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0073f-138">Denna cmdlet returnerar ett objekt som representerar DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="0073f-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="0073f-139">Om inget zonnamn anges returneras en matris med zon objekt.</span><span class="sxs-lookup"><span data-stu-id="0073f-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="0073f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0073f-140">NOTES</span></span>

## <span data-ttu-id="0073f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0073f-141">RELATED LINKS</span></span>

[<span data-ttu-id="0073f-142">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0073f-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="0073f-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0073f-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="0073f-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0073f-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
