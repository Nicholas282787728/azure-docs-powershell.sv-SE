---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758169"
---
# <span data-ttu-id="e6c23-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e6c23-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="e6c23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6c23-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c23-103">Hämtar ett Azure-VirtualHub efter namn och ResourceGroupName eller visar alla virtuella nav efter ResourceGroupName/prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e6c23-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6c23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6c23-104">SYNTAX</span></span>

### <span data-ttu-id="e6c23-105">ListBySubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="e6c23-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6c23-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c23-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c23-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6c23-107">DESCRIPTION</span></span>
<span data-ttu-id="e6c23-108">Hämtar ett Azure-VirtualHub efter namn och ResourceGroupName eller visar alla virtuella nav efter ResourceGroupName/prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e6c23-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="e6c23-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6c23-109">EXAMPLES</span></span>

### <span data-ttu-id="e6c23-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6c23-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="e6c23-111">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c23-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e6c23-112">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="e6c23-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e6c23-113">Den får sedan det virtuella navet med dess ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e6c23-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="e6c23-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6c23-114">PARAMETERS</span></span>

### <span data-ttu-id="e6c23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c23-115">-DefaultProfile</span></span>
<span data-ttu-id="e6c23-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c23-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6c23-117">-Name</span></span>
<span data-ttu-id="e6c23-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e6c23-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c23-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c23-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6c23-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e6c23-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c23-121">CommonParameters</span></span>
<span data-ttu-id="e6c23-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c23-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c23-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6c23-124">INPUTS</span></span>

### <span data-ttu-id="e6c23-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="e6c23-125">None</span></span>

## <span data-ttu-id="e6c23-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6c23-126">OUTPUTS</span></span>

### <span data-ttu-id="e6c23-127">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e6c23-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e6c23-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6c23-128">NOTES</span></span>

## <span data-ttu-id="e6c23-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6c23-129">RELATED LINKS</span></span>
