---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: e28ebb5209736ad676404e11961d9095cc30da04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748084"
---
# <span data-ttu-id="b0799-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b0799-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0799-102">SYNOPSIS</span></span>
<span data-ttu-id="b0799-103">Skapar en Azure Express-vägkälla.</span><span class="sxs-lookup"><span data-stu-id="b0799-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="b0799-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0799-104">SYNTAX</span></span>

### <span data-ttu-id="b0799-105">ServiceProvider (standard)</span><span class="sxs-lookup"><span data-stu-id="b0799-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0799-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b0799-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0799-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0799-107">DESCRIPTION</span></span>
<span data-ttu-id="b0799-108">Cmdleten **New-AzExpressRouteCircuit** skapar en Azure Express Route-kretsen.</span><span class="sxs-lookup"><span data-stu-id="b0799-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="b0799-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0799-109">EXAMPLES</span></span>

### <span data-ttu-id="b0799-110">Exempel 1: skapa en ny ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="b0799-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="b0799-111">Exempel 2: skapa en ny ExpressRoute-krets på ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b0799-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="b0799-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0799-112">PARAMETERS</span></span>

### <span data-ttu-id="b0799-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="b0799-113">-AllowClassicOperations</span></span>
<span data-ttu-id="b0799-114">Genom att använda den här parametern kan du använda de klassiska Azure PowerShell-cmdletarna för att hantera kretsen.</span><span class="sxs-lookup"><span data-stu-id="b0799-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0799-115">-AsJob</span></span>
<span data-ttu-id="b0799-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0799-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0799-117">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="b0799-117">-Authorization</span></span>
<span data-ttu-id="b0799-118">En lista över trafikgodkännanden.</span><span class="sxs-lookup"><span data-stu-id="b0799-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="b0799-119">-BandwidthInGbps</span></span>
<span data-ttu-id="b0799-120">Bandbredden för kretsen när kretsen etableras på en ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="b0799-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b0799-121">-BandwidthInMbps</span></span>
<span data-ttu-id="b0799-122">Kretsens bandbredd.</span><span class="sxs-lookup"><span data-stu-id="b0799-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="b0799-123">Det måste vara ett värde som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="b0799-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0799-124">-DefaultProfile</span></span>
<span data-ttu-id="b0799-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0799-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0799-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b0799-126">-ExpressRoutePort</span></span>
<span data-ttu-id="b0799-127">Referensen till ExpressRoutePort-resursen när kretsen etableras på en ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="b0799-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b0799-128">-Force</span></span>
<span data-ttu-id="b0799-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b0799-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0799-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="b0799-130">-Location</span></span>
<span data-ttu-id="b0799-131">Placeringen av kretsen.</span><span class="sxs-lookup"><span data-stu-id="b0799-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="b0799-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0799-132">-Name</span></span>
<span data-ttu-id="b0799-133">Namnet på den ExpressRoute-krets som skapas.</span><span class="sxs-lookup"><span data-stu-id="b0799-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="b0799-134">-Peering</span></span>
<span data-ttu-id="b0799-135">En lista över peer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="b0799-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b0799-136">-PeeringLocation</span></span>
<span data-ttu-id="b0799-137">Namnet på den peering-plats som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="b0799-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0799-138">-ResourceGroupName</span></span>
<span data-ttu-id="b0799-139">Resurs gruppen som ska innehålla kretsen.</span><span class="sxs-lookup"><span data-stu-id="b0799-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="b0799-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="b0799-140">-ServiceProviderName</span></span>
<span data-ttu-id="b0799-141">Namnet på kretskorts tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="b0799-141">The name of the circuit service provider.</span></span> <span data-ttu-id="b0799-142">Måste matcha ett namn som visas i Get-AzExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0799-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="b0799-143">-SkuFamily</span></span>
<span data-ttu-id="b0799-144">SKU-familjen bestämmer fakturerings typen.</span><span class="sxs-lookup"><span data-stu-id="b0799-144">SKU family determines the billing type.</span></span> <span data-ttu-id="b0799-145">Möjliga värden för den här parametern är: `MeteredData` eller `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="b0799-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="b0799-146">Observera att du kan ändra fakturerings typen från MeteredData till UnlimitedData, men du kan inte ändra typen från UnlimitedData till MeteredData.</span><span class="sxs-lookup"><span data-stu-id="b0799-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b0799-147">-SkuTier</span></span>
<span data-ttu-id="b0799-148">Tjänst nivån för kretsen.</span><span class="sxs-lookup"><span data-stu-id="b0799-148">The tier of service for the circuit.</span></span> <span data-ttu-id="b0799-149">Möjliga värden för den här parametern är: `Standard` , `Premium` eller `Basic` .</span><span class="sxs-lookup"><span data-stu-id="b0799-149">Possible values for this parameter are: `Standard`, `Premium` or `Basic`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b0799-150">-Tag</span></span>
<span data-ttu-id="b0799-151">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b0799-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b0799-152">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b0799-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b0799-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0799-153">-Confirm</span></span>
<span data-ttu-id="b0799-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0799-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0799-155">-WhatIf</span></span>
<span data-ttu-id="b0799-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0799-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0799-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0799-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0799-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0799-158">CommonParameters</span></span>
<span data-ttu-id="b0799-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0799-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0799-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0799-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0799-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0799-161">INPUTS</span></span>

### <span data-ttu-id="b0799-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b0799-162">System.String</span></span>

### <span data-ttu-id="b0799-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b0799-163">System.Int32</span></span>

### <span data-ttu-id="b0799-164">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b0799-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="b0799-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="b0799-165">System.Double</span></span>

### <span data-ttu-id="b0799-166">Microsoft. Azure. commands. Network. Models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="b0799-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="b0799-167">Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="b0799-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="b0799-168">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b0799-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b0799-169">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b0799-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b0799-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0799-170">OUTPUTS</span></span>

### <span data-ttu-id="b0799-171">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b0799-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0799-172">NOTES</span></span>

## <span data-ttu-id="b0799-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0799-173">RELATED LINKS</span></span>

[<span data-ttu-id="b0799-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b0799-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="b0799-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="b0799-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b0799-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)