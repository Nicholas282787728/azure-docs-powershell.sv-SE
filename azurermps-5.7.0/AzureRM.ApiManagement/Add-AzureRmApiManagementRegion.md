---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586136"
---
# <span data-ttu-id="9ae9e-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9ae9e-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="9ae9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ae9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae9e-103">Lägger till nya distributions områden till en PsApiManagement-instans.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ae9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ae9e-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ae9e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae9e-106">Cmdleten **Add-AzureRmApiManagementRegion** lägger till en ny instans av typen **PsApiManagementRegion** till samlingen **AdditionalRegions** av angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9ae9e-107">Denna cmdlet distribuerar inte något automatiskt, utan uppdaterar en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9ae9e-108">Uppdatera en distribution av en API-hantering genom att överföra den ändrade **PsApiManagement** -instansen till Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="9ae9e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ae9e-109">EXAMPLES</span></span>

### <span data-ttu-id="9ae9e-110">Exempel 1: lägga till nya distributions områden i en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="9ae9e-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="9ae9e-111">Det här kommandot lägger till två Premium SKU-enheter och regionen "östra" till **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="9ae9e-112">Exempel 2: lägga till nya distributions områden till en PsApiManagement-instans och sedan uppdatera distributionen</span><span class="sxs-lookup"><span data-stu-id="9ae9e-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="9ae9e-113">Det här kommandot får ett **PsApiManagement** -objekt, lägger till två Premium SKU-enheter för den region som heter öst och sedan uppdaterar distribution.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="9ae9e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ae9e-114">PARAMETERS</span></span>

### <span data-ttu-id="9ae9e-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9ae9e-115">-ApiManagement</span></span>
<span data-ttu-id="9ae9e-116">Anger den **PsApiManagement** -instans som denna cmdlet lägger till ytterligare distributions områden till.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-117">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="9ae9e-117">-Capacity</span></span>
<span data-ttu-id="9ae9e-118">Anger SKU-kapaciteten för distributions området.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae9e-119">-DefaultProfile</span></span>
<span data-ttu-id="9ae9e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9ae9e-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="9ae9e-121">-Location</span></span>
<span data-ttu-id="9ae9e-122">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="9ae9e-123">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="9ae9e-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="9ae9e-124">-Sku</span></span>
<span data-ttu-id="9ae9e-125">Anger nivån för distributions området.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="9ae9e-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9ae9e-126">Valid values are:</span></span> 

- <span data-ttu-id="9ae9e-127">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="9ae9e-127">Developer</span></span>
- <span data-ttu-id="9ae9e-128">Standar</span><span class="sxs-lookup"><span data-stu-id="9ae9e-128">Standard</span></span>
- <span data-ttu-id="9ae9e-129">Beta</span><span class="sxs-lookup"><span data-stu-id="9ae9e-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ae9e-130">-VirtualNetwork</span></span>
<span data-ttu-id="9ae9e-131">Anger en virtuell nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae9e-132">CommonParameters</span></span>
<span data-ttu-id="9ae9e-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae9e-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae9e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae9e-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ae9e-135">INPUTS</span></span>

### <span data-ttu-id="9ae9e-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9ae9e-136">PsApiManagement</span></span>
<span data-ttu-id="9ae9e-137">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9ae9e-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9ae9e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ae9e-138">OUTPUTS</span></span>

### <span data-ttu-id="9ae9e-139">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9ae9e-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9ae9e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ae9e-140">NOTES</span></span>
* <span data-ttu-id="9ae9e-141">Cmdleten skriver den uppdaterade **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="9ae9e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ae9e-142">RELATED LINKS</span></span>

[<span data-ttu-id="9ae9e-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9ae9e-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9ae9e-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9ae9e-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9ae9e-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9ae9e-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

