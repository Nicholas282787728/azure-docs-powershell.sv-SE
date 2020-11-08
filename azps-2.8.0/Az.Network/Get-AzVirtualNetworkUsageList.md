---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918409"
---
# <span data-ttu-id="e2e82-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="e2e82-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="e2e82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2e82-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e82-103">Hämtar aktuell användning av virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="e2e82-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="e2e82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2e82-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2e82-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e82-106">Cmdleten **Get-AzVirtualNetworkUsageList** hämtar per Subnet-användning för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="e2e82-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="e2e82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2e82-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e82-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e2e82-108">Example 1</span></span>
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

<span data-ttu-id="e2e82-109">Hämtar aktuella värden per undernät för det usagetest virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="e2e82-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="e2e82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2e82-110">PARAMETERS</span></span>

### <span data-ttu-id="e2e82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e82-111">-DefaultProfile</span></span>
<span data-ttu-id="e2e82-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e82-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2e82-113">-Name</span></span>
<span data-ttu-id="e2e82-114">Anger namnet på det virtuella nätverk som ska Visa användningar för.</span><span class="sxs-lookup"><span data-stu-id="e2e82-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="e2e82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e82-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2e82-116">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="e2e82-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="e2e82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e82-117">CommonParameters</span></span>
<span data-ttu-id="e2e82-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e82-119">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2e82-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e82-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2e82-120">INPUTS</span></span>

### <span data-ttu-id="e2e82-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e82-121">System.String</span></span>

## <span data-ttu-id="e2e82-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2e82-122">OUTPUTS</span></span>

### <span data-ttu-id="e2e82-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="e2e82-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="e2e82-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2e82-124">NOTES</span></span>

## <span data-ttu-id="e2e82-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2e82-125">RELATED LINKS</span></span>