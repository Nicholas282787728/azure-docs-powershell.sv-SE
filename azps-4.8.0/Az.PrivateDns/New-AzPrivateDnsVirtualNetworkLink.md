---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261992"
---
# <span data-ttu-id="e0e27-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e0e27-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e0e27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0e27-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e27-103">Skapar en ny länk till ett privat virtuellt DNS-nätverk.</span><span class="sxs-lookup"><span data-stu-id="e0e27-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="e0e27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0e27-104">SYNTAX</span></span>

### <span data-ttu-id="e0e27-105">VirtualNetworkId (standard)</span><span class="sxs-lookup"><span data-stu-id="e0e27-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e27-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e0e27-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e27-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0e27-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e27-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0e27-108">DESCRIPTION</span></span>
<span data-ttu-id="e0e27-109">Cmdleten **New-AzPrivateDnsVirtualNetworkLink** skapar en ny virtuell DNS-länk (Domain Name System) i den angivna resurs gruppen och den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="e0e27-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="e0e27-110">Du måste ange ett unikt länknamn för parametern *namn* , eller så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="e0e27-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="e0e27-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e0e27-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e0e27-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0e27-112">EXAMPLES</span></span>

### <span data-ttu-id="e0e27-113">Exempel 1: skapa ett privat virtuellt DNS-nätverk.</span><span class="sxs-lookup"><span data-stu-id="e0e27-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="e0e27-114">Det här kommandot skapar en ny virtuell nätverks länk som är kopplad till den privata DNS-zon som heter myzone.com och Virtual Network "myvirtualnetwork" (som redan har skapats i resurs gruppen) i den angivna resurs gruppen och sedan lagrar den i $Link variabel.</span><span class="sxs-lookup"><span data-stu-id="e0e27-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="e0e27-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0e27-115">PARAMETERS</span></span>

### <span data-ttu-id="e0e27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e27-116">-DefaultProfile</span></span>
<span data-ttu-id="e0e27-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0e27-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0e27-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="e0e27-118">-EnableRegistration</span></span>
<span data-ttu-id="e0e27-119">Byt parameter som representerar om länken är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="e0e27-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="e0e27-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0e27-120">-Name</span></span>
<span data-ttu-id="e0e27-121">Anger namnet på den virtuella nätverks länk som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e0e27-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="e0e27-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0e27-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="e0e27-123">Resurs-ID för det virtuella nätverket i en annan klient organisation.</span><span class="sxs-lookup"><span data-stu-id="e0e27-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e27-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0e27-125">Anger den resurs grupp som länken ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="e0e27-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="e0e27-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e0e27-126">-Tag</span></span>
<span data-ttu-id="e0e27-127">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="e0e27-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e0e27-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e0e27-128">-VirtualNetwork</span></span>
<span data-ttu-id="e0e27-129">Det virtuella nätverks objekt som är kopplat till länken.</span><span class="sxs-lookup"><span data-stu-id="e0e27-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="e0e27-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0e27-130">-VirtualNetworkId</span></span>
<span data-ttu-id="e0e27-131">Resurs-ID för det virtuella nätverk som är kopplat till länken.</span><span class="sxs-lookup"><span data-stu-id="e0e27-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="e0e27-132">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="e0e27-132">-ZoneName</span></span>
<span data-ttu-id="e0e27-133">Anger namnet på den zon som ska länkas till länken virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="e0e27-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="e0e27-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0e27-134">-Confirm</span></span>
<span data-ttu-id="e0e27-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0e27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e27-136">-WhatIf</span></span>
<span data-ttu-id="e0e27-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0e27-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0e27-138">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0e27-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0e27-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0e27-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e27-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e27-140">CommonParameters</span></span>
<span data-ttu-id="e0e27-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e27-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e27-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0e27-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e27-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0e27-143">INPUTS</span></span>

### <span data-ttu-id="e0e27-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0e27-144">None</span></span>

## <span data-ttu-id="e0e27-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0e27-145">OUTPUTS</span></span>

### <span data-ttu-id="e0e27-146">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e0e27-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e0e27-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0e27-147">NOTES</span></span>

## <span data-ttu-id="e0e27-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0e27-148">RELATED LINKS</span></span>

[<span data-ttu-id="e0e27-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e0e27-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e0e27-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e0e27-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e0e27-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e0e27-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
