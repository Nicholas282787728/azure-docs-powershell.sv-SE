---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 8552592acb45702c866c8d918121b8dd61d126a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423083"
---
# <span data-ttu-id="5a329-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5a329-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="5a329-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a329-102">SYNOPSIS</span></span>
<span data-ttu-id="5a329-103">Uppdaterar det befintliga distributions området i PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="5a329-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="5a329-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a329-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a329-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a329-105">DESCRIPTION</span></span>
<span data-ttu-id="5a329-106">Cmdleten **Update-AzApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion** i en samling **AdditionalRegions** -objekt av en angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="5a329-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="5a329-107">Denna cmdlet distribuerar inte något men uppdaterar inte en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="5a329-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="5a329-108">Om du vill uppdatera en distribution av en API-hantering använder du den ändrade **PsApiManagementInstance** till cmdleten Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5a329-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="5a329-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a329-109">EXAMPLES</span></span>

### <span data-ttu-id="5a329-110">Exempel 1: ökar kapaciteten för ytterligare områden i en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="5a329-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="5a329-111">Det här kommandot får API Management Premium SKU-tjänsten med regioner i södra centrala USA och norra centrala USA.</span><span class="sxs-lookup"><span data-stu-id="5a329-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="5a329-112">Därefter ökar kapaciteten för Nord Central USA-regionen till 2 med hjälp av **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="5a329-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="5a329-113">Nästa cmdlet **set-AzApiManagement** tillämpar konfigurations ändringen för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5a329-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="5a329-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5a329-114">Example 2</span></span>

<span data-ttu-id="5a329-115">Uppdaterar det befintliga distributions området i PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="5a329-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="5a329-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="5a329-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="5a329-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a329-117">PARAMETERS</span></span>

### <span data-ttu-id="5a329-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a329-118">-ApiManagement</span></span>
<span data-ttu-id="5a329-119">Anger den **PsApiManagement** -instans som du vill uppdatera ett befintligt distributions område i.</span><span class="sxs-lookup"><span data-stu-id="5a329-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="5a329-120">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="5a329-120">-Capacity</span></span>
<span data-ttu-id="5a329-121">Anger det nya värdet för SKU-kapacitet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="5a329-121">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="5a329-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a329-122">-DefaultProfile</span></span>
<span data-ttu-id="5a329-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a329-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a329-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a329-124">-Location</span></span>
<span data-ttu-id="5a329-125">Anger platsen för det distributions område som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="5a329-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="5a329-126">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5a329-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="5a329-127">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="5a329-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="5a329-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="5a329-128">-Sku</span></span>
<span data-ttu-id="5a329-129">Anger det nya nivå svärdet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="5a329-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="5a329-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="5a329-130">Valid values are:</span></span>
- <span data-ttu-id="5a329-131">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="5a329-131">Developer</span></span>
- <span data-ttu-id="5a329-132">Standar</span><span class="sxs-lookup"><span data-stu-id="5a329-132">Standard</span></span>
- <span data-ttu-id="5a329-133">Beta</span><span class="sxs-lookup"><span data-stu-id="5a329-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a329-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a329-134">-VirtualNetwork</span></span>
<span data-ttu-id="5a329-135">Anger en virtuell nätverks konfiguration för distributions området.</span><span class="sxs-lookup"><span data-stu-id="5a329-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="5a329-136">Om du överför $null tas nätverkets konfiguration för området bort.</span><span class="sxs-lookup"><span data-stu-id="5a329-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="5a329-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a329-137">CommonParameters</span></span>
<span data-ttu-id="5a329-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a329-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a329-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a329-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a329-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a329-140">INPUTS</span></span>

### <span data-ttu-id="5a329-141">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a329-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="5a329-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5a329-142">System.String</span></span>

### <span data-ttu-id="5a329-143">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="5a329-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="5a329-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5a329-144">System.Int32</span></span>

### <span data-ttu-id="5a329-145">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a329-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="5a329-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a329-146">OUTPUTS</span></span>

### <span data-ttu-id="5a329-147">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a329-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5a329-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a329-148">NOTES</span></span>

## <span data-ttu-id="5a329-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a329-149">RELATED LINKS</span></span>

[<span data-ttu-id="5a329-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5a329-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="5a329-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5a329-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="5a329-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a329-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
