---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522474"
---
# <span data-ttu-id="3d88a-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d88a-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="3d88a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d88a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d88a-103">Skapar en tabell resurs för virtuell hubb som är underordnad VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="3d88a-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="3d88a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d88a-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d88a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d88a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d88a-106">Den virtuella nav-routningstabellen innehåller listan över vägar och en lista med anslutningar som den kan kopplas till och som används för att dirigera trafik i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="3d88a-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="3d88a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d88a-107">EXAMPLES</span></span>

### <span data-ttu-id="3d88a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d88a-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="3d88a-109">Med kommandot ovan skapas en tabell resurs för virtuell hubb från vägarna som skickas till den och det här objektet kan användas för att dirigera trafik i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="3d88a-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="3d88a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d88a-110">PARAMETERS</span></span>

### <span data-ttu-id="3d88a-111">-Anslutning</span><span class="sxs-lookup"><span data-stu-id="3d88a-111">-Connection</span></span>
<span data-ttu-id="3d88a-112">Lista över anslutningar som den här väg tabellen är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="3d88a-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="3d88a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d88a-113">-DefaultProfile</span></span>
<span data-ttu-id="3d88a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d88a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d88a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d88a-115">-Name</span></span>
<span data-ttu-id="3d88a-116">Namn på routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="3d88a-116">Name of the route table.</span></span>

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

### <span data-ttu-id="3d88a-117">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="3d88a-117">-Route</span></span>
<span data-ttu-id="3d88a-118">Lista över virtuella nav-vägar.</span><span class="sxs-lookup"><span data-stu-id="3d88a-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d88a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d88a-119">CommonParameters</span></span>
<span data-ttu-id="3d88a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d88a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d88a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d88a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d88a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d88a-122">INPUTS</span></span>

### <span data-ttu-id="3d88a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d88a-123">None</span></span>

## <span data-ttu-id="3d88a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d88a-124">OUTPUTS</span></span>

### <span data-ttu-id="3d88a-125">Microsoft. Azure. commands. Networks. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d88a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="3d88a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d88a-126">NOTES</span></span>

## <span data-ttu-id="3d88a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d88a-127">RELATED LINKS</span></span>
