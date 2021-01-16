---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421728"
---
# <span data-ttu-id="33b3e-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="33b3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="33b3e-103">Skapar en Azure-ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="33b3e-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="33b3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33b3e-104">SYNTAX</span></span>

### <span data-ttu-id="33b3e-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="33b3e-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33b3e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b3e-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33b3e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="33b3e-108">Cmdleten **New-AzExpressRoutePort** skapar en Azure-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="33b3e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33b3e-109">EXAMPLES</span></span>

### <span data-ttu-id="33b3e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="33b3e-110">Example 1</span></span>
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

### <span data-ttu-id="33b3e-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="33b3e-111">Example 2</span></span>
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

## <span data-ttu-id="33b3e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33b3e-112">PARAMETERS</span></span>

### <span data-ttu-id="33b3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33b3e-113">-AsJob</span></span>
<span data-ttu-id="33b3e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="33b3e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33b3e-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="33b3e-115">-BandwidthInGbps</span></span>
<span data-ttu-id="33b3e-116">Bandbredd för upphandlade portar i Gbit/s</span><span class="sxs-lookup"><span data-stu-id="33b3e-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="33b3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b3e-117">-DefaultProfile</span></span>
<span data-ttu-id="33b3e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33b3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b3e-119">-Inkapsling</span><span class="sxs-lookup"><span data-stu-id="33b3e-119">-Encapsulation</span></span>
<span data-ttu-id="33b3e-120">Inkapslings metod på fysiska portar.</span><span class="sxs-lookup"><span data-stu-id="33b3e-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="33b3e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33b3e-121">-Force</span></span>
<span data-ttu-id="33b3e-122">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="33b3e-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="33b3e-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="33b3e-123">-Identity</span></span>
<span data-ttu-id="33b3e-124">Tilldelad identitet för att läsa MacSec-konfiguration</span><span class="sxs-lookup"><span data-stu-id="33b3e-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3e-125">-Länk</span><span class="sxs-lookup"><span data-stu-id="33b3e-125">-Link</span></span>
<span data-ttu-id="33b3e-126">Uppsättningen med fysiska Länkar för ExpressRoutePort-resursen</span><span class="sxs-lookup"><span data-stu-id="33b3e-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="33b3e-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="33b3e-127">-Location</span></span>
<span data-ttu-id="33b3e-128">Platsen.</span><span class="sxs-lookup"><span data-stu-id="33b3e-128">The location.</span></span>

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

### <span data-ttu-id="33b3e-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="33b3e-129">-Name</span></span>
<span data-ttu-id="33b3e-130">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="33b3e-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="33b3e-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="33b3e-131">-PeeringLocation</span></span>
<span data-ttu-id="33b3e-132">Namnet på peering-platsen som ExpressRoutePort är mappad till fysiskt.</span><span class="sxs-lookup"><span data-stu-id="33b3e-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="33b3e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b3e-133">-ResourceGroupName</span></span>
<span data-ttu-id="33b3e-134">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="33b3e-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="33b3e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33b3e-135">-ResourceId</span></span>
<span data-ttu-id="33b3e-136">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="33b3e-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="33b3e-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="33b3e-137">-Tag</span></span>
<span data-ttu-id="33b3e-138">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="33b3e-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="33b3e-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33b3e-139">-Confirm</span></span>
<span data-ttu-id="33b3e-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33b3e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b3e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b3e-141">-WhatIf</span></span>
<span data-ttu-id="33b3e-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33b3e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33b3e-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33b3e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b3e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b3e-144">CommonParameters</span></span>
<span data-ttu-id="33b3e-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b3e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b3e-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b3e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b3e-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33b3e-147">INPUTS</span></span>

### <span data-ttu-id="33b3e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="33b3e-148">System.String</span></span>

### <span data-ttu-id="33b3e-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="33b3e-149">System.Int32</span></span>

### <span data-ttu-id="33b3e-150">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="33b3e-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="33b3e-151">Microsoft. Azure. commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="33b3e-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="33b3e-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33b3e-152">OUTPUTS</span></span>

### <span data-ttu-id="33b3e-153">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="33b3e-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33b3e-154">NOTES</span></span>

## <span data-ttu-id="33b3e-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33b3e-155">RELATED LINKS</span></span>

[<span data-ttu-id="33b3e-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="33b3e-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="33b3e-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="33b3e-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
