---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747811"
---
# <span data-ttu-id="ed3b5-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed3b5-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="ed3b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3b5-103">Remove-AzVpnGateway cmdlet tar bort en Azure VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="ed3b5-104">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="ed3b5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed3b5-105">SYNTAX</span></span>

### <span data-ttu-id="ed3b5-106">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="ed3b5-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3b5-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ed3b5-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3b5-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ed3b5-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed3b5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed3b5-109">DESCRIPTION</span></span>
<span data-ttu-id="ed3b5-110">Remove-AzVpnGateway cmdlet tar bort en Azure VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="ed3b5-111">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="ed3b5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed3b5-112">EXAMPLES</span></span>

### <span data-ttu-id="ed3b5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed3b5-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="ed3b5-114">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, utbyggbar VPN gateway i Central USA och sedan omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="ed3b5-115">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="ed3b5-116">Detta tar bort VpnGateway och alla VpnConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="ed3b5-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ed3b5-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="ed3b5-118">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, utbyggbar VPN gateway i Central USA och sedan omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="ed3b5-119">Denna borttagning sker med PowerShell-rör som använder VpnGateway-objektet som returneras av kommandot Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="ed3b5-120">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="ed3b5-121">Detta tar bort VpnGateway och alla VpnConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="ed3b5-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed3b5-122">PARAMETERS</span></span>

### <span data-ttu-id="ed3b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3b5-123">-DefaultProfile</span></span>
<span data-ttu-id="ed3b5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3b5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ed3b5-125">-Force</span></span>
<span data-ttu-id="ed3b5-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ed3b5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3b5-127">-InputObject</span></span>
<span data-ttu-id="ed3b5-128">VpnGateway-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3b5-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed3b5-129">-Name</span></span>
<span data-ttu-id="ed3b5-130">VpnGateway namn.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3b5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed3b5-131">-PassThru</span></span>
<span data-ttu-id="ed3b5-132">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed3b5-133">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed3b5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3b5-134">-ResourceGroupName</span></span>
<span data-ttu-id="ed3b5-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3b5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed3b5-136">-ResourceId</span></span>
<span data-ttu-id="ed3b5-137">Azure Resource ID för vpnGateway ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3b5-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed3b5-138">-Confirm</span></span>
<span data-ttu-id="ed3b5-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed3b5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed3b5-140">-WhatIf</span></span>
<span data-ttu-id="ed3b5-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed3b5-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed3b5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3b5-143">CommonParameters</span></span>
<span data-ttu-id="ed3b5-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3b5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3b5-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3b5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3b5-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed3b5-146">INPUTS</span></span>

### <span data-ttu-id="ed3b5-147">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed3b5-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ed3b5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ed3b5-148">System.String</span></span>

## <span data-ttu-id="ed3b5-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed3b5-149">OUTPUTS</span></span>

### <span data-ttu-id="ed3b5-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed3b5-150">System.Boolean</span></span>

## <span data-ttu-id="ed3b5-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed3b5-151">NOTES</span></span>

## <span data-ttu-id="ed3b5-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed3b5-152">RELATED LINKS</span></span>

[<span data-ttu-id="ed3b5-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed3b5-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="ed3b5-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed3b5-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="ed3b5-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ed3b5-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)