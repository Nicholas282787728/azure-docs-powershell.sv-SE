---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576158"
---
# <span data-ttu-id="42a43-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="42a43-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="42a43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42a43-102">SYNOPSIS</span></span>
<span data-ttu-id="42a43-103">Tar bort en VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="42a43-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42a43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42a43-104">SYNTAX</span></span>

### <span data-ttu-id="42a43-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="42a43-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a43-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="42a43-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a43-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="42a43-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a43-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42a43-108">DESCRIPTION</span></span>
<span data-ttu-id="42a43-109">Tar bort en VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="42a43-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="42a43-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42a43-110">EXAMPLES</span></span>

### <span data-ttu-id="42a43-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42a43-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="42a43-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="42a43-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="42a43-113">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="42a43-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="42a43-114">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="42a43-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="42a43-115">Därefter tas anslutningen bort med anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="42a43-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="42a43-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="42a43-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="42a43-117">Samma som exempel 1 men tar nu bort anslutningen med piped-objektet från get-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="42a43-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="42a43-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42a43-118">PARAMETERS</span></span>

### <span data-ttu-id="42a43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a43-119">-DefaultProfile</span></span>
<span data-ttu-id="42a43-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42a43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a43-121">-Force</span><span class="sxs-lookup"><span data-stu-id="42a43-121">-Force</span></span>
<span data-ttu-id="42a43-122">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="42a43-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="42a43-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42a43-123">-InputObject</span></span>
<span data-ttu-id="42a43-124">VpnConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="42a43-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="42a43-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="42a43-125">-Name</span></span>
<span data-ttu-id="42a43-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="42a43-126">The resource name.</span></span>

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

### <span data-ttu-id="42a43-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="42a43-127">-ParentResourceName</span></span>
<span data-ttu-id="42a43-128">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="42a43-128">The parent resource name.</span></span>

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

### <span data-ttu-id="42a43-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42a43-129">-PassThru</span></span>
<span data-ttu-id="42a43-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="42a43-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42a43-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="42a43-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42a43-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a43-132">-ResourceGroupName</span></span>
<span data-ttu-id="42a43-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="42a43-133">The resource group name.</span></span>

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

### <span data-ttu-id="42a43-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a43-134">-ResourceId</span></span>
<span data-ttu-id="42a43-135">Resurs-ID för det VpnConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="42a43-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="42a43-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42a43-136">-Confirm</span></span>
<span data-ttu-id="42a43-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42a43-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a43-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a43-138">-WhatIf</span></span>
<span data-ttu-id="42a43-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42a43-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a43-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42a43-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a43-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a43-141">CommonParameters</span></span>
<span data-ttu-id="42a43-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a43-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a43-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a43-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a43-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42a43-144">INPUTS</span></span>

### <span data-ttu-id="42a43-145">System. String</span><span class="sxs-lookup"><span data-stu-id="42a43-145">System.String</span></span>

### <span data-ttu-id="42a43-146">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="42a43-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="42a43-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42a43-147">OUTPUTS</span></span>

### <span data-ttu-id="42a43-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42a43-148">System.Boolean</span></span>

## <span data-ttu-id="42a43-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42a43-149">NOTES</span></span>

## <span data-ttu-id="42a43-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42a43-150">RELATED LINKS</span></span>
