---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922199"
---
# <span data-ttu-id="c2512-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c2512-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="c2512-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2512-102">SYNOPSIS</span></span>
<span data-ttu-id="c2512-103">Hämtar virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="c2512-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="c2512-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2512-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2512-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2512-105">DESCRIPTION</span></span>
<span data-ttu-id="c2512-106">Cmdleten **Get-AzVirtualNetworkPeering** hämtar det virtuella nätverkets peering.</span><span class="sxs-lookup"><span data-stu-id="c2512-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="c2512-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2512-107">EXAMPLES</span></span>

### <span data-ttu-id="c2512-108">Exempel 1: skapa en peering mellan två virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="c2512-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="c2512-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2512-109">PARAMETERS</span></span>

### <span data-ttu-id="c2512-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2512-110">-DefaultProfile</span></span>
<span data-ttu-id="c2512-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2512-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2512-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2512-112">-Name</span></span>
<span data-ttu-id="c2512-113">Anger det virtuella nätverkets peering-namn.</span><span class="sxs-lookup"><span data-stu-id="c2512-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2512-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2512-114">-ResourceGroupName</span></span>
<span data-ttu-id="c2512-115">Anger namnet på den resurs grupp som det virtuella nätverks peer-datorn tillhör.</span><span class="sxs-lookup"><span data-stu-id="c2512-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="c2512-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c2512-116">-VirtualNetworkName</span></span>
<span data-ttu-id="c2512-117">Anger det virtuella nätverks namnet som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c2512-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2512-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2512-118">CommonParameters</span></span>
<span data-ttu-id="c2512-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2512-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2512-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2512-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2512-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2512-121">INPUTS</span></span>

## <span data-ttu-id="c2512-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2512-122">OUTPUTS</span></span>

### <span data-ttu-id="c2512-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c2512-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="c2512-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2512-124">NOTES</span></span>

## <span data-ttu-id="c2512-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2512-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2512-126">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c2512-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c2512-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c2512-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="c2512-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c2512-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


