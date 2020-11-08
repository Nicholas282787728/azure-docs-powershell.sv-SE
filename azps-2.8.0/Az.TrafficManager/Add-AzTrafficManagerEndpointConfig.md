---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 0ad478b1e60008619e579abf868f4d6aba25bbd9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919878"
---
# <span data-ttu-id="d5efb-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d5efb-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="d5efb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5efb-102">SYNOPSIS</span></span>
<span data-ttu-id="d5efb-103">Lägger till en slut punkt till ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="d5efb-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d5efb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5efb-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5efb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5efb-105">DESCRIPTION</span></span>
<span data-ttu-id="d5efb-106">Cmdleten **Add-AzTrafficManagerEndpointConfig** lägger till en slut punkt till ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="d5efb-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d5efb-107">Du kan hämta en profil med hjälp av New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="d5efb-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="d5efb-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="d5efb-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d5efb-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5efb-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="d5efb-110">Om du vill skapa en slut punkt och bekräfta ändringen i en enskild åtgärd, Använd cmdleten New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d5efb-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="d5efb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5efb-111">EXAMPLES</span></span>

### <span data-ttu-id="d5efb-112">Exempel 1: lägga till en slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="d5efb-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d5efb-113">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="d5efb-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d5efb-114">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="d5efb-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="d5efb-115">Det andra kommandot lägger till en slut punkt med namnet contoso till profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d5efb-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d5efb-116">Kommandot innehåller konfigurations data för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d5efb-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="d5efb-117">Det här kommandot ändrar bara det lokala objektet.</span><span class="sxs-lookup"><span data-stu-id="d5efb-117">This command changes only the local object.</span></span>

<span data-ttu-id="d5efb-118">Det sista kommandot uppdaterar Traffic Manager-profilen i Azure så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d5efb-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d5efb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5efb-119">PARAMETERS</span></span>

### <span data-ttu-id="d5efb-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="d5efb-120">-CustomHeader</span></span>
<span data-ttu-id="d5efb-121">Lista över anpassade rubrik namn och värdepar för avsöknings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="d5efb-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-122">-DefaultProfile</span></span>
<span data-ttu-id="d5efb-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5efb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5efb-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="d5efb-124">-EndpointLocation</span></span>
<span data-ttu-id="d5efb-125">Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.</span><span class="sxs-lookup"><span data-stu-id="d5efb-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="d5efb-126">Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints eller NestedEndpoints-typen.</span><span class="sxs-lookup"><span data-stu-id="d5efb-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="d5efb-127">Du måste ange den här parametern när routningsmetoden för prestanda trafik används.</span><span class="sxs-lookup"><span data-stu-id="d5efb-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="d5efb-128">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="d5efb-128">Specify an Azure region name.</span></span>
<span data-ttu-id="d5efb-129">En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="d5efb-129">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d5efb-130">-EndpointName</span></span>
<span data-ttu-id="d5efb-131">Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="d5efb-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="d5efb-132">-EndpointStatus</span></span>
<span data-ttu-id="d5efb-133">Anger statusen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d5efb-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="d5efb-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="d5efb-134">Valid values are:</span></span> 

- <span data-ttu-id="d5efb-135">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="d5efb-135">Enabled</span></span> 
- <span data-ttu-id="d5efb-136">Aktiv</span><span class="sxs-lookup"><span data-stu-id="d5efb-136">Disabled</span></span> 

<span data-ttu-id="d5efb-137">Om statusen är aktive rad avsöks slut punkten för slut punkts tillstånd och är inkluderad i Traffic routing-metoden.</span><span class="sxs-lookup"><span data-stu-id="d5efb-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-138">-Polymappning</span><span class="sxs-lookup"><span data-stu-id="d5efb-138">-GeoMapping</span></span>
<span data-ttu-id="d5efb-139">Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk".</span><span class="sxs-lookup"><span data-stu-id="d5efb-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="d5efb-140">Se dokumentationen för Traffic Manager för en [fullständig lista över godkända värden](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span><span class="sxs-lookup"><span data-stu-id="d5efb-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="d5efb-141">-MinChildEndpoints</span></span>
<span data-ttu-id="d5efb-142">Det minsta antalet slut punkter som måste vara tillgängliga i den underordnade profilen för att den kapslade slut punkten i den överordnade profilen ska vara tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="d5efb-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="d5efb-143">Gäller endast för slut punkten av typen ' NestedEndpoints '.</span><span class="sxs-lookup"><span data-stu-id="d5efb-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-144">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="d5efb-144">-Priority</span></span>
<span data-ttu-id="d5efb-145">Anger den prioritet som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d5efb-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="d5efb-146">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med metoden för prioritets cirkulation.</span><span class="sxs-lookup"><span data-stu-id="d5efb-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="d5efb-147">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="d5efb-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="d5efb-148">Lägre värden är högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="d5efb-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="d5efb-149">Om du anger en prioritet måste du ange prioritet för alla slut punkter i profilen, och två slut punkter kan inte dela samma prioritets värde.</span><span class="sxs-lookup"><span data-stu-id="d5efb-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="d5efb-150">Om du inte anger prioriteringar tilldelar trafik hanteraren standardvärden för prioritet till slut punkterna, med start från ett (1), i den ordning som profilen listar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="d5efb-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="d5efb-151">-SubnetMapping</span></span>
<span data-ttu-id="d5efb-152">Listan över adress områden eller undernät som mappats till den här slut punkten vid användning av routing-metoden "subnet".</span><span class="sxs-lookup"><span data-stu-id="d5efb-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-153">-Mål</span><span class="sxs-lookup"><span data-stu-id="d5efb-153">-Target</span></span>
<span data-ttu-id="d5efb-154">Anger slut punktens fullständiga DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="d5efb-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="d5efb-155">Traffic Manager returnerar detta värde i DNS-svar när det dirigerar trafik till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d5efb-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="d5efb-156">Ange endast den här parametern för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d5efb-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="d5efb-157">Ange parametern *TargetResourceId* i stället för andra slut punkts typer.</span><span class="sxs-lookup"><span data-stu-id="d5efb-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d5efb-158">-TargetResourceId</span></span>
<span data-ttu-id="d5efb-159">Anger målets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d5efb-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="d5efb-160">Ange endast den här parametern för slut punkts typerna AzureEndpoints och NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d5efb-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="d5efb-161">Ange parametern *target* för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d5efb-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="d5efb-163">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5efb-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d5efb-164">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="d5efb-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d5efb-165">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d5efb-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-166">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d5efb-166">-Type</span></span>
<span data-ttu-id="d5efb-167">Anger den typ av slut punkt som denna cmdlet lägger till i Azure Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="d5efb-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d5efb-168">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="d5efb-168">Valid values are:</span></span> 

- <span data-ttu-id="d5efb-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d5efb-169">AzureEndpoints</span></span>
- <span data-ttu-id="d5efb-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d5efb-170">ExternalEndpoints</span></span>
- <span data-ttu-id="d5efb-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d5efb-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-172">-Vikt</span><span class="sxs-lookup"><span data-stu-id="d5efb-172">-Weight</span></span>
<span data-ttu-id="d5efb-173">Anger den vikt som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d5efb-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="d5efb-174">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="d5efb-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="d5efb-175">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="d5efb-175">The default value is one (1).</span></span>
<span data-ttu-id="d5efb-176">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med den viktade trafikdragnings metoden.</span><span class="sxs-lookup"><span data-stu-id="d5efb-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efb-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5efb-177">CommonParameters</span></span>
<span data-ttu-id="d5efb-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5efb-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5efb-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5efb-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5efb-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5efb-180">INPUTS</span></span>

### <span data-ttu-id="d5efb-181">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d5efb-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5efb-182">OUTPUTS</span></span>

### <span data-ttu-id="d5efb-183">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d5efb-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5efb-184">NOTES</span></span>

## <span data-ttu-id="d5efb-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5efb-185">RELATED LINKS</span></span>

[<span data-ttu-id="d5efb-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d5efb-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d5efb-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d5efb-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d5efb-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d5efb-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5efb-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

