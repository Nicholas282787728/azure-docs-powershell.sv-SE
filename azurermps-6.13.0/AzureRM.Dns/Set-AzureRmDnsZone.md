---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 67997145a327d7f9e47f4cf346cbfd5e3a6bf0f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756173"
---
# <span data-ttu-id="2100a-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="2100a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2100a-102">SYNOPSIS</span></span>
<span data-ttu-id="2100a-103">Uppdaterar egenskaperna för en DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="2100a-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2100a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2100a-104">SYNTAX</span></span>

### <span data-ttu-id="2100a-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="2100a-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2100a-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="2100a-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2100a-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="2100a-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2100a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2100a-108">DESCRIPTION</span></span>
<span data-ttu-id="2100a-109">Cmdleten **set-AzureRmDnsZone** uppdaterar den angivna DNS-zonen i Azure DNS-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2100a-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="2100a-110">Denna cmdlet uppdaterar inte post uppsättningarna i zonen.</span><span class="sxs-lookup"><span data-stu-id="2100a-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="2100a-111">Du kan skicka ett **dnsZone** -objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2100a-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2100a-112">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2100a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2100a-113">När du skickar en DNS-zon som ett objekt (med målobjektet eller pipeline) uppdateras den inte om den har ändrats i Azure DNS sedan det lokala DnsZone-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="2100a-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2100a-114">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="2100a-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2100a-115">Du kan förhindra detta med den *överskrivnings* parameter som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="2100a-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2100a-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2100a-116">EXAMPLES</span></span>

### <span data-ttu-id="2100a-117">Exempel 1: uppdatera en DNS-zon</span><span class="sxs-lookup"><span data-stu-id="2100a-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="2100a-118">Det första kommandot får zonen som heter myzone.com från angiven resurs grupp och lagrar den sedan i $Zone variabel.</span><span class="sxs-lookup"><span data-stu-id="2100a-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="2100a-119">Det andra kommandot uppdaterar taggarna för $Zone.</span><span class="sxs-lookup"><span data-stu-id="2100a-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="2100a-120">Det slutliga kommandot utför ändringen.</span><span class="sxs-lookup"><span data-stu-id="2100a-120">The final command commits the change.</span></span>

### <span data-ttu-id="2100a-121">Exempel 2: uppdatera taggar för en zon</span><span class="sxs-lookup"><span data-stu-id="2100a-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="2100a-122">Det här kommandot uppdaterar taggarna för zonen med namnet myzone.com utan att först explicit komma åt zonen.</span><span class="sxs-lookup"><span data-stu-id="2100a-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="2100a-123">Exempel 3: associera en privat zon med ett virtuellt nätverk genom att ange dess ID</span><span class="sxs-lookup"><span data-stu-id="2100a-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="2100a-124">Det här kommandot associerar den privata DNS-zonen myprivatezone.com med det virtuella nätverks myvnet som ett registrerings nätverk genom att ange dess ID.</span><span class="sxs-lookup"><span data-stu-id="2100a-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="2100a-125">Exempel 4: associera en privat zon med ett virtuellt nätverk genom att ange nätverks objekt.</span><span class="sxs-lookup"><span data-stu-id="2100a-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="2100a-126">Det här kommandot associerar den privata DNS-zonen myprivatezone.com med det virtuella nätverks myvnet som ett registrerings nätverk genom att överföra det virtuella nätverks objekt som representeras av $vnet variabel till Set-AzureRmDnsZone cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2100a-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="2100a-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2100a-127">PARAMETERS</span></span>

### <span data-ttu-id="2100a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2100a-128">-DefaultProfile</span></span>
<span data-ttu-id="2100a-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2100a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2100a-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="2100a-130">-Name</span></span>
<span data-ttu-id="2100a-131">Anger namnet på den DNS-zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2100a-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-132">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="2100a-132">-Overwrite</span></span>
<span data-ttu-id="2100a-133">När du skickar en DNS-zon som ett objekt (med målobjektet eller pipeline) uppdateras den inte om den har ändrats i Azure DNS sedan det lokala DnsZone-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="2100a-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2100a-134">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="2100a-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2100a-135">Du kan förhindra detta med den *överskrivnings* parameter som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="2100a-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2100a-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="2100a-137">Listan med virtuella nätverk som ska registrera poster för virtuella dator namn i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="2100a-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2100a-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="2100a-139">Listan över virtuella nätverks-ID: n som registrerar virtuella dator namn poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="2100a-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2100a-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="2100a-141">Listan med virtuella nätverk som kan lösa poster i den här DNS-zonen, är endast tillgänglig för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="2100a-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2100a-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="2100a-143">Listan över virtuella nätverks-ID: n som kan användas för att lösa poster i denna DNS-zon är bara tillgängliga för privata zoner.</span><span class="sxs-lookup"><span data-stu-id="2100a-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2100a-144">-ResourceGroupName</span></span>
<span data-ttu-id="2100a-145">Anger namnet på den resurs grupp som innehåller den zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2100a-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="2100a-146">Du måste också ange parametern zonnamn.</span><span class="sxs-lookup"><span data-stu-id="2100a-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="2100a-147">Alternativt kan du ange zonen med hjälp av ett DnsZone-objekt med parametern *Zone* eller pipeline.</span><span class="sxs-lookup"><span data-stu-id="2100a-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2100a-148">-Tag</span></span>
<span data-ttu-id="2100a-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2100a-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2100a-150">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="2100a-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="2100a-151">-Zone</span></span>
<span data-ttu-id="2100a-152">Anger den DNS-zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="2100a-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="2100a-153">Alternativt kan du ange zonen med parametrarna *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2100a-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2100a-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2100a-154">-Confirm</span></span>
<span data-ttu-id="2100a-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2100a-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2100a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2100a-156">-WhatIf</span></span>
<span data-ttu-id="2100a-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2100a-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2100a-158">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2100a-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2100a-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2100a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2100a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2100a-160">CommonParameters</span></span>
<span data-ttu-id="2100a-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2100a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2100a-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2100a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2100a-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2100a-163">INPUTS</span></span>

### <span data-ttu-id="2100a-164">System. String</span><span class="sxs-lookup"><span data-stu-id="2100a-164">System.String</span></span>

### <span data-ttu-id="2100a-165">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="2100a-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2100a-166">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2100a-166">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2100a-167">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. commands. Common. Network, version = 1.0.0.0; Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2100a-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2100a-168">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2100a-169">Parametrar: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2100a-169">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="2100a-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2100a-170">OUTPUTS</span></span>

### <span data-ttu-id="2100a-171">Microsoft. Azure. commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-171">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="2100a-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2100a-172">NOTES</span></span>
<span data-ttu-id="2100a-173">Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2100a-173">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2100a-174">Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.</span><span class="sxs-lookup"><span data-stu-id="2100a-174">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="2100a-175">Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.</span><span class="sxs-lookup"><span data-stu-id="2100a-175">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2100a-176">Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2100a-176">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2100a-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2100a-177">RELATED LINKS</span></span>

[<span data-ttu-id="2100a-178">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-178">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2100a-179">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-179">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="2100a-180">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2100a-180">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)