---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754121"
---
# <span data-ttu-id="cc151-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc151-101">New-AzDnsZone</span></span>

## <span data-ttu-id="cc151-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc151-102">SYNOPSIS</span></span>
<span data-ttu-id="cc151-103">Skapar en ny DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="cc151-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="cc151-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc151-104">SYNTAX</span></span>

### <span data-ttu-id="cc151-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="cc151-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc151-106">Objekten</span><span class="sxs-lookup"><span data-stu-id="cc151-106">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc151-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc151-107">DESCRIPTION</span></span>
<span data-ttu-id="cc151-108">Cmdleten **New-AzDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc151-108">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="cc151-109">Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="cc151-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="cc151-110">När zonen har skapats kan du använda New-AzDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="cc151-110">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="cc151-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cc151-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cc151-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc151-112">EXAMPLES</span></span>

### <span data-ttu-id="cc151-113">Exempel 1: skapa en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="cc151-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="cc151-114">Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="cc151-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="cc151-115">Exempel 2: skapa en privat DNS-zon genom att ange virtuella nätverks-ID</span><span class="sxs-lookup"><span data-stu-id="cc151-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="cc151-116">Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (som anger dess ID) och lagrar det sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="cc151-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="cc151-117">Exempel 3: skapa en privat DNS-zon genom att ange virtuella nätverks objekt</span><span class="sxs-lookup"><span data-stu-id="cc151-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="cc151-118">Det här kommandot skapar en ny privat DNS-zon som heter myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (kallas $ResVirtualNetwork variabel) och lagrar sedan in det i $Zone-variabeln.</span><span class="sxs-lookup"><span data-stu-id="cc151-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="cc151-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc151-119">PARAMETERS</span></span>

### <span data-ttu-id="cc151-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc151-120">-DefaultProfile</span></span>
<span data-ttu-id="cc151-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cc151-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc151-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc151-122">-Name</span></span>
<span data-ttu-id="cc151-123">Anger namnet på DNS-zonen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cc151-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="cc151-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc151-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="cc151-125">Listan med virtuella nätverk som ska registrera poster för virtuella dator namn i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="cc151-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cc151-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cc151-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="cc151-127">Listan över virtuella nätverks-ID: n som registrerar virtuella dator namn poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="cc151-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cc151-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cc151-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="cc151-129">Listan med virtuella nätverk som kan lösa poster i den här DNS-zonen, är endast tillgänglig för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="cc151-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cc151-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cc151-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="cc151-131">Listan över virtuella nätverks-ID: n som kan användas för att lösa poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="cc151-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cc151-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc151-132">-ResourceGroupName</span></span>
<span data-ttu-id="cc151-133">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="cc151-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="cc151-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cc151-134">-Tag</span></span>
<span data-ttu-id="cc151-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cc151-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc151-136">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="cc151-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cc151-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="cc151-137">-ZoneType</span></span>
<span data-ttu-id="cc151-138">Typen av zon, offentlig eller privat.</span><span class="sxs-lookup"><span data-stu-id="cc151-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="cc151-139">Zoner utan typ eller med en typ av offentliga tjänster görs tillgängliga för det offentliga DNS-tjänsten för användning i DNS-hierarkin.</span><span class="sxs-lookup"><span data-stu-id="cc151-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="cc151-140">Zoner med en typ av privat är bara synliga från med uppsättningen associerade virtuella nätverk (den här funktionen är i för hands version).</span><span class="sxs-lookup"><span data-stu-id="cc151-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="cc151-141">Det går inte att ändra den här egenskapen för en zon.</span><span class="sxs-lookup"><span data-stu-id="cc151-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="cc151-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc151-142">-Confirm</span></span>
<span data-ttu-id="cc151-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc151-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc151-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc151-144">-WhatIf</span></span>
<span data-ttu-id="cc151-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc151-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc151-146">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc151-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc151-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc151-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc151-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc151-148">CommonParameters</span></span>
<span data-ttu-id="cc151-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc151-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc151-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc151-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc151-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc151-151">INPUTS</span></span>

### <span data-ttu-id="cc151-152">System. String</span><span class="sxs-lookup"><span data-stu-id="cc151-152">System.String</span></span>

### <span data-ttu-id="cc151-153">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cc151-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cc151-154">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cc151-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cc151-155">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc151-155">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc151-156">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cc151-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="cc151-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc151-157">OUTPUTS</span></span>

### <span data-ttu-id="cc151-158">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="cc151-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="cc151-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc151-159">NOTES</span></span>
<span data-ttu-id="cc151-160">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cc151-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="cc151-161">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="cc151-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="cc151-162">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="cc151-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="cc151-163">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cc151-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cc151-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc151-164">RELATED LINKS</span></span>

[<span data-ttu-id="cc151-165">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc151-165">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="cc151-166">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cc151-166">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="cc151-167">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cc151-167">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
