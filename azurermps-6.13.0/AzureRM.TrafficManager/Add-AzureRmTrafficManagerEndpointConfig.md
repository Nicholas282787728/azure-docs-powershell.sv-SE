---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3c77ca67999ffa9cecbe35de4d4533f5d163f17f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584815"
---
# <span data-ttu-id="8cbc1-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8cbc1-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="8cbc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbc1-103">Lägger till en slut punkt till ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cbc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cbc1-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cbc1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cbc1-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbc1-106">Cmdleten **Add-AzureRmTrafficManagerEndpointConfig** lägger till en slut punkt till ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="8cbc1-107">Du kan hämta en profil med hjälp av New-AzureRmTrafficManagerProfile eller Get-AzureRmTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="8cbc1-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="8cbc1-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="8cbc1-110">Om du vill skapa en slut punkt och bekräfta ändringen i en enskild åtgärd, Använd cmdleten New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8cbc1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cbc1-111">EXAMPLES</span></span>

### <span data-ttu-id="8cbc1-112">Exempel 1: lägga till en slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="8cbc1-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="8cbc1-113">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="8cbc1-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="8cbc1-114">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="8cbc1-115">Det andra kommandot lägger till en slut punkt med namnet contoso till profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="8cbc1-116">Kommandot innehåller konfigurations data för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="8cbc1-117">Det här kommandot ändrar bara det lokala objektet.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-117">This command changes only the local object.</span></span>

<span data-ttu-id="8cbc1-118">Det sista kommandot uppdaterar Traffic Manager-profilen i Azure så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="8cbc1-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cbc1-119">PARAMETERS</span></span>

### <span data-ttu-id="8cbc1-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="8cbc1-120">-CustomHeader</span></span>
<span data-ttu-id="8cbc1-121">Lista över anpassade rubrik namn och värdepar för avsöknings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="8cbc1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-122">-DefaultProfile</span></span>
<span data-ttu-id="8cbc1-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cbc1-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="8cbc1-124">-EndpointLocation</span></span>
<span data-ttu-id="8cbc1-125">Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="8cbc1-126">Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints eller NestedEndpoints-typen.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="8cbc1-127">Du måste ange den här parametern när routningsmetoden för prestanda trafik används.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="8cbc1-128">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-128">Specify an Azure region name.</span></span>
<span data-ttu-id="8cbc1-129">En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="8cbc1-129">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="8cbc1-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8cbc1-130">-EndpointName</span></span>
<span data-ttu-id="8cbc1-131">Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8cbc1-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="8cbc1-132">-EndpointStatus</span></span>
<span data-ttu-id="8cbc1-133">Anger statusen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="8cbc1-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="8cbc1-134">Valid values are:</span></span> 

- <span data-ttu-id="8cbc1-135">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="8cbc1-135">Enabled</span></span> 
- <span data-ttu-id="8cbc1-136">Aktiv</span><span class="sxs-lookup"><span data-stu-id="8cbc1-136">Disabled</span></span> 

<span data-ttu-id="8cbc1-137">Om statusen är aktive rad avsöks slut punkten för slut punkts tillstånd och är inkluderad i Traffic routing-metoden.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="8cbc1-138">-Polymappning</span><span class="sxs-lookup"><span data-stu-id="8cbc1-138">-GeoMapping</span></span>
<span data-ttu-id="8cbc1-139">Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk".</span><span class="sxs-lookup"><span data-stu-id="8cbc1-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="8cbc1-140">Se dokumentationen för Traffic Manager för en [fullständig lista över godkända värden](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span><span class="sxs-lookup"><span data-stu-id="8cbc1-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="8cbc1-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="8cbc1-141">-MinChildEndpoints</span></span>
<span data-ttu-id="8cbc1-142">Det minsta antalet slut punkter som måste vara tillgängliga i den underordnade profilen för att den kapslade slut punkten i den överordnade profilen ska vara tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="8cbc1-143">Gäller endast för slut punkten av typen ' NestedEndpoints '.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="8cbc1-144">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="8cbc1-144">-Priority</span></span>
<span data-ttu-id="8cbc1-145">Anger den prioritet som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8cbc1-146">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med metoden för prioritets cirkulation.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="8cbc1-147">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8cbc1-148">Lägre värden är högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="8cbc1-149">Om du anger en prioritet måste du ange prioritet för alla slut punkter i profilen, och två slut punkter kan inte dela samma prioritets värde.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="8cbc1-150">Om du inte anger prioriteringar tilldelar trafik hanteraren standardvärden för prioritet till slut punkterna, med start från ett (1), i den ordning som profilen listar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="8cbc1-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="8cbc1-151">-SubnetMapping</span></span>
<span data-ttu-id="8cbc1-152">Listan med adress områden eller undernät som mappats till den här slut punkten när du använder ̃Subnetâ "™ trafik vägen".</span><span class="sxs-lookup"><span data-stu-id="8cbc1-152">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

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

### <span data-ttu-id="8cbc1-153">-Mål</span><span class="sxs-lookup"><span data-stu-id="8cbc1-153">-Target</span></span>
<span data-ttu-id="8cbc1-154">Anger slut punktens fullständiga DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="8cbc1-155">Traffic Manager returnerar detta värde i DNS-svar när det dirigerar trafik till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="8cbc1-156">Ange endast den här parametern för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="8cbc1-157">Ange parametern *TargetResourceId* i stället för andra slut punkts typer.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="8cbc1-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbc1-158">-TargetResourceId</span></span>
<span data-ttu-id="8cbc1-159">Anger målets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="8cbc1-160">Ange endast den här parametern för slut punkts typerna AzureEndpoints och NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="8cbc1-161">Ange parametern *target* för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="8cbc1-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="8cbc1-163">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="8cbc1-164">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8cbc1-165">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-165">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8cbc1-166">– Skriv</span><span class="sxs-lookup"><span data-stu-id="8cbc1-166">-Type</span></span>
<span data-ttu-id="8cbc1-167">Anger den typ av slut punkt som denna cmdlet lägger till i Azure Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8cbc1-168">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="8cbc1-168">Valid values are:</span></span> 

- <span data-ttu-id="8cbc1-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8cbc1-169">AzureEndpoints</span></span>
- <span data-ttu-id="8cbc1-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8cbc1-170">ExternalEndpoints</span></span>
- <span data-ttu-id="8cbc1-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="8cbc1-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="8cbc1-172">-Vikt</span><span class="sxs-lookup"><span data-stu-id="8cbc1-172">-Weight</span></span>
<span data-ttu-id="8cbc1-173">Anger den vikt som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8cbc1-174">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8cbc1-175">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="8cbc1-175">The default value is one (1).</span></span>
<span data-ttu-id="8cbc1-176">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med den viktade trafikdragnings metoden.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="8cbc1-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbc1-177">CommonParameters</span></span>
<span data-ttu-id="8cbc1-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbc1-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbc1-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbc1-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cbc1-180">INPUTS</span></span>

### <span data-ttu-id="8cbc1-181">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-181">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8cbc1-182">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-182">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="8cbc1-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cbc1-183">OUTPUTS</span></span>

### <span data-ttu-id="8cbc1-184">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-184">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8cbc1-185">Denna cmdlet returnerar ett ändrat **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8cbc1-185">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="8cbc1-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cbc1-186">NOTES</span></span>

## <span data-ttu-id="8cbc1-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cbc1-187">RELATED LINKS</span></span>

[<span data-ttu-id="8cbc1-188">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-188">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8cbc1-189">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cbc1-189">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8cbc1-190">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8cbc1-190">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="8cbc1-191">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc1-191">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


