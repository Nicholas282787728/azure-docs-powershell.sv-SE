---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584071"
---
# <span data-ttu-id="459be-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="459be-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="459be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="459be-102">SYNOPSIS</span></span>
<span data-ttu-id="459be-103">Remove-AzureRmVpnGateway cmdlet tar bort en Azure VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="459be-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="459be-104">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="459be-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="459be-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="459be-105">SYNTAX</span></span>

### <span data-ttu-id="459be-106">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="459be-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459be-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="459be-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459be-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="459be-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="459be-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="459be-109">DESCRIPTION</span></span>
<span data-ttu-id="459be-110">Remove-AzureRmVpnGateway cmdlet tar bort en Azure VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="459be-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="459be-111">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="459be-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="459be-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="459be-112">EXAMPLES</span></span>

### <span data-ttu-id="459be-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="459be-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="459be-114">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, utbyggbar VPN gateway i Central USA och sedan omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="459be-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="459be-115">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="459be-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="459be-116">Detta tar bort VpnGateway och alla VpnConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="459be-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="459be-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="459be-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="459be-118">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, utbyggbar VPN gateway i Central USA och sedan omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="459be-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="459be-119">Denna borttagning sker med PowerShell-rör som använder VpnGateway-objektet som returneras av kommandot Get-AzureRmVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="459be-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="459be-120">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="459be-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="459be-121">Detta tar bort VpnGateway och alla VpnConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="459be-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="459be-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="459be-122">PARAMETERS</span></span>

### <span data-ttu-id="459be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459be-123">-DefaultProfile</span></span>
<span data-ttu-id="459be-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="459be-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="459be-125">-Force</span><span class="sxs-lookup"><span data-stu-id="459be-125">-Force</span></span>
<span data-ttu-id="459be-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="459be-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="459be-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="459be-127">-InputObject</span></span>
<span data-ttu-id="459be-128">VpnGateway-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="459be-128">The vpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="459be-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="459be-129">-Name</span></span>
<span data-ttu-id="459be-130">VpnGateway namn.</span><span class="sxs-lookup"><span data-stu-id="459be-130">The vpnGateway name.</span></span>

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

### <span data-ttu-id="459be-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="459be-131">-PassThru</span></span>
<span data-ttu-id="459be-132">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="459be-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="459be-133">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="459be-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="459be-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459be-134">-ResourceGroupName</span></span>
<span data-ttu-id="459be-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="459be-135">The resource group name.</span></span>

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

### <span data-ttu-id="459be-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="459be-136">-ResourceId</span></span>
<span data-ttu-id="459be-137">Azure Resource ID för vpnGateway ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="459be-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="459be-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="459be-138">-Confirm</span></span>
<span data-ttu-id="459be-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="459be-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="459be-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459be-140">-WhatIf</span></span>
<span data-ttu-id="459be-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="459be-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459be-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="459be-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="459be-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459be-143">CommonParameters</span></span>
<span data-ttu-id="459be-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="459be-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459be-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="459be-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459be-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="459be-146">INPUTS</span></span>

### <span data-ttu-id="459be-147">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="459be-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="459be-148">System. String</span><span class="sxs-lookup"><span data-stu-id="459be-148">System.String</span></span>

## <span data-ttu-id="459be-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="459be-149">OUTPUTS</span></span>

### <span data-ttu-id="459be-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="459be-150">System.Boolean</span></span>

## <span data-ttu-id="459be-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="459be-151">NOTES</span></span>

## <span data-ttu-id="459be-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="459be-152">RELATED LINKS</span></span>
