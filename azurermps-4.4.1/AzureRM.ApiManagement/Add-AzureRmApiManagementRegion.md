---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583900"
---
# <span data-ttu-id="866cb-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="866cb-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="866cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="866cb-102">SYNOPSIS</span></span>
<span data-ttu-id="866cb-103">Lägger till nya distributions områden till en PsApiManagement-instans.</span><span class="sxs-lookup"><span data-stu-id="866cb-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="866cb-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="866cb-105">DESCRIPTION</span></span>
<span data-ttu-id="866cb-106">Cmdleten **Add-AzureRmApiManagementRegion** lägger till en ny instans av typen **PsApiManagementRegion** till samlingen **AdditionalRegions** av angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="866cb-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="866cb-107">Denna cmdlet distribuerar inte något automatiskt, utan uppdaterar en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="866cb-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="866cb-108">Uppdatera en distribution av en API-hantering genom att överföra den ändrade **PsApiManagement** -instansen till Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="866cb-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="866cb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="866cb-109">EXAMPLES</span></span>

### <span data-ttu-id="866cb-110">Exempel 1: lägga till nya distributions områden i en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="866cb-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="866cb-111">Det här kommandot lägger till två Premium SKU-enheter och regionen "östra" till **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="866cb-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="866cb-112">Exempel 2: lägga till nya distributions områden till en PsApiManagement-instans och sedan uppdatera distributionen</span><span class="sxs-lookup"><span data-stu-id="866cb-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="866cb-113">Det här kommandot får ett **PsApiManagement** -objekt, lägger till två Premium SKU-enheter för den region som heter öst och sedan uppdaterar distribution.</span><span class="sxs-lookup"><span data-stu-id="866cb-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="866cb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="866cb-114">PARAMETERS</span></span>

### <span data-ttu-id="866cb-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="866cb-115">-ApiManagement</span></span>
<span data-ttu-id="866cb-116">Anger den **PsApiManagement** -instans som denna cmdlet lägger till ytterligare distributions områden till.</span><span class="sxs-lookup"><span data-stu-id="866cb-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866cb-117">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="866cb-117">-Capacity</span></span>
<span data-ttu-id="866cb-118">Anger SKU-kapaciteten för distributions området.</span><span class="sxs-lookup"><span data-stu-id="866cb-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866cb-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="866cb-119">-Location</span></span>
<span data-ttu-id="866cb-120">Anger platsen för det nya distributions området.</span><span class="sxs-lookup"><span data-stu-id="866cb-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="866cb-121">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="866cb-121">Valid values are:</span></span> 

- <span data-ttu-id="866cb-122">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="866cb-122">North Central US</span></span>
- <span data-ttu-id="866cb-123">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="866cb-123">South Central US</span></span>
- <span data-ttu-id="866cb-124">Central</span><span class="sxs-lookup"><span data-stu-id="866cb-124">Central US</span></span>
- <span data-ttu-id="866cb-125">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="866cb-125">West Europe</span></span>
- <span data-ttu-id="866cb-126">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="866cb-126">North Europe</span></span>
- <span data-ttu-id="866cb-127">Västra USA</span><span class="sxs-lookup"><span data-stu-id="866cb-127">West US</span></span>
- <span data-ttu-id="866cb-128">Östra USA</span><span class="sxs-lookup"><span data-stu-id="866cb-128">East US</span></span>
- <span data-ttu-id="866cb-129">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="866cb-129">East US 2</span></span>
- <span data-ttu-id="866cb-130">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="866cb-130">Japan East</span></span>
- <span data-ttu-id="866cb-131">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="866cb-131">Japan West</span></span>
- <span data-ttu-id="866cb-132">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="866cb-132">Brazil South</span></span>
- <span data-ttu-id="866cb-133">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="866cb-133">Southeast Asia</span></span>
- <span data-ttu-id="866cb-134">Östasien</span><span class="sxs-lookup"><span data-stu-id="866cb-134">East Asia</span></span>
- <span data-ttu-id="866cb-135">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="866cb-135">Australia East</span></span>
- <span data-ttu-id="866cb-136">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="866cb-136">Australia Southeast</span></span>

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

### <span data-ttu-id="866cb-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="866cb-137">-Sku</span></span>
<span data-ttu-id="866cb-138">Anger nivån för distributions området.</span><span class="sxs-lookup"><span data-stu-id="866cb-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="866cb-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="866cb-139">Valid values are:</span></span> 

- <span data-ttu-id="866cb-140">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="866cb-140">Developer</span></span>
- <span data-ttu-id="866cb-141">Standar</span><span class="sxs-lookup"><span data-stu-id="866cb-141">Standard</span></span>
- <span data-ttu-id="866cb-142">Beta</span><span class="sxs-lookup"><span data-stu-id="866cb-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866cb-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="866cb-143">-VirtualNetwork</span></span>
<span data-ttu-id="866cb-144">Anger en virtuell nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="866cb-144">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866cb-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866cb-145">-DefaultProfile</span></span>
<span data-ttu-id="866cb-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="866cb-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866cb-147">CommonParameters</span></span>
<span data-ttu-id="866cb-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866cb-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866cb-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866cb-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="866cb-150">INPUTS</span></span>

### <span data-ttu-id="866cb-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="866cb-151">PsApiManagement</span></span>
<span data-ttu-id="866cb-152">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="866cb-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="866cb-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="866cb-153">OUTPUTS</span></span>

### <span data-ttu-id="866cb-154">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="866cb-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="866cb-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="866cb-155">NOTES</span></span>
* <span data-ttu-id="866cb-156">Cmdleten skriver den uppdaterade **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="866cb-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="866cb-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="866cb-157">RELATED LINKS</span></span>

[<span data-ttu-id="866cb-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="866cb-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="866cb-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="866cb-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="866cb-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="866cb-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


