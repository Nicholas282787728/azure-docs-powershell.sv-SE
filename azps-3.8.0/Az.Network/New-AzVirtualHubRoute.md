---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090966"
---
# <span data-ttu-id="40fcf-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="40fcf-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="40fcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="40fcf-103">Skapar ett Azure-objekt för virtuell hubb.</span><span class="sxs-lookup"><span data-stu-id="40fcf-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="40fcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40fcf-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fcf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="40fcf-106">Skapar ett Azure-objekt för virtuell hubb.</span><span class="sxs-lookup"><span data-stu-id="40fcf-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="40fcf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="40fcf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40fcf-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="40fcf-109">Ovanstående skapar ett virtuellt nav-objekt som kan inkluderas i den virtuella nav-routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="40fcf-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="40fcf-110">Vägen för virtuella NAV är ett objekt i minnet som kan användas för att skapa ett VirtualHubRouteTable-objekt.</span><span class="sxs-lookup"><span data-stu-id="40fcf-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="40fcf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40fcf-111">PARAMETERS</span></span>

### <span data-ttu-id="40fcf-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40fcf-112">-AddressPrefix</span></span>
<span data-ttu-id="40fcf-113">Lista med adressprefix.</span><span class="sxs-lookup"><span data-stu-id="40fcf-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fcf-114">-DefaultProfile</span></span>
<span data-ttu-id="40fcf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40fcf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40fcf-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="40fcf-116">-NextHopIpAddress</span></span>
<span data-ttu-id="40fcf-117">Nästa hopp-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="40fcf-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="40fcf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fcf-118">CommonParameters</span></span>
<span data-ttu-id="40fcf-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fcf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fcf-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fcf-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fcf-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40fcf-121">INPUTS</span></span>

### <span data-ttu-id="40fcf-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="40fcf-122">None</span></span>

## <span data-ttu-id="40fcf-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40fcf-123">OUTPUTS</span></span>

### <span data-ttu-id="40fcf-124">Microsoft. Azure. commands. Networks. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="40fcf-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="40fcf-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40fcf-125">NOTES</span></span>

## <span data-ttu-id="40fcf-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40fcf-126">RELATED LINKS</span></span>

[<span data-ttu-id="40fcf-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="40fcf-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
