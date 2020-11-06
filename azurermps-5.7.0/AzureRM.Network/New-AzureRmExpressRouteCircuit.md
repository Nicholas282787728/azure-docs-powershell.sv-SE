---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580339"
---
# <span data-ttu-id="97391-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="97391-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97391-102">SYNOPSIS</span></span>
<span data-ttu-id="97391-103">Skapar en Azure Express-vägkälla.</span><span class="sxs-lookup"><span data-stu-id="97391-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97391-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97391-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97391-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97391-105">DESCRIPTION</span></span>
<span data-ttu-id="97391-106">Cmdleten **New-AzureRmExpressRouteCircuit** skapar en Azure Express Route-kretsen.</span><span class="sxs-lookup"><span data-stu-id="97391-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="97391-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97391-107">EXAMPLES</span></span>

### <span data-ttu-id="97391-108">Exempel 1: skapa en ny ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="97391-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="97391-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97391-109">PARAMETERS</span></span>

### <span data-ttu-id="97391-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="97391-110">-AllowClassicOperations</span></span>
<span data-ttu-id="97391-111">Genom att använda den här parametern kan du använda de klassiska Azure PowerShell-cmdletarna för att hantera kretsen.</span><span class="sxs-lookup"><span data-stu-id="97391-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97391-112">-AsJob</span></span>
<span data-ttu-id="97391-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97391-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97391-114">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="97391-114">-Authorization</span></span>
<span data-ttu-id="97391-115">En lista över trafikgodkännanden.</span><span class="sxs-lookup"><span data-stu-id="97391-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="97391-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="97391-116">-BandwidthInMbps</span></span>
<span data-ttu-id="97391-117">Kretsens bandbredd.</span><span class="sxs-lookup"><span data-stu-id="97391-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="97391-118">Det måste vara ett värde som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="97391-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97391-119">-DefaultProfile</span></span>
<span data-ttu-id="97391-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97391-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97391-121">-Force</span><span class="sxs-lookup"><span data-stu-id="97391-121">-Force</span></span>
<span data-ttu-id="97391-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="97391-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97391-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="97391-123">-Location</span></span>
<span data-ttu-id="97391-124">Placeringen av kretsen.</span><span class="sxs-lookup"><span data-stu-id="97391-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="97391-125">-Name</span></span>
<span data-ttu-id="97391-126">Namnet på den ExpressRoute-krets som skapas.</span><span class="sxs-lookup"><span data-stu-id="97391-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-127">-Peering</span><span class="sxs-lookup"><span data-stu-id="97391-127">-Peering</span></span>
<span data-ttu-id="97391-128">En lista över peer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="97391-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="97391-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="97391-129">-PeeringLocation</span></span>
<span data-ttu-id="97391-130">Namnet på den peering-plats som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="97391-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97391-131">-ResourceGroupName</span></span>
<span data-ttu-id="97391-132">Resurs gruppen som ska innehålla kretsen.</span><span class="sxs-lookup"><span data-stu-id="97391-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="97391-133">-ServiceProviderName</span></span>
<span data-ttu-id="97391-134">Namnet på kretskorts tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="97391-134">The name of the circuit service provider.</span></span> <span data-ttu-id="97391-135">Måste matcha ett namn som visas i Get-AzureRmExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97391-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="97391-136">-SkuFamily</span></span>
<span data-ttu-id="97391-137">SKU-familjen bestämmer fakturerings typen.</span><span class="sxs-lookup"><span data-stu-id="97391-137">SKU family determines the billing type.</span></span> <span data-ttu-id="97391-138">Möjliga värden för den här parametern är: `MeteredData` eller `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="97391-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="97391-139">Observera att du kan ändra fakturerings typen från MeteredData till UnlimitedData, men du kan inte ändra typen från UnlimitedData till MeteredData.</span><span class="sxs-lookup"><span data-stu-id="97391-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="97391-140">-SkuTier</span></span>
<span data-ttu-id="97391-141">Tjänst nivån för kretsen.</span><span class="sxs-lookup"><span data-stu-id="97391-141">The tier of service for the circuit.</span></span> <span data-ttu-id="97391-142">Möjliga värden för den här parametern är: `Standard` eller `Premium` .</span><span class="sxs-lookup"><span data-stu-id="97391-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="97391-143">-Tag</span></span>
<span data-ttu-id="97391-144">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="97391-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97391-145">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="97391-145">For example:</span></span>

<span data-ttu-id="97391-146">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="97391-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97391-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97391-147">-Confirm</span></span>
<span data-ttu-id="97391-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97391-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97391-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97391-149">-WhatIf</span></span>
<span data-ttu-id="97391-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97391-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97391-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97391-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97391-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97391-152">CommonParameters</span></span>
<span data-ttu-id="97391-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97391-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97391-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97391-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97391-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97391-155">INPUTS</span></span>

### <span data-ttu-id="97391-156">Ingen</span><span class="sxs-lookup"><span data-stu-id="97391-156">None</span></span>
<span data-ttu-id="97391-157">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="97391-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97391-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97391-158">OUTPUTS</span></span>

### <span data-ttu-id="97391-159">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="97391-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97391-160">NOTES</span></span>

## <span data-ttu-id="97391-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97391-161">RELATED LINKS</span></span>

[<span data-ttu-id="97391-162">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="97391-163">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="97391-164">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="97391-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="97391-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
