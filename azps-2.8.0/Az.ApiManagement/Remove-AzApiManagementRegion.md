---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745693"
---
# <span data-ttu-id="c4099-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c4099-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="c4099-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4099-102">SYNOPSIS</span></span>
<span data-ttu-id="c4099-103">Tar bort ett befintligt distributions område från PsApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="c4099-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="c4099-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4099-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4099-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4099-105">DESCRIPTION</span></span>
<span data-ttu-id="c4099-106">Cmdleten **Remove-AzApiManagementRegion** tar bort instansen av typen **Microsoft. Azure. kommandon. ApiManagement. Models. PsApiManagementRegion** från en mängd **AdditionalRegions** som tillhandahålls instansen av typen **Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="c4099-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="c4099-107">Denna cmdlet ändrar inte distribution fristående men uppdaterar instansen av **PsApiManagement** i minnet.</span><span class="sxs-lookup"><span data-stu-id="c4099-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="c4099-108">Om du vill uppdatera en distribution av en API-hantering skickar du den ändrade **PsApiManagementInstance** till **set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="c4099-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="c4099-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4099-109">EXAMPLES</span></span>

### <span data-ttu-id="c4099-110">Exempel 1: ta bort en region från en PsApiManagement-instans</span><span class="sxs-lookup"><span data-stu-id="c4099-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="c4099-111">Det här kommandot tar bort regionen öst från **PsApiManagement** -instansen.</span><span class="sxs-lookup"><span data-stu-id="c4099-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="c4099-112">Exempel 2: ta bort en region från en PsApiManagement-instans med en serie kommandon</span><span class="sxs-lookup"><span data-stu-id="c4099-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="c4099-113">Det här första kommandot får en instans av **PsApiManagement** från resurs gruppen med namnet contoso med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="c4099-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="c4099-114">Kommandot sista tar sedan bort den region som heter östra USA från den instansen och uppdaterar sedan distributionen.</span><span class="sxs-lookup"><span data-stu-id="c4099-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="c4099-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4099-115">PARAMETERS</span></span>

### <span data-ttu-id="c4099-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4099-116">-ApiManagement</span></span>
<span data-ttu-id="c4099-117">Anger den **PsApiManagement** -instans som denna cmdlet tar bort det extra distributions området från.</span><span class="sxs-lookup"><span data-stu-id="c4099-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="c4099-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4099-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="c4099-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4099-119">-Location</span></span>
<span data-ttu-id="c4099-120">Anger platsen för den region som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="c4099-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="c4099-121">Anger platsen för det nya distributions området bland de regioner som stöds för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c4099-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="c4099-122">För att få giltiga platser, Använd cmdleten Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | där {$ _. ResourceTypes [0]. ResourceTypeName-EQ "tjänst"} | Select-Object platser</span><span class="sxs-lookup"><span data-stu-id="c4099-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c4099-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4099-123">CommonParameters</span></span>
<span data-ttu-id="c4099-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4099-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4099-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4099-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4099-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4099-126">INPUTS</span></span>

### <span data-ttu-id="c4099-127">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4099-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="c4099-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c4099-128">System.String</span></span>

## <span data-ttu-id="c4099-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4099-129">OUTPUTS</span></span>

### <span data-ttu-id="c4099-130">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4099-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c4099-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4099-131">NOTES</span></span>

## <span data-ttu-id="c4099-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4099-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4099-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c4099-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="c4099-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c4099-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


