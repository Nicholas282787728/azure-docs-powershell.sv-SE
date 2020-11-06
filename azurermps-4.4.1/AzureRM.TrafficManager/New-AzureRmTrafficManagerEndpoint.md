---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573613"
---
# <span data-ttu-id="0da53-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="0da53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0da53-102">SYNOPSIS</span></span>
<span data-ttu-id="0da53-103">Skapar en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="0da53-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0da53-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0da53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0da53-105">DESCRIPTION</span></span>
<span data-ttu-id="0da53-106">Cmdleten **New-AzureRmTrafficManagerEndpoint** skapar en slut punkt i en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="0da53-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="0da53-107">Denna cmdlet aktiverar varje ny slut punkt till Traffic Manager-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0da53-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="0da53-108">Om du vill lägga till flera slut punkter i ett lokalt Traffic Manager-Profile-objekt och genomföra ändringar i en enskild åtgärd använder du Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da53-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="0da53-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0da53-109">EXAMPLES</span></span>

### <span data-ttu-id="0da53-110">Exempel 1: skapa en extern slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="0da53-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="0da53-111">Det här kommandot skapar en extern slut punkt som heter Contoso i profilen med namnet ContosoProfile i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0da53-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="0da53-112">Exempel 2: skapa en Azure-slutpunkt för en profil</span><span class="sxs-lookup"><span data-stu-id="0da53-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="0da53-113">Det här kommandot skapar en Azure-slutpunkt som heter Contoso i profilen med namnet ContosoProfile i ResouceGroup11 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0da53-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="0da53-114">Azure-slutpunkten pekar på Azure Web App vars Azure Resource Manager-ID anges av URI-sökvägen i *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="0da53-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="0da53-115">Kommandot anger inte *EndpointLocation* -parametern eftersom Web App-resursen tillhandahåller platsen.</span><span class="sxs-lookup"><span data-stu-id="0da53-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="0da53-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0da53-116">PARAMETERS</span></span>

### <span data-ttu-id="0da53-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="0da53-117">-EndpointLocation</span></span>
<span data-ttu-id="0da53-118">Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.</span><span class="sxs-lookup"><span data-stu-id="0da53-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="0da53-119">Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints-eller NestedEndpoints-typen.</span><span class="sxs-lookup"><span data-stu-id="0da53-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="0da53-120">Du måste ange den här parametern när routningsmetoden för prestanda trafik används.</span><span class="sxs-lookup"><span data-stu-id="0da53-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="0da53-121">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="0da53-121">Specify an Azure region name.</span></span>
<span data-ttu-id="0da53-122">En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="0da53-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="0da53-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="0da53-123">-EndpointStatus</span></span>
<span data-ttu-id="0da53-124">Anger statusen för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0da53-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="0da53-125">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0da53-125">Valid values are:</span></span> 

- <span data-ttu-id="0da53-126">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="0da53-126">Enabled</span></span> 
- <span data-ttu-id="0da53-127">Aktiv</span><span class="sxs-lookup"><span data-stu-id="0da53-127">Disabled</span></span> 

<span data-ttu-id="0da53-128">Om statusen är aktive rad avsöks slut punkten för slut punkts tillstånd och är inkluderad i Traffic routing-metoden.</span><span class="sxs-lookup"><span data-stu-id="0da53-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="0da53-129">-Polymappning</span><span class="sxs-lookup"><span data-stu-id="0da53-129">-GeoMapping</span></span>
<span data-ttu-id="0da53-130">Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk".</span><span class="sxs-lookup"><span data-stu-id="0da53-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="0da53-131">Se dokumentationen för Traffic Manager för en fullständig lista över godkända värden.</span><span class="sxs-lookup"><span data-stu-id="0da53-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="0da53-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="0da53-132">-MinChildEndpoints</span></span>
<span data-ttu-id="0da53-133">Ange ett Azure region namn.</span><span class="sxs-lookup"><span data-stu-id="0da53-133">Specify an Azure region name.</span></span>
<span data-ttu-id="0da53-134">En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="0da53-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="0da53-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="0da53-135">-Name</span></span>
<span data-ttu-id="0da53-136">Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="0da53-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0da53-137">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="0da53-137">-Priority</span></span>
<span data-ttu-id="0da53-138">Anger den prioritet som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0da53-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="0da53-139">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med metoden för prioritets cirkulation.</span><span class="sxs-lookup"><span data-stu-id="0da53-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="0da53-140">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="0da53-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="0da53-141">Lägre värden är högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="0da53-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="0da53-142">Om du anger en prioritet måste du ange prioritet för alla slut punkter i profilen, och två slut punkter kan inte dela samma prioritets värde.</span><span class="sxs-lookup"><span data-stu-id="0da53-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="0da53-143">Om du inte anger prioriteringar tilldelar trafik hanteraren standardvärden för prioritet till slut punkterna, med start från ett (1), i den ordning som profilen listar slut punkter.</span><span class="sxs-lookup"><span data-stu-id="0da53-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="0da53-144">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="0da53-144">-ProfileName</span></span>
<span data-ttu-id="0da53-145">Anger namnet på en Traffic Manager-profil där denna cmdlet lägger till en slut punkt.</span><span class="sxs-lookup"><span data-stu-id="0da53-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="0da53-146">För att få en profil, Använd New-AzureRmTrafficManagerProfile eller Get-AzureRmTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0da53-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="0da53-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da53-147">-ResourceGroupName</span></span>
<span data-ttu-id="0da53-148">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0da53-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0da53-149">Den här cmdleten skapar en Traffic Manager-slutpunkt i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0da53-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0da53-150">-Mål</span><span class="sxs-lookup"><span data-stu-id="0da53-150">-Target</span></span>
<span data-ttu-id="0da53-151">Anger slut punktens fullständiga DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="0da53-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="0da53-152">Traffic Manager returnerar detta värde i DNS-svar när det dirigerar trafik till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0da53-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="0da53-153">Ange endast den här parametern för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="0da53-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="0da53-154">Ange parametern *TargetResourceId* i stället för andra slut punkts typer.</span><span class="sxs-lookup"><span data-stu-id="0da53-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="0da53-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0da53-155">-TargetResourceId</span></span>
<span data-ttu-id="0da53-156">Anger målets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0da53-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="0da53-157">Ange endast den här parametern för slut punkts typerna AzureEndpoints och NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="0da53-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="0da53-158">Ange parametern *target* för slut punkts typen ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="0da53-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="0da53-159">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0da53-159">-Type</span></span>
<span data-ttu-id="0da53-160">Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="0da53-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="0da53-161">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="0da53-161">Valid values are:</span></span> 

- <span data-ttu-id="0da53-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="0da53-162">AzureEndpoints</span></span>
- <span data-ttu-id="0da53-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="0da53-163">ExternalEndpoints</span></span>
- <span data-ttu-id="0da53-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="0da53-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="0da53-165">-Vikt</span><span class="sxs-lookup"><span data-stu-id="0da53-165">-Weight</span></span>
<span data-ttu-id="0da53-166">Anger den vikt som trafik hanteraren tilldelar slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0da53-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="0da53-167">Giltiga värden är heltal från 1 till 1000.</span><span class="sxs-lookup"><span data-stu-id="0da53-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="0da53-168">Standardvärdet är ett (1).</span><span class="sxs-lookup"><span data-stu-id="0da53-168">The default value is one (1).</span></span>
<span data-ttu-id="0da53-169">Den här parametern används endast om Traffic Manager-profilen är konfigurerad med den viktade trafikdragnings metoden.</span><span class="sxs-lookup"><span data-stu-id="0da53-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="0da53-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da53-170">-DefaultProfile</span></span>
<span data-ttu-id="0da53-171">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0da53-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da53-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da53-172">CommonParameters</span></span>
<span data-ttu-id="0da53-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da53-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da53-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da53-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da53-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0da53-175">INPUTS</span></span>

## <span data-ttu-id="0da53-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0da53-176">OUTPUTS</span></span>

### <span data-ttu-id="0da53-177">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0da53-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0da53-178">NOTES</span></span>

## <span data-ttu-id="0da53-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0da53-179">RELATED LINKS</span></span>

[<span data-ttu-id="0da53-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0da53-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0da53-182">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0da53-183">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0da53-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0da53-184">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0da53-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0da53-185">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0da53-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0da53-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0da53-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


