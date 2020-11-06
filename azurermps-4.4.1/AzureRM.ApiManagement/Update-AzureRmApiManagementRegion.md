---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573745"
---
# <span data-ttu-id="f5b8d-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f5b8d-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="f5b8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b8d-103">Uppdaterar det befintliga distributions området i PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5b8d-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5b8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b8d-106">Cmdleten **Update-AzureRmApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion** i en samling **AdditionalRegions** -objekt av en angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f5b8d-107">Denna cmdlet distribuerar inte något men uppdaterar inte en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f5b8d-108">Om du vill uppdatera en distribution av en API-hantering använder du den ändrade **PsApiManagementInstance** till cmdleten Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="f5b8d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5b8d-109">EXAMPLES</span></span>

## <span data-ttu-id="f5b8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5b8d-110">PARAMETERS</span></span>

### <span data-ttu-id="f5b8d-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5b8d-111">-ApiManagement</span></span>
<span data-ttu-id="f5b8d-112">Anger den **PsApiManagement** -instans som du vill uppdatera ett befintligt distributions område i.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="f5b8d-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="f5b8d-113">-Capacity</span></span>
<span data-ttu-id="f5b8d-114">Anger det nya värdet för SKU-kapacitet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="f5b8d-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="f5b8d-115">-Location</span></span>
<span data-ttu-id="f5b8d-116">Anger platsen för det distributions område som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="f5b8d-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f5b8d-117">Valid values are:</span></span>

- <span data-ttu-id="f5b8d-118">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="f5b8d-118">North Central US</span></span>
- <span data-ttu-id="f5b8d-119">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="f5b8d-119">South Central US</span></span>
- <span data-ttu-id="f5b8d-120">Central</span><span class="sxs-lookup"><span data-stu-id="f5b8d-120">Central US</span></span>
- <span data-ttu-id="f5b8d-121">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="f5b8d-121">West Europe</span></span>
- <span data-ttu-id="f5b8d-122">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="f5b8d-122">North Europe</span></span>
- <span data-ttu-id="f5b8d-123">Västra USA</span><span class="sxs-lookup"><span data-stu-id="f5b8d-123">West US</span></span>
- <span data-ttu-id="f5b8d-124">Östra USA</span><span class="sxs-lookup"><span data-stu-id="f5b8d-124">East US</span></span>
- <span data-ttu-id="f5b8d-125">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="f5b8d-125">East US 2</span></span>
- <span data-ttu-id="f5b8d-126">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="f5b8d-126">Japan East</span></span>
- <span data-ttu-id="f5b8d-127">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="f5b8d-127">Japan West</span></span>
- <span data-ttu-id="f5b8d-128">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="f5b8d-128">Brazil South</span></span>
- <span data-ttu-id="f5b8d-129">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="f5b8d-129">Southeast Asia</span></span>
- <span data-ttu-id="f5b8d-130">Östasien</span><span class="sxs-lookup"><span data-stu-id="f5b8d-130">East Asia</span></span>
- <span data-ttu-id="f5b8d-131">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="f5b8d-131">Australia East</span></span>
- <span data-ttu-id="f5b8d-132">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="f5b8d-132">Australia Southeast</span></span>

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

### <span data-ttu-id="f5b8d-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f5b8d-133">-Sku</span></span>
<span data-ttu-id="f5b8d-134">Anger det nya nivå svärdet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="f5b8d-135">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f5b8d-135">Valid values are:</span></span>

- <span data-ttu-id="f5b8d-136">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="f5b8d-136">Developer</span></span>
- <span data-ttu-id="f5b8d-137">Standar</span><span class="sxs-lookup"><span data-stu-id="f5b8d-137">Standard</span></span>
- <span data-ttu-id="f5b8d-138">Beta</span><span class="sxs-lookup"><span data-stu-id="f5b8d-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b8d-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f5b8d-139">-VirtualNetwork</span></span>
<span data-ttu-id="f5b8d-140">Anger en virtuell nätverks konfiguration för distributions området.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="f5b8d-141">Om du överför $null tas nätverkets konfiguration för området bort.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-141">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b8d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b8d-142">-DefaultProfile</span></span>
<span data-ttu-id="f5b8d-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5b8d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b8d-144">CommonParameters</span></span>
<span data-ttu-id="f5b8d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b8d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b8d-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b8d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b8d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5b8d-147">INPUTS</span></span>

### <span data-ttu-id="f5b8d-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5b8d-148">PsApiManagement</span></span>
<span data-ttu-id="f5b8d-149">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f5b8d-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="f5b8d-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5b8d-150">OUTPUTS</span></span>

### <span data-ttu-id="f5b8d-151">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5b8d-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f5b8d-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5b8d-152">NOTES</span></span>

## <span data-ttu-id="f5b8d-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5b8d-153">RELATED LINKS</span></span>

[<span data-ttu-id="f5b8d-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f5b8d-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f5b8d-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f5b8d-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f5b8d-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f5b8d-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
