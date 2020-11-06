---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 855385b55922f6255b407ceafef7422113968516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576233"
---
# <span data-ttu-id="68fe9-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="68fe9-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="68fe9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="68fe9-103">Hämtar aktuell användning av virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="68fe9-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fe9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68fe9-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68fe9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="68fe9-106">Cmdleten **Get-AzureRmVirtualNetworkUsageList** hämtar per Subnet-användning för det angivna virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="68fe9-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="68fe9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68fe9-107">EXAMPLES</span></span>

### <span data-ttu-id="68fe9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="68fe9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="68fe9-109">Hämtar aktuella värden per undernät för det usagetest virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="68fe9-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="68fe9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68fe9-110">PARAMETERS</span></span>

### <span data-ttu-id="68fe9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fe9-111">-DefaultProfile</span></span>
<span data-ttu-id="68fe9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68fe9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fe9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="68fe9-113">-Name</span></span>
<span data-ttu-id="68fe9-114">Anger namnet på det virtuella nätverk som ska Visa användningar för.</span><span class="sxs-lookup"><span data-stu-id="68fe9-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="68fe9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fe9-115">-ResourceGroupName</span></span>
<span data-ttu-id="68fe9-116">Anger namnet på den resurs grupp som det virtuella nätverket tillhör.</span><span class="sxs-lookup"><span data-stu-id="68fe9-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="68fe9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fe9-117">CommonParameters</span></span>
<span data-ttu-id="68fe9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fe9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fe9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fe9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fe9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68fe9-120">INPUTS</span></span>

### <span data-ttu-id="68fe9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="68fe9-121">System.String</span></span>

## <span data-ttu-id="68fe9-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68fe9-122">OUTPUTS</span></span>

### <span data-ttu-id="68fe9-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="68fe9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="68fe9-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68fe9-124">NOTES</span></span>

## <span data-ttu-id="68fe9-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68fe9-125">RELATED LINKS</span></span>
