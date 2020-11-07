---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3aea2414a4b7fdfbc14e65d4d087bb7e31206aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919834"
---
# <span data-ttu-id="f8f6e-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f8f6e-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f8f6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f6e-103">Hämtar en virtuell nätverks länk som är kopplad till den angivna privata DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="f8f6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8f6e-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f6e-106">Cmdleten **Get-AzPrivateDnsVirtualNetworkLink** hämtar virtuella nätverks länkar som är kopplade till en viss privat DNS-zon från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="f8f6e-107">Om du anger parametern *Name* returneras ett enskilt **PSPrivateDnsVirtualNetworkLink** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="f8f6e-108">Om du inte anger parametern *Name* returneras en matris med alla länkar som är kopplade till zonen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="f8f6e-109">Du kan använda **PSPrivateDnsVirtualNetworkLink** -objektet för att uppdatera länken.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="f8f6e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8f6e-110">EXAMPLES</span></span>

### <span data-ttu-id="f8f6e-111">Exempel 1: Hämta ett virtuellt nätverks länk.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="f8f6e-112">Det här exemplet hämtar länken för den virtuella nätverks länken som är kopplad till den privata DNS-zonen med namnet myzone.com från den angivna resurs gruppen och lagrar den sedan i $Link variabel.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="f8f6e-113">Exempel 2: Hämta alla länkar som är kopplade till en zon i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="f8f6e-114">Det här exemplet får alla virtuella nätverks länkar som är kopplade till den privata DNS-zonen "myzone.com" i den angivna resurs gruppen och lagrar sedan den i $Links variabel.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="f8f6e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8f6e-115">PARAMETERS</span></span>

### <span data-ttu-id="f8f6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f6e-116">-DefaultProfile</span></span>
<span data-ttu-id="f8f6e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f8f6e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8f6e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8f6e-118">-Name</span></span>
<span data-ttu-id="f8f6e-119">Anger namnet på den virtuella nätverks länk som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="f8f6e-120">Om du inte anger ett värde för parametern *Name* får denna cmdlet alla länkar som är kopplade till den angivna privata DNS-zonen i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8f6e-122">Anger namnet på den resurs grupp som innehåller den virtuella nätverks länken som ska visas.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="f8f6e-123">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="f8f6e-123">-ZoneName</span></span>
<span data-ttu-id="f8f6e-124">Anger namnet på den privata DNS-zon som den virtuella nätverks länken är länkad till.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="f8f6e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f6e-125">CommonParameters</span></span>
<span data-ttu-id="f8f6e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f6e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f6e-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f6e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f6e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8f6e-128">INPUTS</span></span>

### <span data-ttu-id="f8f6e-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8f6e-129">None</span></span>

## <span data-ttu-id="f8f6e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8f6e-130">OUTPUTS</span></span>

### <span data-ttu-id="f8f6e-131">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f8f6e-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f8f6e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8f6e-132">NOTES</span></span>

## <span data-ttu-id="f8f6e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8f6e-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8f6e-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f8f6e-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f8f6e-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f8f6e-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f8f6e-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f8f6e-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
