---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: b180dabec976164eac70106b49378d832fb00db8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743434"
---
# <span data-ttu-id="78945-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="78945-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="78945-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78945-102">SYNOPSIS</span></span>
<span data-ttu-id="78945-103">Lägger till nya distributions områden till en PsApiManagement-instans.</span><span class="sxs-lookup"><span data-stu-id="78945-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="78945-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78945-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78945-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78945-105">DESCRIPTION</span></span>
<span data-ttu-id="78945-106">Cmdleten **Add-AzApiManagementRegion** lägger till en ny instans av typen **PsApiManagementRegion** till samlingen **AdditionalRegions** av angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="78945-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="78945-107">Denna cmdlet distribuerar inte något automatiskt, utan uppdaterar en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="78945-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="78945-108">Uppdatera en distribution av en API-hantering genom att överföra den ändrade **PsApiManagement** -instansen till Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="78945-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzApiManagementDeployment.</span></span>

## <span data-ttu-id="78945-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78945-109">EXAMPLES</span></span>

### <span data-ttu-id="78945-110">Exempel 1: lägga till nya distributions områden i en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="78945-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="78945-111">Det här kommandot lägger till två Premium SKU-enheter och regionen "östra" till **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="78945-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="78945-112">Exempel 2: lägga till nya distributions områden till en PsApiManagement-instans och sedan uppdatera distributionen</span><span class="sxs-lookup"><span data-stu-id="78945-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzApiManagementDeployment
```

<span data-ttu-id="78945-113">Det här kommandot får ett **PsApiManagement** -objekt, lägger till två Premium SKU-enheter för den region som heter öst och sedan uppdaterar distribution.</span><span class="sxs-lookup"><span data-stu-id="78945-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="78945-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78945-114">PARAMETERS</span></span>

### <span data-ttu-id="78945-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="78945-115">-ApiManagement</span></span>
<span data-ttu-id="78945-116">Anger den **PsApiManagement** -instans som denna cmdlet lägger till ytterligare distributions områden till.</span><span class="sxs-lookup"><span data-stu-id="78945-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="78945-117">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="78945-117">-Capacity</span></span>
<span data-ttu-id="78945-118">Anger SKU-kapaciteten för distributions området.</span><span class="sxs-lookup"><span data-stu-id="78945-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="78945-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78945-119">-DefaultProfile</span></span>
<span data-ttu-id="78945-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78945-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78945-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="78945-121">-Location</span></span>
<span data-ttu-id="78945-122">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="78945-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="78945-123">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="78945-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="78945-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="78945-124">-Sku</span></span>
<span data-ttu-id="78945-125">Anger nivån för distributions området.</span><span class="sxs-lookup"><span data-stu-id="78945-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="78945-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="78945-126">Valid values are:</span></span> 
- <span data-ttu-id="78945-127">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="78945-127">Developer</span></span>
- <span data-ttu-id="78945-128">Standar</span><span class="sxs-lookup"><span data-stu-id="78945-128">Standard</span></span>
- <span data-ttu-id="78945-129">Beta</span><span class="sxs-lookup"><span data-stu-id="78945-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78945-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="78945-130">-VirtualNetwork</span></span>
<span data-ttu-id="78945-131">Anger en virtuell nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="78945-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="78945-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78945-132">CommonParameters</span></span>
<span data-ttu-id="78945-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78945-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78945-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78945-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78945-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78945-135">INPUTS</span></span>

### <span data-ttu-id="78945-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="78945-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="78945-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78945-137">OUTPUTS</span></span>

### <span data-ttu-id="78945-138">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="78945-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="78945-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78945-139">NOTES</span></span>
* <span data-ttu-id="78945-140">Cmdleten skriver den uppdaterade **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="78945-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="78945-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78945-141">RELATED LINKS</span></span>

[<span data-ttu-id="78945-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="78945-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="78945-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="78945-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="78945-144">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="78945-144">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

