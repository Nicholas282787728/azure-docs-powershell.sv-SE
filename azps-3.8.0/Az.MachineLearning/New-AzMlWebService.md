---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091958"
---
# <span data-ttu-id="a4f20-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="a4f20-101">New-AzMlWebService</span></span>

## <span data-ttu-id="a4f20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4f20-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f20-103">Skapar en ny webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="a4f20-103">Creates a new web service.</span></span>

## <span data-ttu-id="a4f20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4f20-104">SYNTAX</span></span>

### <span data-ttu-id="a4f20-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="a4f20-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f20-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="a4f20-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f20-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4f20-107">DESCRIPTION</span></span>
<span data-ttu-id="a4f20-108">Skapar en Azure Machine Learning-webbtjänst i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4f20-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="a4f20-109">Om en webb tjänst med samma namn finns i resurs gruppen fungerar samtalet som en uppdaterings åtgärd och den befintliga webb tjänsten skrivs över.</span><span class="sxs-lookup"><span data-stu-id="a4f20-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="a4f20-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4f20-110">EXAMPLES</span></span>

### <span data-ttu-id="a4f20-111">Exempel 1: skapa en ny tjänst från en JSON-filbaserad definition</span><span class="sxs-lookup"><span data-stu-id="a4f20-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="a4f20-112">Skapar en ny Azure Machine Learning-webbtjänst med namnet "mywebservicename" i gruppen "myresourcegroup" och det centrala amerikanska området, baserat på definitionen i den refererade JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="a4f20-113">Exempel 2: skapa en ny tjänst från en objekt instans</span><span class="sxs-lookup"><span data-stu-id="a4f20-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="a4f20-114">Du kan få en instans av en webb tjänst objekt att anpassa innan du publicerar den som en resurs genom att använda Import-AzMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f20-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="a4f20-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4f20-115">PARAMETERS</span></span>

### <span data-ttu-id="a4f20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f20-116">-DefaultProfile</span></span>
<span data-ttu-id="a4f20-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4f20-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f20-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a4f20-118">-DefinitionFile</span></span>
<span data-ttu-id="a4f20-119">Anger sökvägen till filen som innehåller JSON-formatet för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a4f20-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="a4f20-120">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="a4f20-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f20-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a4f20-121">-Force</span></span>
<span data-ttu-id="a4f20-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4f20-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f20-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4f20-123">-Location</span></span>
<span data-ttu-id="a4f20-124">Regionen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a4f20-124">The region of the web service.</span></span>
<span data-ttu-id="a4f20-125">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="a4f20-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="a4f20-126">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="a4f20-127">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="a4f20-128">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="a4f20-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="a4f20-129">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f20-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="a4f20-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4f20-130">-Name</span></span>
<span data-ttu-id="a4f20-131">Namnet på webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a4f20-131">The name for the web service.</span></span>
<span data-ttu-id="a4f20-132">Namnet måste vara unikt i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="a4f20-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="a4f20-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="a4f20-134">Definitionen för den nya webb tjänsten som innehåller alla egenskaper som utgör tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a4f20-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="a4f20-135">Den här parametern är obligatorisk och representerar en instans av klassen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="a4f20-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="a4f20-136">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="a4f20-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f20-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f20-137">-ResourceGroupName</span></span>
<span data-ttu-id="a4f20-138">Resurs gruppen där webb tjänsten ska placeras.</span><span class="sxs-lookup"><span data-stu-id="a4f20-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="a4f20-139">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="a4f20-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="a4f20-140">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="a4f20-141">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4f20-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="a4f20-142">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="a4f20-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="a4f20-143">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f20-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="a4f20-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4f20-144">-Confirm</span></span>
<span data-ttu-id="a4f20-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4f20-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f20-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f20-146">-WhatIf</span></span>
<span data-ttu-id="a4f20-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4f20-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f20-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4f20-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f20-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f20-149">CommonParameters</span></span>
<span data-ttu-id="a4f20-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f20-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f20-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f20-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f20-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4f20-152">INPUTS</span></span>

### <span data-ttu-id="a4f20-153">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a4f20-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a4f20-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4f20-154">OUTPUTS</span></span>

### <span data-ttu-id="a4f20-155">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a4f20-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a4f20-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4f20-156">NOTES</span></span>
<span data-ttu-id="a4f20-157">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="a4f20-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a4f20-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4f20-158">RELATED LINKS</span></span>
