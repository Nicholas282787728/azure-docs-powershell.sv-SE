---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928037"
---
# <span data-ttu-id="666f1-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="666f1-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="666f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="666f1-102">SYNOPSIS</span></span>
<span data-ttu-id="666f1-103">Uppdaterar en befintlig HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="666f1-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="666f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="666f1-104">SYNTAX</span></span>

### <span data-ttu-id="666f1-105">ByHubVirtualNetworkConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="666f1-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="666f1-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="666f1-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="666f1-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="666f1-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="666f1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="666f1-108">DESCRIPTION</span></span>
<span data-ttu-id="666f1-109">Uppdaterar en befintlig HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="666f1-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="666f1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="666f1-110">EXAMPLES</span></span>

### <span data-ttu-id="666f1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="666f1-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="666f1-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="666f1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="666f1-113">En virtuell nätverks anslutning skapas också som är peer det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="666f1-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="666f1-114">Den här virtuella nätverks anslutningen uppdateras sedan för att aktivera Internet säkerhet.</span><span class="sxs-lookup"><span data-stu-id="666f1-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="666f1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="666f1-115">PARAMETERS</span></span>

### <span data-ttu-id="666f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="666f1-116">-AsJob</span></span>
<span data-ttu-id="666f1-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="666f1-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666f1-118">-DefaultProfile</span></span>
<span data-ttu-id="666f1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="666f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="666f1-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="666f1-121">Aktivera Internet säkerhet för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="666f1-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="666f1-122">-InputObject</span></span>
<span data-ttu-id="666f1-123">Hubvirtualnetworkconnection-resursen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="666f1-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="666f1-124">-Name</span></span>
<span data-ttu-id="666f1-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="666f1-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="666f1-126">-ParentResourceName</span></span>
<span data-ttu-id="666f1-127">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="666f1-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="666f1-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="666f1-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="666f1-130">-ResourceId</span></span>
<span data-ttu-id="666f1-131">Resurs-ID för den hubvirtualnetworkconnection-resurs som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="666f1-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="666f1-132">-Confirm</span></span>
<span data-ttu-id="666f1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="666f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666f1-134">-WhatIf</span></span>
<span data-ttu-id="666f1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="666f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="666f1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="666f1-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666f1-137">CommonParameters</span></span>
<span data-ttu-id="666f1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666f1-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="666f1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666f1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="666f1-140">INPUTS</span></span>

### <span data-ttu-id="666f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="666f1-141">System.String</span></span>

### <span data-ttu-id="666f1-142">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="666f1-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="666f1-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="666f1-143">OUTPUTS</span></span>

### <span data-ttu-id="666f1-144">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="666f1-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="666f1-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="666f1-145">NOTES</span></span>

## <span data-ttu-id="666f1-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="666f1-146">RELATED LINKS</span></span>