---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757271"
---
# <span data-ttu-id="367dc-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="367dc-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="367dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="367dc-102">SYNOPSIS</span></span>
<span data-ttu-id="367dc-103">Uppdaterar det befintliga distributions området i PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="367dc-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="367dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="367dc-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="367dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="367dc-105">DESCRIPTION</span></span>
<span data-ttu-id="367dc-106">Cmdleten **Update-AzureRmApiManagementRegion** uppdaterar en befintlig instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementRegion** i en samling **AdditionalRegions** -objekt av en angiven instans av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="367dc-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="367dc-107">Denna cmdlet distribuerar inte något men uppdaterar inte en instans av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="367dc-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="367dc-108">Om du vill uppdatera en distribution av en API-hantering använder du den ändrade **PsApiManagementInstance** till cmdleten Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="367dc-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="367dc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="367dc-109">EXAMPLES</span></span>

## <span data-ttu-id="367dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="367dc-110">PARAMETERS</span></span>

### <span data-ttu-id="367dc-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="367dc-111">-ApiManagement</span></span>
<span data-ttu-id="367dc-112">Anger den **PsApiManagement** -instans som du vill uppdatera ett befintligt distributions område i.</span><span class="sxs-lookup"><span data-stu-id="367dc-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="367dc-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="367dc-113">-Capacity</span></span>
<span data-ttu-id="367dc-114">Anger det nya värdet för SKU-kapacitet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="367dc-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367dc-115">-DefaultProfile</span></span>
<span data-ttu-id="367dc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="367dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="367dc-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="367dc-117">-Location</span></span>
<span data-ttu-id="367dc-118">Anger platsen för det distributions område som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="367dc-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="367dc-119">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="367dc-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="367dc-120">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="367dc-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367dc-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="367dc-121">-Sku</span></span>
<span data-ttu-id="367dc-122">Anger det nya nivå svärdet för distributions området.</span><span class="sxs-lookup"><span data-stu-id="367dc-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="367dc-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="367dc-123">Valid values are:</span></span>

- <span data-ttu-id="367dc-124">Utvecklar</span><span class="sxs-lookup"><span data-stu-id="367dc-124">Developer</span></span>
- <span data-ttu-id="367dc-125">Standar</span><span class="sxs-lookup"><span data-stu-id="367dc-125">Standard</span></span>
- <span data-ttu-id="367dc-126">Beta</span><span class="sxs-lookup"><span data-stu-id="367dc-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367dc-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="367dc-127">-VirtualNetwork</span></span>
<span data-ttu-id="367dc-128">Anger en virtuell nätverks konfiguration för distributions området.</span><span class="sxs-lookup"><span data-stu-id="367dc-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="367dc-129">Om du överför $null tas nätverkets konfiguration för området bort.</span><span class="sxs-lookup"><span data-stu-id="367dc-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367dc-130">CommonParameters</span></span>
<span data-ttu-id="367dc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367dc-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367dc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367dc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="367dc-133">INPUTS</span></span>

### <span data-ttu-id="367dc-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="367dc-134">PsApiManagement</span></span>
<span data-ttu-id="367dc-135">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="367dc-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="367dc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="367dc-136">OUTPUTS</span></span>

### <span data-ttu-id="367dc-137">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="367dc-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="367dc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="367dc-138">NOTES</span></span>

## <span data-ttu-id="367dc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="367dc-139">RELATED LINKS</span></span>

[<span data-ttu-id="367dc-140">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="367dc-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="367dc-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="367dc-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="367dc-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="367dc-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
