---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526204"
---
# <span data-ttu-id="a855c-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a855c-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="a855c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a855c-102">SYNOPSIS</span></span>
<span data-ttu-id="a855c-103">Hämtar en tabell resurs för en hubb som är associerad med en VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a855c-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="a855c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a855c-104">SYNTAX</span></span>

### <span data-ttu-id="a855c-105">ByVHubRouteTableName (standard)</span><span class="sxs-lookup"><span data-stu-id="a855c-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a855c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a855c-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a855c-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="a855c-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a855c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a855c-108">DESCRIPTION</span></span>
<span data-ttu-id="a855c-109">Hämtar den angivna nav tabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="a855c-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="a855c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a855c-110">EXAMPLES</span></span>

### <span data-ttu-id="a855c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a855c-111">Example 1</span></span>

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

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="a855c-112">Det här kommandot hämtar nav vägs tabellen för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="a855c-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="a855c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a855c-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="a855c-114">Det här kommandot visar alla nav flödes tabeller i angiven VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a855c-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="a855c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a855c-115">PARAMETERS</span></span>

### <span data-ttu-id="a855c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a855c-116">-AsJob</span></span>
<span data-ttu-id="a855c-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a855c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a855c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a855c-118">-DefaultProfile</span></span>
<span data-ttu-id="a855c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a855c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a855c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a855c-120">-Name</span></span>
<span data-ttu-id="a855c-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a855c-121">The resource name.</span></span>

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

### <span data-ttu-id="a855c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a855c-122">-ParentObject</span></span>
<span data-ttu-id="a855c-123">Överordnat objekt för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="a855c-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="a855c-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a855c-124">-ParentResourceName</span></span>
<span data-ttu-id="a855c-125">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="a855c-125">The parent resource name.</span></span>

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

### <span data-ttu-id="a855c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a855c-126">-ResourceGroupName</span></span>
<span data-ttu-id="a855c-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a855c-127">The resource group name.</span></span>

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

### <span data-ttu-id="a855c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a855c-128">-ResourceId</span></span>
<span data-ttu-id="a855c-129">Resurs-ID för den vhubroutetable-resurs som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a855c-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="a855c-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a855c-130">-Confirm</span></span>
<span data-ttu-id="a855c-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a855c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a855c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a855c-132">-WhatIf</span></span>
<span data-ttu-id="a855c-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a855c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a855c-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a855c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a855c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a855c-135">CommonParameters</span></span>
<span data-ttu-id="a855c-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a855c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a855c-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a855c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a855c-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a855c-138">INPUTS</span></span>

### <span data-ttu-id="a855c-139">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a855c-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a855c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a855c-140">System.String</span></span>

## <span data-ttu-id="a855c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a855c-141">OUTPUTS</span></span>

### <span data-ttu-id="a855c-142">Microsoft. Azure. commands. Networks. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a855c-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="a855c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a855c-143">NOTES</span></span>

## <span data-ttu-id="a855c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a855c-144">RELATED LINKS</span></span>

[<span data-ttu-id="a855c-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="a855c-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="a855c-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a855c-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="a855c-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a855c-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="a855c-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a855c-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)