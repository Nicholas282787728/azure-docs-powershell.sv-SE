---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 4b58561783fac3d0c068ec61821c9669a97e1542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580064"
---
# <span data-ttu-id="03806-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="03806-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="03806-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03806-102">SYNOPSIS</span></span>
<span data-ttu-id="03806-103">Hämtar virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="03806-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03806-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03806-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03806-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03806-105">DESCRIPTION</span></span>
<span data-ttu-id="03806-106">Cmdleten **Get-AzureRmVirtualNetworkPeering** hämtar det virtuella nätverkets peering.</span><span class="sxs-lookup"><span data-stu-id="03806-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="03806-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03806-107">EXAMPLES</span></span>

### <span data-ttu-id="03806-108">Exempel 1: skapa en peering mellan två virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="03806-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="03806-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03806-109">PARAMETERS</span></span>

### <span data-ttu-id="03806-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03806-110">-DefaultProfile</span></span>
<span data-ttu-id="03806-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03806-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03806-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="03806-112">-Name</span></span>
<span data-ttu-id="03806-113">Anger det virtuella nätverkets peering-namn.</span><span class="sxs-lookup"><span data-stu-id="03806-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03806-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03806-114">-ResourceGroupName</span></span>
<span data-ttu-id="03806-115">Anger namnet på den resurs grupp som det virtuella nätverks peer-datorn tillhör.</span><span class="sxs-lookup"><span data-stu-id="03806-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="03806-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="03806-116">-VirtualNetworkName</span></span>
<span data-ttu-id="03806-117">Anger det virtuella nätverks namnet som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="03806-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03806-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03806-118">CommonParameters</span></span>
<span data-ttu-id="03806-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03806-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03806-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03806-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03806-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03806-121">INPUTS</span></span>

### <span data-ttu-id="03806-122">System. String</span><span class="sxs-lookup"><span data-stu-id="03806-122">System.String</span></span>

## <span data-ttu-id="03806-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03806-123">OUTPUTS</span></span>

### <span data-ttu-id="03806-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="03806-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="03806-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03806-125">NOTES</span></span>

## <span data-ttu-id="03806-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03806-126">RELATED LINKS</span></span>

[<span data-ttu-id="03806-127">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="03806-127">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="03806-128">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="03806-128">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="03806-129">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="03806-129">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


