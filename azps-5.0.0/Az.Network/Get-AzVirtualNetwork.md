---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271356"
---
# <span data-ttu-id="df85a-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df85a-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="df85a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df85a-102">SYNOPSIS</span></span>
<span data-ttu-id="df85a-103">Hämtar ett virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="df85a-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="df85a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df85a-104">SYNTAX</span></span>

### <span data-ttu-id="df85a-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="df85a-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df85a-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="df85a-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df85a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df85a-107">DESCRIPTION</span></span>
<span data-ttu-id="df85a-108">Cmdleten **Get-AzVirtualNetwork** får ett eller flera virtuella nätverk n en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="df85a-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="df85a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df85a-109">EXAMPLES</span></span>

### <span data-ttu-id="df85a-110">1: Hämta ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="df85a-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="df85a-111">Det här kommandot får det virtuella nätverk som heter MyVirtualNetwork i resurs gruppen TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df85a-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="df85a-112">2: lista virtuella nätverk med filter</span><span class="sxs-lookup"><span data-stu-id="df85a-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="df85a-113">Det här kommandot får alla virtuella nätverk som börjar med "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="df85a-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="df85a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df85a-114">PARAMETERS</span></span>

### <span data-ttu-id="df85a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df85a-115">-DefaultProfile</span></span>
<span data-ttu-id="df85a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df85a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df85a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="df85a-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df85a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="df85a-118">-Name</span></span>
<span data-ttu-id="df85a-119">Anger namnet på det virtuella nätverk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="df85a-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="df85a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df85a-120">-ResourceGroupName</span></span>
<span data-ttu-id="df85a-121">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="df85a-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="df85a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df85a-122">CommonParameters</span></span>
<span data-ttu-id="df85a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df85a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df85a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df85a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df85a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df85a-125">INPUTS</span></span>

### <span data-ttu-id="df85a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="df85a-126">System.String</span></span>

## <span data-ttu-id="df85a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df85a-127">OUTPUTS</span></span>

### <span data-ttu-id="df85a-128">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df85a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df85a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df85a-129">NOTES</span></span>

## <span data-ttu-id="df85a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df85a-130">RELATED LINKS</span></span>

[<span data-ttu-id="df85a-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df85a-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="df85a-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df85a-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="df85a-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df85a-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


