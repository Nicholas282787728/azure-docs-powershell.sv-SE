---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 7f6b68b02644b8244459398028680c9872fffa84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748072"
---
# <span data-ttu-id="25b46-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="25b46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25b46-102">SYNOPSIS</span></span>
<span data-ttu-id="25b46-103">Skapar en Azure-ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="25b46-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="25b46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25b46-104">SYNTAX</span></span>

### <span data-ttu-id="25b46-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25b46-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25b46-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25b46-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25b46-107">DESCRIPTION</span></span>
<span data-ttu-id="25b46-108">Cmdleten **New-AzExpressRoutePort** skapar en Azure-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="25b46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25b46-109">EXAMPLES</span></span>

### <span data-ttu-id="25b46-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25b46-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="25b46-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="25b46-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="25b46-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25b46-112">PARAMETERS</span></span>

### <span data-ttu-id="25b46-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25b46-113">-AsJob</span></span>
<span data-ttu-id="25b46-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="25b46-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25b46-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="25b46-115">-BandwidthInGbps</span></span>
<span data-ttu-id="25b46-116">Bandbredd för upphandlade portar i Gbit/s</span><span class="sxs-lookup"><span data-stu-id="25b46-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b46-117">-DefaultProfile</span></span>
<span data-ttu-id="25b46-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25b46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b46-119">-Inkapsling</span><span class="sxs-lookup"><span data-stu-id="25b46-119">-Encapsulation</span></span>
<span data-ttu-id="25b46-120">Inkapslings metod på fysiska portar.</span><span class="sxs-lookup"><span data-stu-id="25b46-120">Encapsulation method on physical ports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-121">-Force</span><span class="sxs-lookup"><span data-stu-id="25b46-121">-Force</span></span>
<span data-ttu-id="25b46-122">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="25b46-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="25b46-123">-Länk</span><span class="sxs-lookup"><span data-stu-id="25b46-123">-Link</span></span>
<span data-ttu-id="25b46-124">Uppsättningen med fysiska Länkar för ExpressRoutePort-resursen</span><span class="sxs-lookup"><span data-stu-id="25b46-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="25b46-125">-Location</span></span>
<span data-ttu-id="25b46-126">Platsen.</span><span class="sxs-lookup"><span data-stu-id="25b46-126">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="25b46-127">-Name</span></span>
<span data-ttu-id="25b46-128">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="25b46-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="25b46-129">-PeeringLocation</span></span>
<span data-ttu-id="25b46-130">Namnet på peering-platsen som ExpressRoutePort är mappad till fysiskt.</span><span class="sxs-lookup"><span data-stu-id="25b46-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b46-131">-ResourceGroupName</span></span>
<span data-ttu-id="25b46-132">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="25b46-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b46-133">-ResourceId</span></span>
<span data-ttu-id="25b46-134">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="25b46-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="25b46-135">-Tag</span></span>
<span data-ttu-id="25b46-136">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="25b46-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25b46-137">-Confirm</span></span>
<span data-ttu-id="25b46-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25b46-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b46-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b46-139">-WhatIf</span></span>
<span data-ttu-id="25b46-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25b46-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b46-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25b46-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b46-142">CommonParameters</span></span>
<span data-ttu-id="25b46-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b46-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b46-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b46-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25b46-145">INPUTS</span></span>

### <span data-ttu-id="25b46-146">System. String</span><span class="sxs-lookup"><span data-stu-id="25b46-146">System.String</span></span>

### <span data-ttu-id="25b46-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25b46-147">System.Int32</span></span>

### <span data-ttu-id="25b46-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="25b46-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="25b46-149">Microsoft. Azure. commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="25b46-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="25b46-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25b46-150">OUTPUTS</span></span>

### <span data-ttu-id="25b46-151">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="25b46-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25b46-152">NOTES</span></span>

## <span data-ttu-id="25b46-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25b46-153">RELATED LINKS</span></span>

[<span data-ttu-id="25b46-154">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-154">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="25b46-155">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-155">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="25b46-156">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="25b46-156">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
