---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270703"
---
# <span data-ttu-id="b5f3b-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b5f3b-101">New-AzDnsZone</span></span>

## <span data-ttu-id="b5f3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f3b-103">Skapar en ny DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="b5f3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5f3b-104">SYNTAX</span></span>

### <span data-ttu-id="b5f3b-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="b5f3b-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f3b-106">Könamn</span><span class="sxs-lookup"><span data-stu-id="b5f3b-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f3b-107">Objekten</span><span class="sxs-lookup"><span data-stu-id="b5f3b-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f3b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5f3b-108">DESCRIPTION</span></span>
<span data-ttu-id="b5f3b-109">Cmdleten **New-AzDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="b5f3b-110">Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="b5f3b-111">När zonen har skapats kan du använda New-AzDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="b5f3b-112">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b5f3b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5f3b-113">EXAMPLES</span></span>

### <span data-ttu-id="b5f3b-114">Exempel 1: skapa en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="b5f3b-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b5f3b-115">Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b5f3b-116">Exempel 2: skapa en privat DNS-zon genom att ange virtuella nätverks-ID</span><span class="sxs-lookup"><span data-stu-id="b5f3b-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="b5f3b-117">Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (som anger dess ID) och lagrar det sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b5f3b-118">Exempel 3: skapa en privat DNS-zon genom att ange virtuella nätverks objekt</span><span class="sxs-lookup"><span data-stu-id="b5f3b-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="b5f3b-119">Det här kommandot skapar en ny privat DNS-zon som heter myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (kallas $ResVirtualNetwork variabel) och lagrar sedan in det i $Zone-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b5f3b-120">Exempel 4: skapa en DNS-zon med ombud genom att ange namnet på den överordnade zonen</span><span class="sxs-lookup"><span data-stu-id="b5f3b-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="b5f3b-121">Det här kommandot skapar en ny underordnad DNS-zon som heter mychild.zone.com i angiven resurs grupp och butiker i variabeln $Zone.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b5f3b-122">Dessutom läggs delegering till i den överordnade DNS-zonen med namnet zone.com som finns i samma prenumeration och resurs grupp som den underordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="b5f3b-123">Exempel 5: skapa en DNS-zon med delegering genom att ange överordnat zon-ID</span><span class="sxs-lookup"><span data-stu-id="b5f3b-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="b5f3b-124">Det här kommandot skapar en ny underordnad DNS-zon som heter mychild.zone.com i angiven resurs grupp och butiker i variabeln $Zone.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b5f3b-125">Dessutom läggs delegering till i den överordnade DNS-zonen med namnet zone.com i resurs gruppen annat-RG-abonnemang som har angetts som den underordnade zonen har skapat.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="b5f3b-126">Exempel 6: skapa en DNS-zon med delegering genom att ange överordnat Zone-objekt</span><span class="sxs-lookup"><span data-stu-id="b5f3b-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="b5f3b-127">Det här kommandot skapar en ny underordnad DNS-zon som heter mychild.zone.com i angiven resurs grupp och butiker i variabeln $Zone.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="b5f3b-128">Dessutom läggs delegering till i den överordnade DNS-zonen med namnet zone.com som skickades i ParentZone-objektet</span><span class="sxs-lookup"><span data-stu-id="b5f3b-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="b5f3b-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5f3b-129">PARAMETERS</span></span>

### <span data-ttu-id="b5f3b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f3b-130">-DefaultProfile</span></span>
<span data-ttu-id="b5f3b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b5f3b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5f3b-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5f3b-132">-Name</span></span>
<span data-ttu-id="b5f3b-133">Anger namnet på DNS-zonen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="b5f3b-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="b5f3b-134">-ParentZone</span></span>
<span data-ttu-id="b5f3b-135">Det fullständiga namnet på den överordnade zonen för att lägga till delegering (utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="b5f3b-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="b5f3b-136">-ParentZoneId</span></span>
<span data-ttu-id="b5f3b-137">Resurs-ID för den överordnade zonen för att lägga till delegering (utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="b5f3b-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="b5f3b-138">-ParentZoneName</span></span>
<span data-ttu-id="b5f3b-139">Det fullständiga namnet på den överordnade zonen för att lägga till delegering (utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="b5f3b-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b5f3b-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="b5f3b-141">Listan med virtuella nätverk som ska registrera poster för virtuella dator namn i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b5f3b-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="b5f3b-143">Listan över virtuella nätverks-ID: n som registrerar virtuella dator namn poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b5f3b-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="b5f3b-145">Listan med virtuella nätverk som kan lösa poster i den här DNS-zonen, är endast tillgänglig för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b5f3b-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="b5f3b-147">Listan över virtuella nätverks-ID: n som kan användas för att lösa poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f3b-148">-ResourceGroupName</span></span>
<span data-ttu-id="b5f3b-149">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="b5f3b-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b5f3b-150">-Tag</span></span>
<span data-ttu-id="b5f3b-151">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b5f3b-152">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b5f3b-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b5f3b-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="b5f3b-153">-ZoneType</span></span>
<span data-ttu-id="b5f3b-154">Typen av zon, offentlig eller privat.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="b5f3b-155">Zoner utan typ eller med en typ av offentliga tjänster görs tillgängliga för det offentliga DNS-tjänsten för användning i DNS-hierarkin.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="b5f3b-156">Zoner med en typ av privat är bara synliga från med uppsättningen associerade virtuella nätverk (den här funktionen är i för hands version).</span><span class="sxs-lookup"><span data-stu-id="b5f3b-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="b5f3b-157">Det går inte att ändra den här egenskapen för en zon.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5f3b-158">-Confirm</span></span>
<span data-ttu-id="b5f3b-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f3b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f3b-160">-WhatIf</span></span>
<span data-ttu-id="b5f3b-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f3b-162">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f3b-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f3b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f3b-164">CommonParameters</span></span>
<span data-ttu-id="b5f3b-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f3b-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f3b-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f3b-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5f3b-167">INPUTS</span></span>

### <span data-ttu-id="b5f3b-168">System. String</span><span class="sxs-lookup"><span data-stu-id="b5f3b-168">System.String</span></span>

### <span data-ttu-id="b5f3b-169">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b5f3b-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b5f3b-170">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b5f3b-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b5f3b-171">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b5f3b-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b5f3b-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b5f3b-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b5f3b-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5f3b-173">OUTPUTS</span></span>

### <span data-ttu-id="b5f3b-174">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b5f3b-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b5f3b-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5f3b-175">NOTES</span></span>
<span data-ttu-id="b5f3b-176">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b5f3b-177">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b5f3b-178">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b5f3b-179">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b5f3b-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5f3b-180">RELATED LINKS</span></span>

[<span data-ttu-id="b5f3b-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b5f3b-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="b5f3b-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b5f3b-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="b5f3b-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b5f3b-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
