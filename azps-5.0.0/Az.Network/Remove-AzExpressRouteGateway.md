---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269190"
---
# <span data-ttu-id="b7c4f-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b7c4f-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="b7c4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c4f-103">Remove-AzExpressRouteGateway cmdlet tar bort en Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="b7c4f-104">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="b7c4f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7c4f-105">SYNTAX</span></span>

### <span data-ttu-id="b7c4f-106">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="b7c4f-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c4f-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b7c4f-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c4f-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c4f-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c4f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7c4f-109">DESCRIPTION</span></span>
<span data-ttu-id="b7c4f-110">Remove-AzExpressRouteGateway cmdlet tar bort en Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="b7c4f-111">Det här är en gateway som är specifik för den program varu anslutning som definierats i Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="b7c4f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7c4f-112">EXAMPLES</span></span>

### <span data-ttu-id="b7c4f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7c4f-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="b7c4f-114">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, skalbar ExpressRoute gateway i Central USA och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="b7c4f-115">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="b7c4f-116">Detta tar bort ExpressRouteGateway och alla ExpressRouteConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="b7c4f-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b7c4f-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="b7c4f-118">I det här exemplet skapas en resurs grupp, virtuellt WAN, virtuellt nav, skalbar ExpressRoute gateway i västra Central USA och sedan omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="b7c4f-119">Denna borttagning sker med PowerShell-rör som använder ExpressRouteGateway-objektet som returneras av kommandot Get-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="b7c4f-120">Använd flaggan-Force för att utelämna uppmaningen när du tar bort den virtuella gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="b7c4f-121">Detta tar bort ExpressRouteGateway och alla ExpressRouteConnections som är kopplade till den.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="b7c4f-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7c4f-122">PARAMETERS</span></span>

### <span data-ttu-id="b7c4f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c4f-123">-DefaultProfile</span></span>
<span data-ttu-id="b7c4f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c4f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b7c4f-125">-Force</span></span>
<span data-ttu-id="b7c4f-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7c4f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7c4f-127">-InputObject</span></span>
<span data-ttu-id="b7c4f-128">ExpressRouteGateway-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c4f-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7c4f-129">-Name</span></span>
<span data-ttu-id="b7c4f-130">ExpressRouteGateway namn.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c4f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7c4f-131">-PassThru</span></span>
<span data-ttu-id="b7c4f-132">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7c4f-133">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7c4f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c4f-134">-ResourceGroupName</span></span>
<span data-ttu-id="b7c4f-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c4f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c4f-136">-ResourceId</span></span>
<span data-ttu-id="b7c4f-137">Azure Resource ID för ExpressRouteGateway ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c4f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7c4f-138">-Confirm</span></span>
<span data-ttu-id="b7c4f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c4f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c4f-140">-WhatIf</span></span>
<span data-ttu-id="b7c4f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c4f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c4f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c4f-143">CommonParameters</span></span>
<span data-ttu-id="b7c4f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c4f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c4f-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c4f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c4f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7c4f-146">INPUTS</span></span>

### <span data-ttu-id="b7c4f-147">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b7c4f-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="b7c4f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c4f-148">System.String</span></span>

## <span data-ttu-id="b7c4f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7c4f-149">OUTPUTS</span></span>

### <span data-ttu-id="b7c4f-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7c4f-150">System.Boolean</span></span>

## <span data-ttu-id="b7c4f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7c4f-151">NOTES</span></span>

## <span data-ttu-id="b7c4f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7c4f-152">RELATED LINKS</span></span>
