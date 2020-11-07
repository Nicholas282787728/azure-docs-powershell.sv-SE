---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 16a17ed437194963f3cfd715a6e5364c8f4348c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747839"
---
# <span data-ttu-id="1a492-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1a492-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="1a492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a492-102">SYNOPSIS</span></span>
<span data-ttu-id="1a492-103">Remove-AzVirtualHubVnetConnection cmdlet tar bort en Azure Virtual Network-anslutning som peererar ett fjärrnätverk till hubbens VNET.</span><span class="sxs-lookup"><span data-stu-id="1a492-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="1a492-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a492-104">SYNTAX</span></span>

### <span data-ttu-id="1a492-105">ByHubVirtualNetworkConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="1a492-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a492-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="1a492-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a492-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="1a492-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a492-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a492-108">DESCRIPTION</span></span>
<span data-ttu-id="1a492-109">Remove-AzVirtualHubVnetConnection cmdlet tar bort en Azure Virtual Network-anslutning som peererar ett fjärrnätverk till hubbens VNET.</span><span class="sxs-lookup"><span data-stu-id="1a492-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="1a492-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a492-110">EXAMPLES</span></span>

### <span data-ttu-id="1a492-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a492-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="1a492-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="1a492-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="1a492-113">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="1a492-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="1a492-114">När anslutningen till navets virtuella nätverk skapas tar det bort den virtuella nav nätverks anslutningen med dess resurs grupp namn, hubbens namn och anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="1a492-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="1a492-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1a492-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="1a492-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="1a492-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="1a492-117">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="1a492-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="1a492-118">När du har skapat navets virtuella nätverks anslutning tar det bort den virtuella nav nätverks anslutningen med PowerShell-inmatningen från get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="1a492-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="1a492-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a492-119">PARAMETERS</span></span>

### <span data-ttu-id="1a492-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a492-120">-AsJob</span></span>
<span data-ttu-id="1a492-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1a492-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a492-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a492-122">-DefaultProfile</span></span>
<span data-ttu-id="1a492-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a492-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a492-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1a492-124">-Force</span></span>
<span data-ttu-id="1a492-125">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="1a492-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1a492-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a492-126">-InputObject</span></span>
<span data-ttu-id="1a492-127">Hubvirtualnetworkconnection-resursen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="1a492-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a492-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a492-128">-Name</span></span>
<span data-ttu-id="1a492-129">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1a492-129">The resource name.</span></span>

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

### <span data-ttu-id="1a492-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1a492-130">-ParentResourceName</span></span>
<span data-ttu-id="1a492-131">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="1a492-131">The parent resource name.</span></span>

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

### <span data-ttu-id="1a492-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a492-132">-PassThru</span></span>
<span data-ttu-id="1a492-133">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1a492-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a492-134">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1a492-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1a492-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a492-135">-ResourceGroupName</span></span>
<span data-ttu-id="1a492-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1a492-136">The resource group name.</span></span>

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

### <span data-ttu-id="1a492-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a492-137">-ResourceId</span></span>
<span data-ttu-id="1a492-138">Resurs-ID för den hubvirtualnetworkconnection-resurs som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="1a492-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="1a492-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a492-139">-Confirm</span></span>
<span data-ttu-id="1a492-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a492-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a492-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a492-141">-WhatIf</span></span>
<span data-ttu-id="1a492-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a492-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a492-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a492-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a492-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a492-144">CommonParameters</span></span>
<span data-ttu-id="1a492-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a492-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a492-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a492-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a492-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a492-147">INPUTS</span></span>

### <span data-ttu-id="1a492-148">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="1a492-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="1a492-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1a492-149">System.String</span></span>

## <span data-ttu-id="1a492-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a492-150">OUTPUTS</span></span>

### <span data-ttu-id="1a492-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a492-151">System.Boolean</span></span>

## <span data-ttu-id="1a492-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a492-152">NOTES</span></span>

## <span data-ttu-id="1a492-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a492-153">RELATED LINKS</span></span>

[<span data-ttu-id="1a492-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1a492-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="1a492-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1a492-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)