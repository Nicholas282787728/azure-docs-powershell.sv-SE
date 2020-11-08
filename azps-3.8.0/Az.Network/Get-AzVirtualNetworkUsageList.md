---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089092"
---
# <span data-ttu-id="d190d-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="d190d-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="d190d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d190d-102">SYNOPSIS</span></span>
<span data-ttu-id="d190d-103">Hämtar aktuell användning av virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="d190d-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="d190d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d190d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d190d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d190d-105">DESCRIPTION</span></span>
<span data-ttu-id="d190d-106">Cmdleten **Get-AzVirtualNetworkUsageList** hämtar per Subnet-användning för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="d190d-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="d190d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d190d-107">EXAMPLES</span></span>

### <span data-ttu-id="d190d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d190d-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="d190d-109">Hämtar aktuella värden per undernät för det usagetest virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="d190d-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="d190d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d190d-110">PARAMETERS</span></span>

### <span data-ttu-id="d190d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d190d-111">-DefaultProfile</span></span>
<span data-ttu-id="d190d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d190d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d190d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d190d-113">-Name</span></span>
<span data-ttu-id="d190d-114">Anger namnet på det virtuella nätverk som ska Visa användningar för.</span><span class="sxs-lookup"><span data-stu-id="d190d-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="d190d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d190d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d190d-116">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="d190d-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="d190d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d190d-117">CommonParameters</span></span>
<span data-ttu-id="d190d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d190d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d190d-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d190d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d190d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d190d-120">INPUTS</span></span>

### <span data-ttu-id="d190d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d190d-121">System.String</span></span>

## <span data-ttu-id="d190d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d190d-122">OUTPUTS</span></span>

### <span data-ttu-id="d190d-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="d190d-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="d190d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d190d-124">NOTES</span></span>

## <span data-ttu-id="d190d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d190d-125">RELATED LINKS</span></span>
