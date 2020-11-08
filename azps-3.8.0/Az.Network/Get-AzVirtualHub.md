---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091010"
---
# <span data-ttu-id="90e99-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90e99-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="90e99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90e99-102">SYNOPSIS</span></span>
<span data-ttu-id="90e99-103">Hämtar ett Azure-VirtualHub efter namn och ResourceGroupName eller visar alla virtuella nav efter ResourceGroupName/prenumeration.</span><span class="sxs-lookup"><span data-stu-id="90e99-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="90e99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90e99-104">SYNTAX</span></span>

### <span data-ttu-id="90e99-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="90e99-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90e99-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e99-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90e99-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90e99-107">DESCRIPTION</span></span>
<span data-ttu-id="90e99-108">Hämtar ett Azure-VirtualHub efter namn och ResourceGroupName eller visar alla virtuella nav efter ResourceGroupName/prenumeration.</span><span class="sxs-lookup"><span data-stu-id="90e99-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="90e99-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90e99-109">EXAMPLES</span></span>

### <span data-ttu-id="90e99-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90e99-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="90e99-111">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="90e99-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="90e99-112">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="90e99-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="90e99-113">Den får sedan det virtuella navet med dess ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="90e99-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="90e99-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="90e99-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="90e99-115">Denna cmdlet får det virtuella navet med filtrering.</span><span class="sxs-lookup"><span data-stu-id="90e99-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="90e99-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90e99-116">PARAMETERS</span></span>

### <span data-ttu-id="90e99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e99-117">-DefaultProfile</span></span>
<span data-ttu-id="90e99-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90e99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e99-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="90e99-119">-Name</span></span>
<span data-ttu-id="90e99-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="90e99-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="90e99-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e99-121">-ResourceGroupName</span></span>
<span data-ttu-id="90e99-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="90e99-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="90e99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e99-123">CommonParameters</span></span>
<span data-ttu-id="90e99-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e99-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90e99-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e99-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90e99-126">INPUTS</span></span>

### <span data-ttu-id="90e99-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="90e99-127">None</span></span>

## <span data-ttu-id="90e99-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90e99-128">OUTPUTS</span></span>

### <span data-ttu-id="90e99-129">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90e99-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="90e99-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90e99-130">NOTES</span></span>

## <span data-ttu-id="90e99-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90e99-131">RELATED LINKS</span></span>

[<span data-ttu-id="90e99-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90e99-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="90e99-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90e99-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="90e99-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="90e99-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)