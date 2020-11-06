---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576896"
---
# <span data-ttu-id="68fad-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="68fad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68fad-102">SYNOPSIS</span></span>
<span data-ttu-id="68fad-103">Skapar en Azure Express-vägkälla.</span><span class="sxs-lookup"><span data-stu-id="68fad-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68fad-104">SYNTAX</span></span>

### <span data-ttu-id="68fad-105">ServiceProvider</span><span class="sxs-lookup"><span data-stu-id="68fad-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fad-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="68fad-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68fad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68fad-107">DESCRIPTION</span></span>
<span data-ttu-id="68fad-108">Cmdleten **New-AzureRmExpressRouteCircuit** skapar en Azure Express Route-kretsen.</span><span class="sxs-lookup"><span data-stu-id="68fad-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="68fad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68fad-109">EXAMPLES</span></span>

### <span data-ttu-id="68fad-110">Exempel 1: skapa en ny ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="68fad-110">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

### <span data-ttu-id="68fad-111">Exempel 2: skapa en ny ExpressRoute-krets på ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="68fad-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="68fad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68fad-112">PARAMETERS</span></span>

### <span data-ttu-id="68fad-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="68fad-113">-AllowClassicOperations</span></span>
<span data-ttu-id="68fad-114">Genom att använda den här parametern kan du använda de klassiska Azure PowerShell-cmdletarna för att hantera kretsen.</span><span class="sxs-lookup"><span data-stu-id="68fad-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="68fad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68fad-115">-AsJob</span></span>
<span data-ttu-id="68fad-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="68fad-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68fad-117">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="68fad-117">-Authorization</span></span>
<span data-ttu-id="68fad-118">En lista över trafikgodkännanden.</span><span class="sxs-lookup"><span data-stu-id="68fad-118">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="68fad-119">-BandwidthInGbps</span></span>
<span data-ttu-id="68fad-120">Bandbredden för kretsen när kretsen etableras på en ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="68fad-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="68fad-121">-BandwidthInMbps</span></span>
<span data-ttu-id="68fad-122">Kretsens bandbredd.</span><span class="sxs-lookup"><span data-stu-id="68fad-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="68fad-123">Det måste vara ett värde som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="68fad-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fad-124">-DefaultProfile</span></span>
<span data-ttu-id="68fad-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68fad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fad-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="68fad-126">-ExpressRoutePort</span></span>
<span data-ttu-id="68fad-127">Referensen till ExpressRoutePort-resursen när kretsen etableras på en ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="68fad-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-128">-Force</span><span class="sxs-lookup"><span data-stu-id="68fad-128">-Force</span></span>
<span data-ttu-id="68fad-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="68fad-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68fad-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="68fad-130">-Location</span></span>
<span data-ttu-id="68fad-131">Placeringen av kretsen.</span><span class="sxs-lookup"><span data-stu-id="68fad-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="68fad-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="68fad-132">-Name</span></span>
<span data-ttu-id="68fad-133">Namnet på den ExpressRoute-krets som skapas.</span><span class="sxs-lookup"><span data-stu-id="68fad-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="68fad-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="68fad-134">-Peering</span></span>
<span data-ttu-id="68fad-135">En lista över peer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="68fad-135">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="68fad-136">-PeeringLocation</span></span>
<span data-ttu-id="68fad-137">Namnet på den peering-plats som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="68fad-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fad-138">-ResourceGroupName</span></span>
<span data-ttu-id="68fad-139">Resurs gruppen som ska innehålla kretsen.</span><span class="sxs-lookup"><span data-stu-id="68fad-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="68fad-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="68fad-140">-ServiceProviderName</span></span>
<span data-ttu-id="68fad-141">Namnet på kretskorts tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="68fad-141">The name of the circuit service provider.</span></span> <span data-ttu-id="68fad-142">Måste matcha ett namn som visas i Get-AzureRmExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fad-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="68fad-143">-SkuFamily</span></span>
<span data-ttu-id="68fad-144">SKU-familjen bestämmer fakturerings typen.</span><span class="sxs-lookup"><span data-stu-id="68fad-144">SKU family determines the billing type.</span></span> <span data-ttu-id="68fad-145">Möjliga värden för den här parametern är: `MeteredData` eller `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="68fad-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="68fad-146">Observera att du kan ändra fakturerings typen från MeteredData till UnlimitedData, men du kan inte ändra typen från UnlimitedData till MeteredData.</span><span class="sxs-lookup"><span data-stu-id="68fad-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="68fad-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="68fad-147">-SkuTier</span></span>
<span data-ttu-id="68fad-148">Tjänst nivån för kretsen.</span><span class="sxs-lookup"><span data-stu-id="68fad-148">The tier of service for the circuit.</span></span> <span data-ttu-id="68fad-149">Möjliga värden för den här parametern är: `Standard` eller `Premium` .</span><span class="sxs-lookup"><span data-stu-id="68fad-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fad-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="68fad-150">-Tag</span></span>
<span data-ttu-id="68fad-151">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="68fad-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="68fad-152">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="68fad-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="68fad-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68fad-153">-Confirm</span></span>
<span data-ttu-id="68fad-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68fad-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68fad-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68fad-155">-WhatIf</span></span>
<span data-ttu-id="68fad-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68fad-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68fad-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68fad-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68fad-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fad-158">CommonParameters</span></span>
<span data-ttu-id="68fad-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fad-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fad-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fad-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fad-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68fad-161">INPUTS</span></span>

### <span data-ttu-id="68fad-162">System. String</span><span class="sxs-lookup"><span data-stu-id="68fad-162">System.String</span></span>

### <span data-ttu-id="68fad-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="68fad-163">System.Int32</span></span>

### <span data-ttu-id="68fad-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSPeering, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="68fad-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="68fad-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="68fad-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="68fad-166">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="68fad-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="68fad-167">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="68fad-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="68fad-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68fad-168">OUTPUTS</span></span>

### <span data-ttu-id="68fad-169">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="68fad-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68fad-170">NOTES</span></span>

## <span data-ttu-id="68fad-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68fad-171">RELATED LINKS</span></span>

[<span data-ttu-id="68fad-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="68fad-173">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="68fad-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="68fad-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="68fad-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
