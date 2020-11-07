---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 87591f5ecf928fb2dc9444fd826ce03f484e665c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747813"
---
# <span data-ttu-id="44942-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44942-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="44942-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44942-102">SYNOPSIS</span></span>
<span data-ttu-id="44942-103">Tar bort en VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="44942-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="44942-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44942-104">SYNTAX</span></span>

### <span data-ttu-id="44942-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="44942-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44942-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="44942-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44942-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="44942-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44942-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44942-108">DESCRIPTION</span></span>
<span data-ttu-id="44942-109">Tar bort en VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="44942-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="44942-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44942-110">EXAMPLES</span></span>

### <span data-ttu-id="44942-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="44942-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="44942-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="44942-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="44942-113">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="44942-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="44942-114">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="44942-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="44942-115">Därefter tas anslutningen bort med anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="44942-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="44942-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="44942-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="44942-117">Samma som exempel 1 men tar nu bort anslutningen med piped-objektet från get-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="44942-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="44942-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44942-118">PARAMETERS</span></span>

### <span data-ttu-id="44942-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44942-119">-DefaultProfile</span></span>
<span data-ttu-id="44942-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44942-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44942-121">-Force</span><span class="sxs-lookup"><span data-stu-id="44942-121">-Force</span></span>
<span data-ttu-id="44942-122">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="44942-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="44942-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44942-123">-InputObject</span></span>
<span data-ttu-id="44942-124">VpnConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="44942-124">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44942-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="44942-125">-Name</span></span>
<span data-ttu-id="44942-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="44942-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44942-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="44942-127">-ParentResourceName</span></span>
<span data-ttu-id="44942-128">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="44942-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44942-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44942-129">-PassThru</span></span>
<span data-ttu-id="44942-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="44942-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="44942-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="44942-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44942-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44942-132">-ResourceGroupName</span></span>
<span data-ttu-id="44942-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="44942-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44942-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44942-134">-ResourceId</span></span>
<span data-ttu-id="44942-135">Resurs-ID för det VpnConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="44942-135">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44942-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44942-136">-Confirm</span></span>
<span data-ttu-id="44942-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44942-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44942-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44942-138">-WhatIf</span></span>
<span data-ttu-id="44942-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44942-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44942-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44942-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44942-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44942-141">CommonParameters</span></span>
<span data-ttu-id="44942-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44942-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44942-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44942-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44942-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44942-144">INPUTS</span></span>

### <span data-ttu-id="44942-145">System. String</span><span class="sxs-lookup"><span data-stu-id="44942-145">System.String</span></span>

### <span data-ttu-id="44942-146">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44942-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="44942-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44942-147">OUTPUTS</span></span>

### <span data-ttu-id="44942-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44942-148">System.Boolean</span></span>

## <span data-ttu-id="44942-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44942-149">NOTES</span></span>

## <span data-ttu-id="44942-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44942-150">RELATED LINKS</span></span>

[<span data-ttu-id="44942-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44942-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="44942-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44942-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="44942-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44942-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
