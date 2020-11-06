---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573748"
---
# <span data-ttu-id="8132e-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8132e-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="8132e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8132e-102">SYNOPSIS</span></span>
<span data-ttu-id="8132e-103">Uppdaterar distribution av en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="8132e-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8132e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8132e-104">SYNTAX</span></span>

### <span data-ttu-id="8132e-105">Specifik API-hanterings tjänst (standard)</span><span class="sxs-lookup"><span data-stu-id="8132e-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8132e-106">Uppdatera från PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="8132e-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8132e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8132e-107">DESCRIPTION</span></span>
<span data-ttu-id="8132e-108">Cmdleten **Update-AzureRmApiManagementDeployment** uppdaterar nuvarande distributioner av en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="8132e-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="8132e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8132e-109">EXAMPLES</span></span>

### <span data-ttu-id="8132e-110">Exempel 1: uppdatera en distribution av en ApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="8132e-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="8132e-111">Det här kommandot uppdaterar distributionen av en API-hanterings instans till en tre enhets kapacitets standard.</span><span class="sxs-lookup"><span data-stu-id="8132e-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="8132e-112">Exempel 2: skaffa en ApiManagement-förekomst och skala den</span><span class="sxs-lookup"><span data-stu-id="8132e-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="8132e-113">Det här exemplet får en API-hanterings instans, ändrar den till fem premie enheter och lägger sedan till ytterligare tre enheter till Premium-området.</span><span class="sxs-lookup"><span data-stu-id="8132e-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="8132e-114">Exempel 3: uppdaterings distribution (externt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="8132e-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="8132e-115">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en extern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="8132e-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="8132e-116">Exempel 4: uppdaterings distribution (internt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="8132e-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="8132e-117">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en intern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="8132e-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="8132e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8132e-118">PARAMETERS</span></span>

### <span data-ttu-id="8132e-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="8132e-119">-AdditionalRegions</span></span>
<span data-ttu-id="8132e-120">Anger ytterligare distributions områden för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="8132e-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8132e-121">-ApiManagement</span></span>
<span data-ttu-id="8132e-122">Anger den **PsApiManagement** -instans som du vill hämta distributions konfigurationen från.</span><span class="sxs-lookup"><span data-stu-id="8132e-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="8132e-123">Använd den här parametern om instansen redan har alla nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="8132e-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-124">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="8132e-124">-Capacity</span></span>
<span data-ttu-id="8132e-125">Anger SKU-kapaciteten för huvud området för distribution av Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8132e-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="8132e-126">-Location</span></span>
<span data-ttu-id="8132e-127">Anger platsen för distributions området Master API Management.</span><span class="sxs-lookup"><span data-stu-id="8132e-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="8132e-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8132e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8132e-129">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="8132e-129">North Central US</span></span>
- <span data-ttu-id="8132e-130">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="8132e-130">South Central US</span></span>
- <span data-ttu-id="8132e-131">Central</span><span class="sxs-lookup"><span data-stu-id="8132e-131">Central US</span></span>
- <span data-ttu-id="8132e-132">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="8132e-132">West Europe</span></span>
- <span data-ttu-id="8132e-133">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="8132e-133">North Europe</span></span>
- <span data-ttu-id="8132e-134">Västra USA</span><span class="sxs-lookup"><span data-stu-id="8132e-134">West US</span></span>
- <span data-ttu-id="8132e-135">Östra USA</span><span class="sxs-lookup"><span data-stu-id="8132e-135">East US</span></span>
- <span data-ttu-id="8132e-136">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="8132e-136">East US 2</span></span>
- <span data-ttu-id="8132e-137">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="8132e-137">Japan East</span></span>
- <span data-ttu-id="8132e-138">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="8132e-138">Japan West</span></span>
- <span data-ttu-id="8132e-139">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="8132e-139">Brazil South</span></span>
- <span data-ttu-id="8132e-140">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="8132e-140">Southeast Asia</span></span>
- <span data-ttu-id="8132e-141">Östasien</span><span class="sxs-lookup"><span data-stu-id="8132e-141">East Asia</span></span>
- <span data-ttu-id="8132e-142">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="8132e-142">Australia East</span></span>
- <span data-ttu-id="8132e-143">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="8132e-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="8132e-144">-Name</span></span>
<span data-ttu-id="8132e-145">Anger namnet på API-hanteringen som uppdateras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8132e-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8132e-146">-PassThru</span></span>
<span data-ttu-id="8132e-147">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="8132e-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8132e-148">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8132e-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8132e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8132e-149">-ResourceGroupName</span></span>
<span data-ttu-id="8132e-150">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="8132e-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="8132e-151">-Sku</span></span>
<span data-ttu-id="8132e-152">Anger nivån för distributions området för Master API-hantering för Azure.</span><span class="sxs-lookup"><span data-stu-id="8132e-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="8132e-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8132e-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8132e-154">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="8132e-154">Developer</span></span>
- <span data-ttu-id="8132e-155">Standar</span><span class="sxs-lookup"><span data-stu-id="8132e-155">Standard</span></span>
- <span data-ttu-id="8132e-156">Beta</span><span class="sxs-lookup"><span data-stu-id="8132e-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8132e-157">-VirtualNetwork</span></span>
<span data-ttu-id="8132e-158">Anger virtuell nätverks konfiguration för distributions regionen Master API Management.</span><span class="sxs-lookup"><span data-stu-id="8132e-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="8132e-159">-VpnType</span></span>
<span data-ttu-id="8132e-160">Anger den virtuella nätverks typen för API-hanterings distributionen.</span><span class="sxs-lookup"><span data-stu-id="8132e-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="8132e-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8132e-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8132e-162">Ingen.</span><span class="sxs-lookup"><span data-stu-id="8132e-162">None.</span></span>
<span data-ttu-id="8132e-163">API-hanterings distributionen är inte en del av något virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="8132e-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="8132e-164">Det här är standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="8132e-164">This is the default value.</span></span> 
- <span data-ttu-id="8132e-165">5,25.</span><span class="sxs-lookup"><span data-stu-id="8132e-165">External.</span></span>
<span data-ttu-id="8132e-166">Distributionen av API-hanteringen har en extern vänd virtuell adress.</span><span class="sxs-lookup"><span data-stu-id="8132e-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="8132e-167">Intern.</span><span class="sxs-lookup"><span data-stu-id="8132e-167">Internal.</span></span>
<span data-ttu-id="8132e-168">Distributionen av API-hanteringen har en vänd intranäts adress.</span><span class="sxs-lookup"><span data-stu-id="8132e-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8132e-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8132e-169">-DefaultProfile</span></span>
<span data-ttu-id="8132e-170">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8132e-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8132e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8132e-171">CommonParameters</span></span>
<span data-ttu-id="8132e-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8132e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8132e-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8132e-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8132e-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8132e-174">INPUTS</span></span>

### <span data-ttu-id="8132e-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8132e-175">PsApiManagement</span></span>
<span data-ttu-id="8132e-176">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8132e-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="8132e-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8132e-177">OUTPUTS</span></span>

### <span data-ttu-id="8132e-178">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8132e-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8132e-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8132e-179">NOTES</span></span>

## <span data-ttu-id="8132e-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8132e-180">RELATED LINKS</span></span>

[<span data-ttu-id="8132e-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8132e-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


