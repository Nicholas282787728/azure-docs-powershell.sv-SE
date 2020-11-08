---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090267"
---
# <span data-ttu-id="46d61-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="46d61-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="46d61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46d61-102">SYNOPSIS</span></span>
<span data-ttu-id="46d61-103">Skapar ett VirtualHubRoute-objekt som kan skickas som parameter till kommandot Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="46d61-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="46d61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46d61-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46d61-105">DESCRIPTION</span></span>
<span data-ttu-id="46d61-106">Skapar ett VirtualHubRoute-objekt.</span><span class="sxs-lookup"><span data-stu-id="46d61-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="46d61-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46d61-107">EXAMPLES</span></span>

### <span data-ttu-id="46d61-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46d61-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="46d61-109">Med kommandot ovan skapas ett VirtualHubRoute-objekt som sedan kan läggas till i en VirtualHubRouteTable-resurs och ställas in på en VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="46d61-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="46d61-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46d61-110">PARAMETERS</span></span>

### <span data-ttu-id="46d61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d61-111">-DefaultProfile</span></span>
<span data-ttu-id="46d61-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46d61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d61-113">-Mål</span><span class="sxs-lookup"><span data-stu-id="46d61-113">-Destination</span></span>
<span data-ttu-id="46d61-114">Lista med destinationer.</span><span class="sxs-lookup"><span data-stu-id="46d61-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d61-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="46d61-115">-DestinationType</span></span>
<span data-ttu-id="46d61-116">Typ av destinationer.</span><span class="sxs-lookup"><span data-stu-id="46d61-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d61-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="46d61-117">-NextHop</span></span>
<span data-ttu-id="46d61-118">Lista över nästa hopp.</span><span class="sxs-lookup"><span data-stu-id="46d61-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d61-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="46d61-119">-NextHopType</span></span>
<span data-ttu-id="46d61-120">Nästa hopp typ.</span><span class="sxs-lookup"><span data-stu-id="46d61-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d61-121">CommonParameters</span></span>
<span data-ttu-id="46d61-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d61-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d61-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d61-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46d61-124">INPUTS</span></span>

### <span data-ttu-id="46d61-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="46d61-125">None</span></span>

## <span data-ttu-id="46d61-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46d61-126">OUTPUTS</span></span>

### <span data-ttu-id="46d61-127">Microsoft. Azure. commands. Networks. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="46d61-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="46d61-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46d61-128">NOTES</span></span>

## <span data-ttu-id="46d61-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46d61-129">RELATED LINKS</span></span>