---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 4a5c59f6cc561bdd5f12462aab1e4cd634e70fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576701"
---
# <span data-ttu-id="e95b2-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e95b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e95b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e95b2-103">Skapar en Azure Express-vägkälla.</span><span class="sxs-lookup"><span data-stu-id="e95b2-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e95b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e95b2-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e95b2-105">DESCRIPTION</span></span>
<span data-ttu-id="e95b2-106">Cmdleten **New-AzureRmExpressRouteCircuit** skapar en Azure Express Route-kretsen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="e95b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e95b2-107">EXAMPLES</span></span>

### <span data-ttu-id="e95b2-108">Exempel 1: skapa en ny ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="e95b2-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="e95b2-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e95b2-109">PARAMETERS</span></span>

### <span data-ttu-id="e95b2-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="e95b2-110">-AllowClassicOperations</span></span>
<span data-ttu-id="e95b2-111">Genom att använda den här parametern kan du använda de klassiska Azure PowerShell-cmdletarna för att hantera kretsen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="e95b2-112">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="e95b2-112">-Authorization</span></span>
<span data-ttu-id="e95b2-113">En lista över trafikgodkännanden.</span><span class="sxs-lookup"><span data-stu-id="e95b2-113">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="e95b2-114">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="e95b2-114">-BandwidthInMbps</span></span>
<span data-ttu-id="e95b2-115">Kretsens bandbredd.</span><span class="sxs-lookup"><span data-stu-id="e95b2-115">The bandwidth of the circuit.</span></span> <span data-ttu-id="e95b2-116">Det måste vara ett värde som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="e95b2-116">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="e95b2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e95b2-117">-Force</span></span>
<span data-ttu-id="e95b2-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e95b2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e95b2-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="e95b2-119">-Location</span></span>
<span data-ttu-id="e95b2-120">Placeringen av kretsen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-120">The location of the circuit.</span></span>

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

### <span data-ttu-id="e95b2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e95b2-121">-Name</span></span>
<span data-ttu-id="e95b2-122">Namnet på den ExpressRoute-krets som skapas.</span><span class="sxs-lookup"><span data-stu-id="e95b2-122">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="e95b2-123">-Peering</span><span class="sxs-lookup"><span data-stu-id="e95b2-123">-Peering</span></span>
<span data-ttu-id="e95b2-124">En lista över peer-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e95b2-124">A list peer configurations.</span></span>

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

### <span data-ttu-id="e95b2-125">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e95b2-125">-PeeringLocation</span></span>
<span data-ttu-id="e95b2-126">Namnet på den peering-plats som stöds av tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="e95b2-126">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="e95b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="e95b2-128">Resurs gruppen som ska innehålla kretsen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-128">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="e95b2-129">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="e95b2-129">-ServiceProviderName</span></span>
<span data-ttu-id="e95b2-130">Namnet på kretskorts tjänste leverantören.</span><span class="sxs-lookup"><span data-stu-id="e95b2-130">The name of the circuit service provider.</span></span> <span data-ttu-id="e95b2-131">Måste matcha ett namn som visas i Get-AzureRmExpressRouteServiceProvider cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95b2-131">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="e95b2-132">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="e95b2-132">-SkuFamily</span></span>
<span data-ttu-id="e95b2-133">SKU-familjen bestämmer fakturerings typen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-133">SKU family determines the billing type.</span></span> <span data-ttu-id="e95b2-134">Möjliga värden för den här parametern är: `MeteredData` eller `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="e95b2-134">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="e95b2-135">Observera att du kan ändra fakturerings typen från MeteredData till UnlimitedData, men du kan inte ändra typen från UnlimitedData till MeteredData.</span><span class="sxs-lookup"><span data-stu-id="e95b2-135">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="e95b2-136">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e95b2-136">-SkuTier</span></span>
<span data-ttu-id="e95b2-137">Tjänst nivån för kretsen.</span><span class="sxs-lookup"><span data-stu-id="e95b2-137">The tier of service for the circuit.</span></span> <span data-ttu-id="e95b2-138">Möjliga värden för den här parametern är: `Standard` eller `Premium` .</span><span class="sxs-lookup"><span data-stu-id="e95b2-138">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="e95b2-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e95b2-139">-Tag</span></span>
<span data-ttu-id="e95b2-140">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e95b2-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e95b2-141">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e95b2-141">For example:</span></span>

<span data-ttu-id="e95b2-142">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e95b2-142">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e95b2-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e95b2-143">-Confirm</span></span>
<span data-ttu-id="e95b2-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e95b2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95b2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95b2-145">-WhatIf</span></span>
<span data-ttu-id="e95b2-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e95b2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95b2-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e95b2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95b2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95b2-148">-DefaultProfile</span></span>
<span data-ttu-id="e95b2-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e95b2-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95b2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95b2-150">CommonParameters</span></span>
<span data-ttu-id="e95b2-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95b2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95b2-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95b2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95b2-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e95b2-153">INPUTS</span></span>

## <span data-ttu-id="e95b2-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e95b2-154">OUTPUTS</span></span>

### <span data-ttu-id="e95b2-155">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-155">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e95b2-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e95b2-156">NOTES</span></span>

## <span data-ttu-id="e95b2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e95b2-157">RELATED LINKS</span></span>

[<span data-ttu-id="e95b2-158">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-158">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e95b2-159">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-159">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e95b2-160">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-160">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e95b2-161">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e95b2-161">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
