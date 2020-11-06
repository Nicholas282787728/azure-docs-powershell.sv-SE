---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576201"
---
# <span data-ttu-id="51a90-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51a90-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="51a90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51a90-102">SYNOPSIS</span></span>
<span data-ttu-id="51a90-103">Skapar en Azure-ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51a90-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51a90-104">SYNTAX</span></span>

### <span data-ttu-id="51a90-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51a90-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51a90-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51a90-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51a90-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51a90-107">DESCRIPTION</span></span>
<span data-ttu-id="51a90-108">Cmdleten **New-AzureRmExpressRoutePort** skapar en Azure-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51a90-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="51a90-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51a90-109">EXAMPLES</span></span>

### <span data-ttu-id="51a90-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51a90-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="51a90-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51a90-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="51a90-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51a90-112">PARAMETERS</span></span>

### <span data-ttu-id="51a90-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51a90-113">-AsJob</span></span>
<span data-ttu-id="51a90-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51a90-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51a90-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="51a90-115">-BandwidthInGbps</span></span>
<span data-ttu-id="51a90-116">Bandbredd för upphandlade portar i Gbit/s</span><span class="sxs-lookup"><span data-stu-id="51a90-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="51a90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a90-117">-DefaultProfile</span></span>
<span data-ttu-id="51a90-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51a90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a90-119">-Inkapsling</span><span class="sxs-lookup"><span data-stu-id="51a90-119">-Encapsulation</span></span>
<span data-ttu-id="51a90-120">Inkapslings metod på fysiska portar.</span><span class="sxs-lookup"><span data-stu-id="51a90-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="51a90-121">-Force</span><span class="sxs-lookup"><span data-stu-id="51a90-121">-Force</span></span>
<span data-ttu-id="51a90-122">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="51a90-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="51a90-123">-Länk</span><span class="sxs-lookup"><span data-stu-id="51a90-123">-Link</span></span>
<span data-ttu-id="51a90-124">Uppsättningen med fysiska Länkar för ExpressRoutePort-resursen</span><span class="sxs-lookup"><span data-stu-id="51a90-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51a90-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="51a90-125">-Location</span></span>
<span data-ttu-id="51a90-126">Platsen.</span><span class="sxs-lookup"><span data-stu-id="51a90-126">The location.</span></span>

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

### <span data-ttu-id="51a90-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="51a90-127">-Name</span></span>
<span data-ttu-id="51a90-128">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51a90-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="51a90-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="51a90-129">-PeeringLocation</span></span>
<span data-ttu-id="51a90-130">Namnet på peering-platsen som ExpressRoutePort är mappad till fysiskt.</span><span class="sxs-lookup"><span data-stu-id="51a90-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="51a90-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a90-131">-ResourceGroupName</span></span>
<span data-ttu-id="51a90-132">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51a90-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="51a90-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51a90-133">-ResourceId</span></span>
<span data-ttu-id="51a90-134">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="51a90-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="51a90-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="51a90-135">-Tag</span></span>
<span data-ttu-id="51a90-136">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="51a90-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="51a90-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51a90-137">-Confirm</span></span>
<span data-ttu-id="51a90-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51a90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a90-139">-WhatIf</span></span>
<span data-ttu-id="51a90-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51a90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a90-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51a90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a90-142">CommonParameters</span></span>
<span data-ttu-id="51a90-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a90-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a90-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a90-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51a90-145">INPUTS</span></span>

### <span data-ttu-id="51a90-146">System. String</span><span class="sxs-lookup"><span data-stu-id="51a90-146">System.String</span></span>

### <span data-ttu-id="51a90-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51a90-147">System.Int32</span></span>

### <span data-ttu-id="51a90-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="51a90-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="51a90-149">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSExpressRouteLink, Microsoft. Azure. commands. Network, version = 6.3.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="51a90-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51a90-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51a90-150">OUTPUTS</span></span>

### <span data-ttu-id="51a90-151">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51a90-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="51a90-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51a90-152">NOTES</span></span>

## <span data-ttu-id="51a90-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51a90-153">RELATED LINKS</span></span>
