---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259324"
---
# <span data-ttu-id="b40d0-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b40d0-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="b40d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b40d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b40d0-103">Hämtar virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="b40d0-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="b40d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b40d0-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b40d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b40d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b40d0-106">Cmdleten **Get-AzVirtualNetworkPeering** hämtar det virtuella nätverkets peering.</span><span class="sxs-lookup"><span data-stu-id="b40d0-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="b40d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b40d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b40d0-108">Exempel 1: skapa en peering mellan två virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="b40d0-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="b40d0-109">Exempel 2: Hämta alla peers i virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="b40d0-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="b40d0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b40d0-110">PARAMETERS</span></span>

### <span data-ttu-id="b40d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40d0-111">-DefaultProfile</span></span>
<span data-ttu-id="b40d0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b40d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b40d0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b40d0-113">-Name</span></span>
<span data-ttu-id="b40d0-114">Anger det virtuella nätverkets peering-namn.</span><span class="sxs-lookup"><span data-stu-id="b40d0-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b40d0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40d0-115">-ResourceGroupName</span></span>
<span data-ttu-id="b40d0-116">Anger namnet på den resurs grupp som det virtuella nätverks peer-datorn tillhör.</span><span class="sxs-lookup"><span data-stu-id="b40d0-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="b40d0-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b40d0-117">-VirtualNetworkName</span></span>
<span data-ttu-id="b40d0-118">Anger det virtuella nätverks namnet som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b40d0-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b40d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40d0-119">CommonParameters</span></span>
<span data-ttu-id="b40d0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40d0-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b40d0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40d0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b40d0-122">INPUTS</span></span>

### <span data-ttu-id="b40d0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b40d0-123">System.String</span></span>

## <span data-ttu-id="b40d0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b40d0-124">OUTPUTS</span></span>

### <span data-ttu-id="b40d0-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b40d0-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b40d0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b40d0-126">NOTES</span></span>

## <span data-ttu-id="b40d0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b40d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="b40d0-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b40d0-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b40d0-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b40d0-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b40d0-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b40d0-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
