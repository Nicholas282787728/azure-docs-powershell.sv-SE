---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: 43084ab54ed20a094cc292eca2bf133598171f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928993"
---
# <span data-ttu-id="3e91e-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3e91e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e91e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e91e-103">Skapar en Azure Express-vägkälla.</span><span class="sxs-lookup"><span data-stu-id="3e91e-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e91e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e91e-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e91e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e91e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e91e-106">Cmdleten **New-AzureRmExpressRouteCircuit** skapar en Azure Express Route-kretsen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3e91e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e91e-107">EXAMPLES</span></span>

### <span data-ttu-id="3e91e-108">Exempel 1: skapa en ny ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="3e91e-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="3e91e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e91e-109">PARAMETERS</span></span>

### <span data-ttu-id="3e91e-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3e91e-110">-AllowClassicOperations</span></span>
<span data-ttu-id="3e91e-111">Genom att använda den här parametern kan du använda de klassiska Azure PowerShell-cmdletarna för att hantera kretsen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="3e91e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e91e-112">-AsJob</span></span>
<span data-ttu-id="3e91e-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e91e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e91e-114">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="3e91e-114">-Authorization</span></span>
<span data-ttu-id="3e91e-115">En lista över trafikgodkännanden.</span><span class="sxs-lookup"><span data-stu-id="3e91e-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="3e91e-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3e91e-116">-BandwidthInMbps</span></span>
<span data-ttu-id="3e91e-117">Kretsens bandbredd.</span><span class="sxs-lookup"><span data-stu-id="3e91e-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="3e91e-118">Det måste vara ett värde som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="3e91e-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="3e91e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e91e-119">-DefaultProfile</span></span>
<span data-ttu-id="3e91e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e91e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e91e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3e91e-121">-Force</span></span>
<span data-ttu-id="3e91e-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3e91e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e91e-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e91e-123">-Location</span></span>
<span data-ttu-id="3e91e-124">Placeringen av kretsen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="3e91e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e91e-125">-Name</span></span>
<span data-ttu-id="3e91e-126">Namnet på den ExpressRoute-krets som skapas.</span><span class="sxs-lookup"><span data-stu-id="3e91e-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="3e91e-127">-Peering</span><span class="sxs-lookup"><span data-stu-id="3e91e-127">-Peering</span></span>
<span data-ttu-id="3e91e-128">En lista över peer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="3e91e-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="3e91e-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3e91e-129">-PeeringLocation</span></span>
<span data-ttu-id="3e91e-130">Namnet på den peering-plats som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="3e91e-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="3e91e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e91e-131">-ResourceGroupName</span></span>
<span data-ttu-id="3e91e-132">Resurs gruppen som ska innehålla kretsen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="3e91e-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="3e91e-133">-ServiceProviderName</span></span>
<span data-ttu-id="3e91e-134">Namnet på kretskorts tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="3e91e-134">The name of the circuit service provider.</span></span> <span data-ttu-id="3e91e-135">Måste matcha ett namn som visas i Get-AzureRmExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e91e-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="3e91e-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3e91e-136">-SkuFamily</span></span>
<span data-ttu-id="3e91e-137">SKU-familjen bestämmer fakturerings typen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-137">SKU family determines the billing type.</span></span> <span data-ttu-id="3e91e-138">Möjliga värden för den här parametern är: `MeteredData` eller `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="3e91e-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3e91e-139">Observera att du kan ändra fakturerings typen från MeteredData till UnlimitedData, men du kan inte ändra typen från UnlimitedData till MeteredData.</span><span class="sxs-lookup"><span data-stu-id="3e91e-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="3e91e-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3e91e-140">-SkuTier</span></span>
<span data-ttu-id="3e91e-141">Tjänst nivån för kretsen.</span><span class="sxs-lookup"><span data-stu-id="3e91e-141">The tier of service for the circuit.</span></span> <span data-ttu-id="3e91e-142">Möjliga värden för den här parametern är: `Standard` eller `Premium` .</span><span class="sxs-lookup"><span data-stu-id="3e91e-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="3e91e-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e91e-143">-Tag</span></span>
<span data-ttu-id="3e91e-144">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e91e-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e91e-145">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3e91e-145">For example:</span></span>

<span data-ttu-id="3e91e-146">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3e91e-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3e91e-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e91e-147">-Confirm</span></span>
<span data-ttu-id="3e91e-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e91e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e91e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e91e-149">-WhatIf</span></span>
<span data-ttu-id="3e91e-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e91e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e91e-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e91e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e91e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e91e-152">CommonParameters</span></span>
<span data-ttu-id="3e91e-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e91e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e91e-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e91e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e91e-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e91e-155">INPUTS</span></span>

## <span data-ttu-id="3e91e-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e91e-156">OUTPUTS</span></span>

### <span data-ttu-id="3e91e-157">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3e91e-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e91e-158">NOTES</span></span>

## <span data-ttu-id="3e91e-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e91e-159">RELATED LINKS</span></span>

[<span data-ttu-id="3e91e-160">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-160">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3e91e-161">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-161">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3e91e-162">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-162">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3e91e-163">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3e91e-163">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
