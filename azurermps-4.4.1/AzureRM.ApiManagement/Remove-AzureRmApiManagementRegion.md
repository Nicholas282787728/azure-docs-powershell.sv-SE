---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573757"
---
# <span data-ttu-id="98e08-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="98e08-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="98e08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98e08-102">SYNOPSIS</span></span>
<span data-ttu-id="98e08-103">Tar bort ett befintligt distributions område från PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="98e08-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98e08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98e08-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98e08-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98e08-105">DESCRIPTION</span></span>
<span data-ttu-id="98e08-106">Cmdleten **Remove-AzureRmApiManagementRegion** tar bort instansen av typen **Microsoft. Azure. kommandon. ApiManagement. Models. PsApiManagementRegion** från en mängd **AdditionalRegions** som tillhandahålls instansen av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="98e08-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="98e08-107">Denna cmdlet ändrar inte distribution fristående men uppdaterar instansen av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="98e08-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="98e08-108">Om du vill uppdatera en distribution av en API-hantering skickar du den ändrade **PsApiManagementInstance** till **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="98e08-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="98e08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98e08-109">EXAMPLES</span></span>

### <span data-ttu-id="98e08-110">Exempel 1: ta bort en region från en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="98e08-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="98e08-111">Det här kommandot tar bort regionen öst från **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="98e08-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="98e08-112">Exempel 2: ta bort en region från en PsApiManagement-instans med en serie kommandon</span><span class="sxs-lookup"><span data-stu-id="98e08-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="98e08-113">Det här första kommandot får en instans av **PsApiManagement** från resurs gruppen med namnet contoso med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="98e08-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="98e08-114">Kommandot sista tar sedan bort den region som heter östra USA från den instansen och uppdaterar sedan distributionen.</span><span class="sxs-lookup"><span data-stu-id="98e08-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="98e08-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98e08-115">PARAMETERS</span></span>

### <span data-ttu-id="98e08-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98e08-116">-ApiManagement</span></span>
<span data-ttu-id="98e08-117">Anger den **PsApiManagement** -instans som denna cmdlet tar bort det extra distributions området från.</span><span class="sxs-lookup"><span data-stu-id="98e08-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="98e08-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="98e08-118">-Location</span></span>
<span data-ttu-id="98e08-119">Anger platsen för den region som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="98e08-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="98e08-120">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="98e08-120">Valid values are:</span></span> 

- <span data-ttu-id="98e08-121">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="98e08-121">North Central US</span></span>
- <span data-ttu-id="98e08-122">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="98e08-122">South Central US</span></span>
- <span data-ttu-id="98e08-123">Central</span><span class="sxs-lookup"><span data-stu-id="98e08-123">Central US</span></span>
- <span data-ttu-id="98e08-124">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="98e08-124">West Europe</span></span>
- <span data-ttu-id="98e08-125">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="98e08-125">North Europe</span></span>
- <span data-ttu-id="98e08-126">Västra USA</span><span class="sxs-lookup"><span data-stu-id="98e08-126">West US</span></span>
- <span data-ttu-id="98e08-127">Östra USA</span><span class="sxs-lookup"><span data-stu-id="98e08-127">East US</span></span>
- <span data-ttu-id="98e08-128">Östra USA 2</span><span class="sxs-lookup"><span data-stu-id="98e08-128">East US 2</span></span>
- <span data-ttu-id="98e08-129">Östra Japan</span><span class="sxs-lookup"><span data-stu-id="98e08-129">Japan East</span></span>
- <span data-ttu-id="98e08-130">Västra Japan</span><span class="sxs-lookup"><span data-stu-id="98e08-130">Japan West</span></span>
- <span data-ttu-id="98e08-131">Brasilien, Syd</span><span class="sxs-lookup"><span data-stu-id="98e08-131">Brazil South</span></span>
- <span data-ttu-id="98e08-132">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="98e08-132">Southeast Asia</span></span>
- <span data-ttu-id="98e08-133">Östasien</span><span class="sxs-lookup"><span data-stu-id="98e08-133">East Asia</span></span>
- <span data-ttu-id="98e08-134">Östra Australien</span><span class="sxs-lookup"><span data-stu-id="98e08-134">Australia East</span></span>
- <span data-ttu-id="98e08-135">Australien, sydöst</span><span class="sxs-lookup"><span data-stu-id="98e08-135">Australia Southeast</span></span>

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

### <span data-ttu-id="98e08-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e08-136">-DefaultProfile</span></span>
<span data-ttu-id="98e08-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98e08-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98e08-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e08-138">CommonParameters</span></span>
<span data-ttu-id="98e08-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e08-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e08-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98e08-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e08-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98e08-141">INPUTS</span></span>

### <span data-ttu-id="98e08-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="98e08-142">PsApiManagement</span></span>
<span data-ttu-id="98e08-143">Parametern ' ApiManagement ' godkänner värdet av typen ' PsApiManagement ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="98e08-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="98e08-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98e08-144">OUTPUTS</span></span>

### <span data-ttu-id="98e08-145">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="98e08-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="98e08-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98e08-146">NOTES</span></span>

## <span data-ttu-id="98e08-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98e08-147">RELATED LINKS</span></span>

[<span data-ttu-id="98e08-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="98e08-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="98e08-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="98e08-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


