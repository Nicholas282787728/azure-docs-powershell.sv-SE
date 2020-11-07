---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756738"
---
# <span data-ttu-id="0f112-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0f112-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="0f112-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f112-102">SYNOPSIS</span></span>
<span data-ttu-id="0f112-103">Tar bort ett befintligt distributions område från PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="0f112-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f112-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f112-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f112-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f112-105">DESCRIPTION</span></span>
<span data-ttu-id="0f112-106">Cmdleten **Remove-AzureRmApiManagementRegion** tar bort instansen av typen **Microsoft. Azure. kommandon. ApiManagement. Models. PsApiManagementRegion** från en mängd **AdditionalRegions** som tillhandahålls instansen av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="0f112-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0f112-107">Denna cmdlet ändrar inte distribution fristående men uppdaterar instansen av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="0f112-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0f112-108">Om du vill uppdatera en distribution av en API-hantering skickar du den ändrade **PsApiManagementInstance** till **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="0f112-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="0f112-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f112-109">EXAMPLES</span></span>

### <span data-ttu-id="0f112-110">Exempel 1: ta bort en region från en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="0f112-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="0f112-111">Det här kommandot tar bort regionen öst från **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="0f112-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="0f112-112">Exempel 2: ta bort en region från en PsApiManagement-instans med en serie kommandon</span><span class="sxs-lookup"><span data-stu-id="0f112-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="0f112-113">Det här första kommandot får en instans av **PsApiManagement** från resurs gruppen med namnet contoso med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="0f112-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="0f112-114">Kommandot sista tar sedan bort den region som heter östra USA från den instansen och uppdaterar sedan distributionen.</span><span class="sxs-lookup"><span data-stu-id="0f112-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="0f112-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f112-115">PARAMETERS</span></span>

### <span data-ttu-id="0f112-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0f112-116">-ApiManagement</span></span>
<span data-ttu-id="0f112-117">Anger den **PsApiManagement** -instans som denna cmdlet tar bort det extra distributions området från.</span><span class="sxs-lookup"><span data-stu-id="0f112-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="0f112-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f112-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="0f112-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0f112-119">-Location</span></span>
<span data-ttu-id="0f112-120">Anger platsen för den region som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0f112-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="0f112-121">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0f112-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="0f112-122">För att få giltiga platser, Använd cmdleten Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="0f112-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="0f112-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f112-123">CommonParameters</span></span>
<span data-ttu-id="0f112-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f112-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f112-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f112-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f112-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f112-126">INPUTS</span></span>

### <span data-ttu-id="0f112-127">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0f112-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="0f112-128">Parametrar: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f112-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="0f112-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0f112-129">System.String</span></span>

## <span data-ttu-id="0f112-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f112-130">OUTPUTS</span></span>

### <span data-ttu-id="0f112-131">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0f112-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0f112-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f112-132">NOTES</span></span>

## <span data-ttu-id="0f112-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f112-133">RELATED LINKS</span></span>

[<span data-ttu-id="0f112-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0f112-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="0f112-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0f112-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


