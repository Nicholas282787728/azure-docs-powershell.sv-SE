---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fff6145adaa909bcadde90f36802072b812ba0ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091884"
---
# <span data-ttu-id="9c202-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9c202-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="9c202-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c202-102">SYNOPSIS</span></span>
<span data-ttu-id="9c202-103">Uppdaterar det befintliga distributions området i PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="9c202-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="9c202-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c202-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c202-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c202-105">DESCRIPTION</span></span>
<span data-ttu-id="9c202-106">Cmdleten **Update-AzApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion** i en samling **AdditionalRegions** -objekt av en angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="9c202-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9c202-107">Denna cmdlet distribuerar inte något men uppdaterar inte en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="9c202-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9c202-108">Om du vill uppdatera en distribution av en API-hantering använder du den ändrade **PsApiManagementInstance** till cmdleten Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9c202-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="9c202-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c202-109">EXAMPLES</span></span>

### <span data-ttu-id="9c202-110">Exempel 1: ökar kapaciteten för ytterligare områden i en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="9c202-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="9c202-111">Det här kommandot får API Management Premium SKU-tjänsten med regioner i södra centrala USA och norra centrala USA.</span><span class="sxs-lookup"><span data-stu-id="9c202-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="9c202-112">Därefter ökar kapaciteten för Nord Central USA-regionen till 2 med hjälp av **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="9c202-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="9c202-113">Nästa cmdlet **set-AzApiManagement** tillämpar konfigurations ändringen för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9c202-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="9c202-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c202-114">PARAMETERS</span></span>

### <span data-ttu-id="9c202-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c202-115">-ApiManagement</span></span>
<span data-ttu-id="9c202-116">Anger den **PsApiManagement** -instans som du vill uppdatera ett befintligt distributions område i.</span><span class="sxs-lookup"><span data-stu-id="9c202-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="9c202-117">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="9c202-117">-Capacity</span></span>
<span data-ttu-id="9c202-118">Anger det nya värdet för SKU-kapacitet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="9c202-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="9c202-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c202-119">-DefaultProfile</span></span>
<span data-ttu-id="9c202-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c202-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c202-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c202-121">-Location</span></span>
<span data-ttu-id="9c202-122">Anger platsen för det distributions område som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="9c202-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="9c202-123">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9c202-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="9c202-124">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="9c202-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="9c202-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="9c202-125">-Sku</span></span>
<span data-ttu-id="9c202-126">Anger det nya nivå svärdet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="9c202-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="9c202-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9c202-127">Valid values are:</span></span>
- <span data-ttu-id="9c202-128">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="9c202-128">Developer</span></span>
- <span data-ttu-id="9c202-129">Standar</span><span class="sxs-lookup"><span data-stu-id="9c202-129">Standard</span></span>
- <span data-ttu-id="9c202-130">Beta</span><span class="sxs-lookup"><span data-stu-id="9c202-130">Premium</span></span>

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

### <span data-ttu-id="9c202-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c202-131">-VirtualNetwork</span></span>
<span data-ttu-id="9c202-132">Anger en virtuell nätverks konfiguration för distributions området.</span><span class="sxs-lookup"><span data-stu-id="9c202-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="9c202-133">Om du överför $null tas nätverkets konfiguration för området bort.</span><span class="sxs-lookup"><span data-stu-id="9c202-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="9c202-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c202-134">CommonParameters</span></span>
<span data-ttu-id="9c202-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c202-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c202-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c202-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c202-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c202-137">INPUTS</span></span>

### <span data-ttu-id="9c202-138">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c202-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="9c202-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c202-139">System.String</span></span>

### <span data-ttu-id="9c202-140">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="9c202-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="9c202-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9c202-141">System.Int32</span></span>

### <span data-ttu-id="9c202-142">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c202-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="9c202-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c202-143">OUTPUTS</span></span>

### <span data-ttu-id="9c202-144">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c202-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9c202-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c202-145">NOTES</span></span>

## <span data-ttu-id="9c202-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c202-146">RELATED LINKS</span></span>

[<span data-ttu-id="9c202-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9c202-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="9c202-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9c202-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="9c202-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c202-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
