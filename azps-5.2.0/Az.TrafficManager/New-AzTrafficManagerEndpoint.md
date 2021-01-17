---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391440"
---
# <span data-ttu-id="1c0a5-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c0a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0a5-103">Skapar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="1c0a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c0a5-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c0a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c0a5-105">DESCRIPTION</span></span>
<span data-ttu-id="1c0a5-106">Cmdleten **New-AzTrafficManagerEndpoint** skapar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1c0a5-107">Denna cmdlet aktiverar varje ny slut punkt till Traffic Manager-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="1c0a5-108">Om du vill lägga till flera slut punkter i ett lokalt Traffic Manager-Profile-objekt och genomföra ändringar i en enskild åtgärd använder du Add-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="1c0a5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c0a5-109">EXAMPLES</span></span>

### <span data-ttu-id="1c0a5-110">Exempel 1: skapa en extern slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="1c0a5-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="1c0a5-111">Det här kommandot skapar en extern slut punkt som heter Contoso i profilen med namnet ContosoProfile i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="1c0a5-112">Exempel 2: skapa en Azure-slutpunkt för en profil</span><span class="sxs-lookup"><span data-stu-id="1c0a5-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="1c0a5-113">Det här kommandot skapar en Azure-slutpunkt som heter Contoso i profilen med namnet ContosoProfile i ResourceGroup11 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="1c0a5-114">Azure-slutpunkten pekar på Azure Web App vars Azure Resource Manager-ID anges av URI-sökvägen i *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="1c0a5-115">Kommandot anger inte *EndpointLocation* -parametern eftersom Web App-resursen tillhandahåller platsen.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="1c0a5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c0a5-116">PARAMETERS</span></span>

### <span data-ttu-id="1c0a5-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="1c0a5-117">-CustomHeader</span></span>
<span data-ttu-id="1c0a5-118">Lista över anpassade rubrik namn och värdepar för avsöknings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="1c0a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0a5-119">-DefaultProfile</span></span>
<span data-ttu-id="1c0a5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c0a5-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="1c0a5-121">-EndpointLocation</span></span>
<span data-ttu-id="1c0a5-122">Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="1c0a5-123">Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints-eller NestedEndpoints-typen.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="1c0a5-124">Du måste ange den här parametern när routningsmetoden för prestanda trafik används.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="1c0a5-125">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-125">Specify an Azure region name.</span></span>
<span data-ttu-id="1c0a5-126">En fullständig lista över Azure-regioner finns i Azure http://azure.microsoft.com/regions/ -regioner ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="1c0a5-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="1c0a5-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="1c0a5-127">-EndpointStatus</span></span>
<span data-ttu-id="1c0a5-128">Anger statusen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="1c0a5-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1c0a5-129">Valid values are:</span></span> 

- <span data-ttu-id="1c0a5-130">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="1c0a5-130">Enabled</span></span> 
- <span data-ttu-id="1c0a5-131">Aktiv</span><span class="sxs-lookup"><span data-stu-id="1c0a5-131">Disabled</span></span> 

<span data-ttu-id="1c0a5-132">Om statusen är aktive rad avsöks slut punkten för slut punkts tillstånd och är inkluderad i Traffic routing-metoden.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="1c0a5-133">-Polymappning</span><span class="sxs-lookup"><span data-stu-id="1c0a5-133">-GeoMapping</span></span>
<span data-ttu-id="1c0a5-134">Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk".</span><span class="sxs-lookup"><span data-stu-id="1c0a5-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="1c0a5-135">Se dokumentationen för Traffic Manager för en fullständig lista över godkända värden.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="1c0a5-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c0a5-136">-MinChildEndpoints</span></span>
<span data-ttu-id="1c0a5-137">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-137">Specify an Azure region name.</span></span>
<span data-ttu-id="1c0a5-138">En fullständig lista över Azure-regioner finns i Azure http://azure.microsoft.com/regions/ -regioner ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="1c0a5-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="1c0a5-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c0a5-139">-Name</span></span>
<span data-ttu-id="1c0a5-140">Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1c0a5-141">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="1c0a5-141">-Priority</span></span>
<span data-ttu-id="1c0a5-142">Anger den prioritet som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="1c0a5-143">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med metoden för prioritets cirkulation.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="1c0a5-144">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="1c0a5-145">Lägre värden är högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="1c0a5-146">Om du anger en prioritet måste du ange prioritet för alla slut punkter i profilen, och två slut punkter kan inte dela samma prioritets värde.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="1c0a5-147">Om du inte anger prioriteringar tilldelar trafik hanteraren standardvärden för prioritet till slut punkterna, med start från ett (1), i den ordning som profilen listar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="1c0a5-148">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="1c0a5-148">-ProfileName</span></span>
<span data-ttu-id="1c0a5-149">Anger namnet på en Traffic Manager-profil där denna cmdlet lägger till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="1c0a5-150">För att få en profil, Använd New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="1c0a5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0a5-151">-ResourceGroupName</span></span>
<span data-ttu-id="1c0a5-152">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1c0a5-153">Den här cmdleten skapar en Traffic Manager-slutpunkt i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c0a5-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="1c0a5-154">-SubnetMapping</span></span>
<span data-ttu-id="1c0a5-155">Listan över adress områden eller undernät som mappats till den här slut punkten vid användning av routing-metoden "subnet".</span><span class="sxs-lookup"><span data-stu-id="1c0a5-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="1c0a5-156">-Mål</span><span class="sxs-lookup"><span data-stu-id="1c0a5-156">-Target</span></span>
<span data-ttu-id="1c0a5-157">Anger slut punktens fullständiga DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="1c0a5-158">Traffic Manager returnerar detta värde i DNS-svar när det dirigerar trafik till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="1c0a5-159">Ange endast den här parametern för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="1c0a5-160">Ange parametern *TargetResourceId* i stället för andra slut punkts typer.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="1c0a5-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1c0a5-161">-TargetResourceId</span></span>
<span data-ttu-id="1c0a5-162">Anger målets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="1c0a5-163">Ange endast den här parametern för slut punkts typerna AzureEndpoints och NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="1c0a5-164">Ange parametern *target* för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="1c0a5-165">– Skriv</span><span class="sxs-lookup"><span data-stu-id="1c0a5-165">-Type</span></span>
<span data-ttu-id="1c0a5-166">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="1c0a5-167">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1c0a5-167">Valid values are:</span></span> 

- <span data-ttu-id="1c0a5-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c0a5-168">AzureEndpoints</span></span>
- <span data-ttu-id="1c0a5-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c0a5-169">ExternalEndpoints</span></span>
- <span data-ttu-id="1c0a5-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c0a5-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="1c0a5-171">-Vikt</span><span class="sxs-lookup"><span data-stu-id="1c0a5-171">-Weight</span></span>
<span data-ttu-id="1c0a5-172">Anger den vikt som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="1c0a5-173">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="1c0a5-174">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="1c0a5-174">The default value is one (1).</span></span>
<span data-ttu-id="1c0a5-175">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med den viktade trafikdragnings metoden.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="1c0a5-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0a5-176">CommonParameters</span></span>
<span data-ttu-id="1c0a5-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0a5-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0a5-178">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0a5-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0a5-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c0a5-179">INPUTS</span></span>

### <span data-ttu-id="1c0a5-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c0a5-180">None</span></span>

## <span data-ttu-id="1c0a5-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c0a5-181">OUTPUTS</span></span>

### <span data-ttu-id="1c0a5-182">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c0a5-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c0a5-183">NOTES</span></span>

## <span data-ttu-id="1c0a5-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c0a5-184">RELATED LINKS</span></span>

[<span data-ttu-id="1c0a5-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c0a5-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c0a5-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c0a5-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c0a5-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c0a5-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c0a5-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c0a5-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0a5-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c0a5-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c0a5-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


