---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102872"
---
# <span data-ttu-id="c70e5-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c70e5-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="c70e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c70e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c70e5-103">Hämtar en DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="c70e5-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="c70e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c70e5-104">SYNTAX</span></span>

### <span data-ttu-id="c70e5-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c70e5-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c70e5-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c70e5-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c70e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c70e5-107">DESCRIPTION</span></span>
<span data-ttu-id="c70e5-108">Cmdleten **Get-AzDnsZone** hämtar en DNS-zon (Domain Name System) från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c70e5-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="c70e5-109">Om du anger parametern *Name* returneras ett enskilt **dnsZone** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c70e5-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="c70e5-110">Om du inte anger parametern *Name* returneras en matris med alla zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c70e5-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="c70e5-111">Du kan använda **dnsZone** -objektet för att uppdatera zonen, till exempel att du kan lägga till **Recordset** -objekt i den.</span><span class="sxs-lookup"><span data-stu-id="c70e5-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="c70e5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c70e5-112">EXAMPLES</span></span>

### <span data-ttu-id="c70e5-113">Exempel 1: Hämta en zon</span><span class="sxs-lookup"><span data-stu-id="c70e5-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="c70e5-114">Det här exemplet hämtar DNS-zonen som heter myzone.com från den angivna resurs gruppen och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="c70e5-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="c70e5-115">Exempel 2: Hämta alla zoner i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c70e5-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c70e5-116">Det här exemplet får alla DNS-zoner i den angivna resurs gruppen och lagrar dem sedan i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="c70e5-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="c70e5-117">Exempel 3: Hämta alla zoner i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c70e5-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="c70e5-118">I det här exemplet får du alla DNS-zoner i den aktuella Azure-prenumerationen och lagrar dem i $Zones variabel.</span><span class="sxs-lookup"><span data-stu-id="c70e5-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="c70e5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c70e5-119">PARAMETERS</span></span>

### <span data-ttu-id="c70e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70e5-120">-DefaultProfile</span></span>
<span data-ttu-id="c70e5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c70e5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c70e5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c70e5-122">-Name</span></span>
<span data-ttu-id="c70e5-123">Anger namnet på den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c70e5-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="c70e5-124">Om du inte anger ett värde för parametern *Name* får denna cmdlet alla DNS-zoner i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c70e5-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="c70e5-125">Om du också utelämnar parametern *ResourceGroupName* får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c70e5-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c70e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c70e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="c70e5-127">Anger namnet på den resurs grupp som innehåller den DNS-zon som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c70e5-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="c70e5-128">Om du inte anger *ResourceGroupName* måste du också utelämna parametern *Name* .</span><span class="sxs-lookup"><span data-stu-id="c70e5-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="c70e5-129">I det här fallet får denna cmdlet alla DNS-zoner i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c70e5-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c70e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70e5-130">CommonParameters</span></span>
<span data-ttu-id="c70e5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c70e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70e5-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c70e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70e5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c70e5-133">INPUTS</span></span>

### <span data-ttu-id="c70e5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c70e5-134">System.String</span></span>

## <span data-ttu-id="c70e5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c70e5-135">OUTPUTS</span></span>

### <span data-ttu-id="c70e5-136">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="c70e5-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c70e5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c70e5-137">NOTES</span></span>

## <span data-ttu-id="c70e5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c70e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="c70e5-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c70e5-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c70e5-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c70e5-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="c70e5-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c70e5-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
