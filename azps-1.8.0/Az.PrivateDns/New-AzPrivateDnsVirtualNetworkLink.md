---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 7d2a9a399e6582e2ff3815447570548ac62f6676
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747507"
---
# <span data-ttu-id="e1136-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e1136-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e1136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1136-102">SYNOPSIS</span></span>
<span data-ttu-id="e1136-103">Skapar en ny länk till ett privat virtuellt DNS-nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1136-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="e1136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1136-104">SYNTAX</span></span>

### <span data-ttu-id="e1136-105">VirtualNetworkId (standard)</span><span class="sxs-lookup"><span data-stu-id="e1136-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1136-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e1136-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1136-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1136-107">DESCRIPTION</span></span>
<span data-ttu-id="e1136-108">Cmdleten **New-AzPrivateDnsVirtualNetworkLink** skapar en ny virtuell DNS-länk (Domain Name System) i den angivna resurs gruppen och den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="e1136-108">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="e1136-109">Du måste ange ett unikt länknamn för parametern *namn* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="e1136-109">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="e1136-110">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e1136-110">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e1136-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1136-111">EXAMPLES</span></span>

### <span data-ttu-id="e1136-112">Exempel 1: skapa ett privat virtuellt DNS-nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1136-112">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="e1136-113">Det här kommandot skapar en ny virtuell nätverks länk som är kopplad till den privata DNS-zon som heter myzone.com och Virtual Network "myvirtualnetwork" (som redan har skapats i resurs gruppen) i den angivna resurs gruppen och sedan lagrar den i $Link variabel.</span><span class="sxs-lookup"><span data-stu-id="e1136-113">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="e1136-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1136-114">PARAMETERS</span></span>

### <span data-ttu-id="e1136-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1136-115">-DefaultProfile</span></span>
<span data-ttu-id="e1136-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e1136-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1136-117">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="e1136-117">-EnableRegistration</span></span>
<span data-ttu-id="e1136-118">Byt parameter som representerar om länken är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="e1136-118">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="e1136-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1136-119">-Name</span></span>
<span data-ttu-id="e1136-120">Anger namnet på den virtuella nätverks länk som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e1136-120">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1136-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1136-122">Anger den resurs grupp som länken ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="e1136-122">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e1136-123">-Tag</span></span>
<span data-ttu-id="e1136-124">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="e1136-124">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1136-125">-VirtualNetwork</span></span>
<span data-ttu-id="e1136-126">Det virtuella nätverks objekt som är kopplat till länken.</span><span class="sxs-lookup"><span data-stu-id="e1136-126">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-127">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e1136-127">-VirtualNetworkId</span></span>
<span data-ttu-id="e1136-128">Resurs-ID för det virtuella nätverk som är kopplat till länken.</span><span class="sxs-lookup"><span data-stu-id="e1136-128">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-129">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="e1136-129">-ZoneName</span></span>
<span data-ttu-id="e1136-130">Anger namnet på den zon som ska länkas till länken virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e1136-130">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1136-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1136-131">-Confirm</span></span>
<span data-ttu-id="e1136-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1136-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1136-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1136-133">-WhatIf</span></span>
<span data-ttu-id="e1136-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1136-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1136-135">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1136-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1136-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1136-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1136-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1136-137">CommonParameters</span></span>
<span data-ttu-id="e1136-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1136-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1136-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1136-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1136-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1136-140">INPUTS</span></span>

### <span data-ttu-id="e1136-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="e1136-141">None</span></span>

## <span data-ttu-id="e1136-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1136-142">OUTPUTS</span></span>

### <span data-ttu-id="e1136-143">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e1136-143">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e1136-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1136-144">NOTES</span></span>

## <span data-ttu-id="e1136-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1136-145">RELATED LINKS</span></span>

[<span data-ttu-id="e1136-146">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e1136-146">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e1136-147">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e1136-147">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e1136-148">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e1136-148">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
