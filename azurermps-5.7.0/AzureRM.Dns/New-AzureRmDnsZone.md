---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755877"
---
# <span data-ttu-id="3944f-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3944f-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="3944f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3944f-102">SYNOPSIS</span></span>
<span data-ttu-id="3944f-103">Skapar en ny DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="3944f-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3944f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3944f-104">SYNTAX</span></span>

### <span data-ttu-id="3944f-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="3944f-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3944f-106">Objekten</span><span class="sxs-lookup"><span data-stu-id="3944f-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3944f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3944f-107">DESCRIPTION</span></span>
<span data-ttu-id="3944f-108">Cmdleten **New-AzureRmDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3944f-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="3944f-109">Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="3944f-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="3944f-110">När zonen har skapats kan du använda New-AzureRmDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="3944f-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="3944f-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3944f-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3944f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3944f-112">EXAMPLES</span></span>

### <span data-ttu-id="3944f-113">Exempel 1: skapa en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="3944f-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3944f-114">Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="3944f-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3944f-115">Exempel 2: skapa en privat DNS-zon genom att ange virtuella nätverks-ID</span><span class="sxs-lookup"><span data-stu-id="3944f-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="3944f-116">Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (som anger dess ID) och lagrar det sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="3944f-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3944f-117">Exempel 3: skapa en privat DNS-zon genom att ange virtuella nätverks objekt</span><span class="sxs-lookup"><span data-stu-id="3944f-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="3944f-118">Det här kommandot skapar en ny privat DNS-zon som heter myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (kallas $ResVirtualNetwork variabel) och lagrar sedan in det i $Zone-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3944f-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="3944f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3944f-119">PARAMETERS</span></span>

### <span data-ttu-id="3944f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3944f-120">-DefaultProfile</span></span>
<span data-ttu-id="3944f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3944f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3944f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3944f-122">-Name</span></span>
<span data-ttu-id="3944f-123">Anger namnet på DNS-zonen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3944f-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="3944f-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3944f-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="3944f-125">Listan med virtuella nätverk som ska registrera poster för virtuella dator namn i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="3944f-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3944f-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3944f-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="3944f-127">Listan över virtuella nätverks-ID: n som registrerar virtuella dator namn poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="3944f-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3944f-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3944f-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="3944f-129">Listan med virtuella nätverk som kan lösa poster i den här DNS-zonen, är endast tillgänglig för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="3944f-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3944f-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3944f-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="3944f-131">Listan över virtuella nätverks-ID: n som kan användas för att lösa poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="3944f-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3944f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3944f-132">-ResourceGroupName</span></span>
<span data-ttu-id="3944f-133">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="3944f-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="3944f-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3944f-134">-Tag</span></span>
<span data-ttu-id="3944f-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3944f-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3944f-136">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3944f-136">For example:</span></span>

<span data-ttu-id="3944f-137">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3944f-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3944f-138">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="3944f-138">-ZoneType</span></span>
<span data-ttu-id="3944f-139">Typen av zon, offentlig eller privat.</span><span class="sxs-lookup"><span data-stu-id="3944f-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="3944f-140">Zoner utan typ eller med en typ av offentliga tjänster görs tillgängliga för det offentliga DNS-tjänsten för användning i DNS-hierarkin.</span><span class="sxs-lookup"><span data-stu-id="3944f-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="3944f-141">Zoner med en typ av privat är bara synliga från med uppsättningen associerade virtuella nätverk (den här funktionen är i för hands version).</span><span class="sxs-lookup"><span data-stu-id="3944f-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="3944f-142">Det går inte att ändra den här egenskapen för en zon.</span><span class="sxs-lookup"><span data-stu-id="3944f-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3944f-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3944f-143">-Confirm</span></span>
<span data-ttu-id="3944f-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3944f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3944f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3944f-145">-WhatIf</span></span>
<span data-ttu-id="3944f-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3944f-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3944f-147">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3944f-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3944f-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3944f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3944f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3944f-149">CommonParameters</span></span>
<span data-ttu-id="3944f-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3944f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3944f-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3944f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3944f-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3944f-152">INPUTS</span></span>

### <span data-ttu-id="3944f-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="3944f-153">None</span></span>
<span data-ttu-id="3944f-154">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3944f-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="3944f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3944f-155">OUTPUTS</span></span>

### <span data-ttu-id="3944f-156">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="3944f-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="3944f-157">Denna cmdlet returnerar ett Microsoft. Azure. commands. DNS. DnsZone-objekt som representerar den nya DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="3944f-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="3944f-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3944f-158">NOTES</span></span>
<span data-ttu-id="3944f-159">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3944f-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3944f-160">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="3944f-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="3944f-161">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="3944f-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3944f-162">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3944f-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3944f-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3944f-163">RELATED LINKS</span></span>

[<span data-ttu-id="3944f-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3944f-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="3944f-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3944f-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="3944f-166">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3944f-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
