---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526199"
---
# <span data-ttu-id="25a81-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="25a81-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="25a81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25a81-102">SYNOPSIS</span></span>
<span data-ttu-id="25a81-103">Hämtar en virtuell hubb för väg tabell i ett virtuellt nav eller visar alla väg tabeller i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="25a81-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="25a81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25a81-104">SYNTAX</span></span>

### <span data-ttu-id="25a81-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="25a81-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a81-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="25a81-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a81-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="25a81-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a81-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25a81-108">DESCRIPTION</span></span>
<span data-ttu-id="25a81-109">Hämtar en virtuell hubb för väg tabell i ett virtuellt nav eller visar alla väg tabeller i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="25a81-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="25a81-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25a81-110">EXAMPLES</span></span>

### <span data-ttu-id="25a81-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25a81-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="25a81-112">Denna cmdlet hämtar en väg tabell resurs med resurs grupp namn, nav namn och väg tabell namn.</span><span class="sxs-lookup"><span data-stu-id="25a81-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="25a81-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="25a81-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="25a81-114">Denna cmdlet visar alla väg tabeller som finns i en virtuell hubb med resurs grupp namn och hubbens namn.</span><span class="sxs-lookup"><span data-stu-id="25a81-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="25a81-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25a81-115">PARAMETERS</span></span>

### <span data-ttu-id="25a81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a81-116">-DefaultProfile</span></span>
<span data-ttu-id="25a81-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25a81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a81-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="25a81-118">-HubName</span></span>
<span data-ttu-id="25a81-119">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="25a81-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a81-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="25a81-120">-Name</span></span>
<span data-ttu-id="25a81-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25a81-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a81-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="25a81-122">-ParentResourceId</span></span>
<span data-ttu-id="25a81-123">Överordnat resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="25a81-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a81-124">-ResourceGroupName</span></span>
<span data-ttu-id="25a81-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="25a81-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a81-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="25a81-126">-VirtualHub</span></span>
<span data-ttu-id="25a81-127">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="25a81-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a81-128">CommonParameters</span></span>
<span data-ttu-id="25a81-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a81-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25a81-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a81-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25a81-131">INPUTS</span></span>

### <span data-ttu-id="25a81-132">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="25a81-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="25a81-133">System. String</span><span class="sxs-lookup"><span data-stu-id="25a81-133">System.String</span></span>

## <span data-ttu-id="25a81-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25a81-134">OUTPUTS</span></span>

### <span data-ttu-id="25a81-135">Microsoft. Azure. commands. Networks. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="25a81-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="25a81-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25a81-136">NOTES</span></span>

## <span data-ttu-id="25a81-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25a81-137">RELATED LINKS</span></span>
