---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261771"
---
# <span data-ttu-id="ea54f-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="ea54f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea54f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea54f-103">Ta bort en tabell resurs för en hubb som är associerad med en VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ea54f-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="ea54f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea54f-104">SYNTAX</span></span>

### <span data-ttu-id="ea54f-105">ByVHubRouteTableName (standard)</span><span class="sxs-lookup"><span data-stu-id="ea54f-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea54f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ea54f-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea54f-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="ea54f-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea54f-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="ea54f-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea54f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea54f-109">DESCRIPTION</span></span>
<span data-ttu-id="ea54f-110">Uppdaterar den angivna routningstabellen som är kopplad till det virtuella navet med de angivna vägarna eller etiketterna.</span><span class="sxs-lookup"><span data-stu-id="ea54f-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="ea54f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea54f-111">EXAMPLES</span></span>

### <span data-ttu-id="ea54f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea54f-112">Example 1</span></span>
```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="ea54f-113">Det här kommandot tar bort nav-routningstabellen för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="ea54f-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="ea54f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea54f-114">PARAMETERS</span></span>

### <span data-ttu-id="ea54f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea54f-115">-AsJob</span></span>
<span data-ttu-id="ea54f-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ea54f-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea54f-117">-DefaultProfile</span></span>
<span data-ttu-id="ea54f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea54f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea54f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea54f-119">-InputObject</span></span>
<span data-ttu-id="ea54f-120">Vhubroutetable-resursen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ea54f-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-121">-Etikett</span><span class="sxs-lookup"><span data-stu-id="ea54f-121">-Label</span></span>
<span data-ttu-id="ea54f-122">Listan med etiketter.</span><span class="sxs-lookup"><span data-stu-id="ea54f-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea54f-123">-Name</span></span>
<span data-ttu-id="ea54f-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ea54f-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ea54f-125">-ParentObject</span></span>
<span data-ttu-id="ea54f-126">Överordnat objekt för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="ea54f-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ea54f-127">-ParentResourceName</span></span>
<span data-ttu-id="ea54f-128">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="ea54f-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea54f-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea54f-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ea54f-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea54f-131">-ResourceId</span></span>
<span data-ttu-id="ea54f-132">Resurs-ID för den vhubroutetable-resurs som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="ea54f-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-133">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="ea54f-133">-Route</span></span>
<span data-ttu-id="ea54f-134">Listan över vägar för den här routningstabellen.</span><span class="sxs-lookup"><span data-stu-id="ea54f-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea54f-135">-Confirm</span></span>
<span data-ttu-id="ea54f-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea54f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea54f-137">-WhatIf</span></span>
<span data-ttu-id="ea54f-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea54f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea54f-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea54f-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea54f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea54f-140">CommonParameters</span></span>
<span data-ttu-id="ea54f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea54f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea54f-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea54f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea54f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea54f-143">INPUTS</span></span>

### <span data-ttu-id="ea54f-144">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea54f-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ea54f-145">Microsoft. Azure. commands. Networks. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="ea54f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ea54f-146">System.String</span></span>

## <span data-ttu-id="ea54f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea54f-147">OUTPUTS</span></span>

### <span data-ttu-id="ea54f-148">Microsoft. Azure. commands. Networks. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="ea54f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea54f-149">NOTES</span></span>

## <span data-ttu-id="ea54f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea54f-150">RELATED LINKS</span></span>

[<span data-ttu-id="ea54f-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="ea54f-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="ea54f-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="ea54f-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="ea54f-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea54f-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)