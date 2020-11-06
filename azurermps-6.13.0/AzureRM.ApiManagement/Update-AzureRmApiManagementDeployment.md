---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574058"
---
# <span data-ttu-id="401d9-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="401d9-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="401d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="401d9-102">SYNOPSIS</span></span>
<span data-ttu-id="401d9-103">Uppdaterar distribution av en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="401d9-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="401d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="401d9-104">SYNTAX</span></span>

### <span data-ttu-id="401d9-105">UpdateSpecificService (standard)</span><span class="sxs-lookup"><span data-stu-id="401d9-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="401d9-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="401d9-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="401d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="401d9-107">DESCRIPTION</span></span>
<span data-ttu-id="401d9-108">Cmdleten **Update-AzureRmApiManagementDeployment** uppdaterar nuvarande distributioner av en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="401d9-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="401d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="401d9-109">EXAMPLES</span></span>

### <span data-ttu-id="401d9-110">Exempel 1: uppdatera en distribution av en ApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="401d9-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="401d9-111">Det här kommandot uppdaterar distributionen av en API-hanterings instans till en tre enhets kapacitets standard.</span><span class="sxs-lookup"><span data-stu-id="401d9-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="401d9-112">Exempel 2: skaffa en ApiManagement-förekomst och skala den</span><span class="sxs-lookup"><span data-stu-id="401d9-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="401d9-113">Det här exemplet får en API-hanterings instans, ändrar den till fem premie enheter och lägger sedan till ytterligare tre enheter till Premium-området.</span><span class="sxs-lookup"><span data-stu-id="401d9-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="401d9-114">Exempel 3: uppdaterings distribution (externt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="401d9-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="401d9-115">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en extern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="401d9-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="401d9-116">Exempel 4: uppdaterings distribution (internt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="401d9-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="401d9-117">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en intern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="401d9-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="401d9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="401d9-118">PARAMETERS</span></span>

### <span data-ttu-id="401d9-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="401d9-119">-AdditionalRegions</span></span>
<span data-ttu-id="401d9-120">Anger ytterligare distributions områden för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="401d9-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="401d9-121">-ApiManagement</span></span>
<span data-ttu-id="401d9-122">Anger den **PsApiManagement** -instans som du vill hämta distributions konfigurationen från.</span><span class="sxs-lookup"><span data-stu-id="401d9-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="401d9-123">Använd den här parametern om instansen redan har alla nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="401d9-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-124">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="401d9-124">-Capacity</span></span>
<span data-ttu-id="401d9-125">Anger SKU-kapaciteten för huvud området för distribution av Azure API-hantering.</span><span class="sxs-lookup"><span data-stu-id="401d9-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401d9-126">-DefaultProfile</span></span>
<span data-ttu-id="401d9-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="401d9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="401d9-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="401d9-128">-Location</span></span>
<span data-ttu-id="401d9-129">Anger platsen för distributions området Master API Management.</span><span class="sxs-lookup"><span data-stu-id="401d9-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="401d9-130">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="401d9-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="401d9-131">-Name</span></span>
<span data-ttu-id="401d9-132">Anger namnet på API-hanteringen som uppdateras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="401d9-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="401d9-133">-PassThru</span></span>
<span data-ttu-id="401d9-134">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="401d9-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="401d9-135">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="401d9-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="401d9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="401d9-136">-ResourceGroupName</span></span>
<span data-ttu-id="401d9-137">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="401d9-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="401d9-138">-Sku</span></span>
<span data-ttu-id="401d9-139">Anger nivån för distributions området för Master API-hantering för Azure.</span><span class="sxs-lookup"><span data-stu-id="401d9-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="401d9-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="401d9-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="401d9-141">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="401d9-141">Developer</span></span>
- <span data-ttu-id="401d9-142">Standar</span><span class="sxs-lookup"><span data-stu-id="401d9-142">Standard</span></span>
- <span data-ttu-id="401d9-143">Beta</span><span class="sxs-lookup"><span data-stu-id="401d9-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="401d9-144">-VirtualNetwork</span></span>
<span data-ttu-id="401d9-145">Anger virtuell nätverks konfiguration för distributions regionen Master API Management.</span><span class="sxs-lookup"><span data-stu-id="401d9-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="401d9-146">-VpnType</span></span>
<span data-ttu-id="401d9-147">Anger den virtuella nätverks typen för API-hanterings distributionen.</span><span class="sxs-lookup"><span data-stu-id="401d9-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="401d9-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="401d9-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="401d9-149">Ingen.</span><span class="sxs-lookup"><span data-stu-id="401d9-149">None.</span></span>
<span data-ttu-id="401d9-150">API-hanterings distributionen är inte en del av något virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="401d9-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="401d9-151">Det här är standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="401d9-151">This is the default value.</span></span> 
- <span data-ttu-id="401d9-152">5,25.</span><span class="sxs-lookup"><span data-stu-id="401d9-152">External.</span></span>
<span data-ttu-id="401d9-153">Distributionen av API-hanteringen har en extern vänd virtuell adress.</span><span class="sxs-lookup"><span data-stu-id="401d9-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="401d9-154">Intern.</span><span class="sxs-lookup"><span data-stu-id="401d9-154">Internal.</span></span>
<span data-ttu-id="401d9-155">Distributionen av API-hanteringen har en vänd intranäts adress.</span><span class="sxs-lookup"><span data-stu-id="401d9-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401d9-156">CommonParameters</span></span>
<span data-ttu-id="401d9-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401d9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401d9-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401d9-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401d9-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="401d9-159">INPUTS</span></span>

### <span data-ttu-id="401d9-160">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="401d9-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="401d9-161">Parametrar: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="401d9-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="401d9-162">System. String</span><span class="sxs-lookup"><span data-stu-id="401d9-162">System.String</span></span>

### <span data-ttu-id="401d9-163">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="401d9-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="401d9-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="401d9-164">System.Int32</span></span>

### <span data-ttu-id="401d9-165">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="401d9-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="401d9-166">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVpnType</span><span class="sxs-lookup"><span data-stu-id="401d9-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="401d9-167">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion, Microsoft. Azure. commands. ApiManagement, version = 6.1.2.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="401d9-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="401d9-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="401d9-168">OUTPUTS</span></span>

### <span data-ttu-id="401d9-169">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="401d9-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="401d9-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="401d9-170">NOTES</span></span>

## <span data-ttu-id="401d9-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="401d9-171">RELATED LINKS</span></span>

[<span data-ttu-id="401d9-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="401d9-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


