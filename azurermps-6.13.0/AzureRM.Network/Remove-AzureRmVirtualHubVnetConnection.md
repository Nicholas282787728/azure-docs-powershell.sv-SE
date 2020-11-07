---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755337"
---
# <span data-ttu-id="fb0d6-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="fb0d6-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="fb0d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0d6-103">Remove-AzureRmVirtualHubVnetConnection cmdlet tar bort en Azure Virtual Network-anslutning som peererar ett fjärrnätverk till hubbens VNET.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb0d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb0d6-104">SYNTAX</span></span>

### <span data-ttu-id="fb0d6-105">ByHubVirtualNetworkConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="fb0d6-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb0d6-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fb0d6-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb0d6-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0d6-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb0d6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb0d6-108">DESCRIPTION</span></span>
<span data-ttu-id="fb0d6-109">Remove-AzureRmVirtualHubVnetConnection cmdlet tar bort en Azure Virtual Network-anslutning som peererar ett fjärrnätverk till hubbens VNET.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="fb0d6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb0d6-110">EXAMPLES</span></span>

### <span data-ttu-id="fb0d6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb0d6-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="fb0d6-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="fb0d6-113">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="fb0d6-114">När anslutningen till navets virtuella nätverk skapas tar det bort den virtuella nav nätverks anslutningen med dess resurs grupp namn, hubbens namn och anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="fb0d6-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fb0d6-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="fb0d6-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="fb0d6-117">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="fb0d6-118">När du har skapat navets virtuella nätverks anslutning tar det bort den virtuella nav nätverks anslutningen med PowerShell-inmatningen från get-AzureRmHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="fb0d6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb0d6-119">PARAMETERS</span></span>

### <span data-ttu-id="fb0d6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb0d6-120">-AsJob</span></span>
<span data-ttu-id="fb0d6-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fb0d6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb0d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0d6-122">-DefaultProfile</span></span>
<span data-ttu-id="fb0d6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb0d6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fb0d6-124">-Force</span></span>
<span data-ttu-id="fb0d6-125">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="fb0d6-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fb0d6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb0d6-126">-InputObject</span></span>
<span data-ttu-id="fb0d6-127">Hubvirtualnetworkconnection-resursen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="fb0d6-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb0d6-128">-Name</span></span>
<span data-ttu-id="fb0d6-129">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-129">The resource name.</span></span>

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

### <span data-ttu-id="fb0d6-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fb0d6-130">-ParentResourceName</span></span>
<span data-ttu-id="fb0d6-131">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-131">The parent resource name.</span></span>

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

### <span data-ttu-id="fb0d6-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb0d6-132">-PassThru</span></span>
<span data-ttu-id="fb0d6-133">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb0d6-134">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb0d6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0d6-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb0d6-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-136">The resource group name.</span></span>

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

### <span data-ttu-id="fb0d6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb0d6-137">-ResourceId</span></span>
<span data-ttu-id="fb0d6-138">Resurs-ID för den hubvirtualnetworkconnection-resurs som du vill ändra.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="fb0d6-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb0d6-139">-Confirm</span></span>
<span data-ttu-id="fb0d6-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb0d6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb0d6-141">-WhatIf</span></span>
<span data-ttu-id="fb0d6-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb0d6-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb0d6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0d6-144">CommonParameters</span></span>
<span data-ttu-id="fb0d6-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0d6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0d6-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb0d6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0d6-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb0d6-147">INPUTS</span></span>

### <span data-ttu-id="fb0d6-148">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="fb0d6-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="fb0d6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fb0d6-149">System.String</span></span>

## <span data-ttu-id="fb0d6-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb0d6-150">OUTPUTS</span></span>

### <span data-ttu-id="fb0d6-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb0d6-151">System.Boolean</span></span>

## <span data-ttu-id="fb0d6-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb0d6-152">NOTES</span></span>

## <span data-ttu-id="fb0d6-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb0d6-153">RELATED LINKS</span></span>
