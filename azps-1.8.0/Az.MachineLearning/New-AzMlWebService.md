---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: e6ac8c2a47f7a8d11eb4f82d46be2047fd5ff47d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915869"
---
# <span data-ttu-id="9ee3b-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="9ee3b-101">New-AzMlWebService</span></span>

## <span data-ttu-id="9ee3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ee3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee3b-103">Skapar en ny webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-103">Creates a new web service.</span></span>

## <span data-ttu-id="9ee3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ee3b-104">SYNTAX</span></span>

### <span data-ttu-id="9ee3b-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="9ee3b-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee3b-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="9ee3b-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ee3b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ee3b-107">DESCRIPTION</span></span>
<span data-ttu-id="9ee3b-108">Skapar en Azure Machine Learning-webbtjänst i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="9ee3b-109">Om en webb tjänst med samma namn finns i resurs gruppen fungerar samtalet som en uppdaterings åtgärd och den befintliga webb tjänsten skrivs över.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="9ee3b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ee3b-110">EXAMPLES</span></span>

### <span data-ttu-id="9ee3b-111">Exempel 1: skapa en ny tjänst från en JSON-filbaserad definition</span><span class="sxs-lookup"><span data-stu-id="9ee3b-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="9ee3b-112">Skapar en ny Azure Machine Learning-webbtjänst med namnet "mywebservicename" i gruppen "myresourcegroup" och det centrala amerikanska området, baserat på definitionen i den refererade JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="9ee3b-113">Exempel 2: skapa en ny tjänst från en objekt instans</span><span class="sxs-lookup"><span data-stu-id="9ee3b-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="9ee3b-114">Du kan få en instans av en webb tjänst objekt att anpassa innan du publicerar den som en resurs genom att använda Import-AzMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="9ee3b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ee3b-115">PARAMETERS</span></span>

### <span data-ttu-id="9ee3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee3b-116">-DefaultProfile</span></span>
<span data-ttu-id="9ee3b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9ee3b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ee3b-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9ee3b-118">-DefinitionFile</span></span>
<span data-ttu-id="9ee3b-119">Specifes sökvägen till filen som innehåller JSON-formatet för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="9ee3b-120">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="9ee3b-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="9ee3b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9ee3b-121">-Force</span></span>
<span data-ttu-id="9ee3b-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9ee3b-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="9ee3b-123">-Location</span></span>
<span data-ttu-id="9ee3b-124">Regionen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-124">The region of the web service.</span></span>
<span data-ttu-id="9ee3b-125">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="9ee3b-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="9ee3b-126">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="9ee3b-127">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="9ee3b-128">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="9ee3b-129">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="9ee3b-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ee3b-130">-Name</span></span>
<span data-ttu-id="9ee3b-131">Namnet på webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-131">The name for the web service.</span></span>
<span data-ttu-id="9ee3b-132">Namnet måste vara unikt i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="9ee3b-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="9ee3b-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="9ee3b-134">Definitionen för den nya webb tjänsten som innehåller alla egenskaper som utgör tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="9ee3b-135">Den här parametern är obligatorisk och representerar en instans av klassen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="9ee3b-136">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="9ee3b-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="9ee3b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee3b-137">-ResourceGroupName</span></span>
<span data-ttu-id="9ee3b-138">Resurs gruppen där webb tjänsten ska placeras.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="9ee3b-139">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="9ee3b-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="9ee3b-140">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="9ee3b-141">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="9ee3b-142">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="9ee3b-143">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="9ee3b-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ee3b-144">-Confirm</span></span>
<span data-ttu-id="9ee3b-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee3b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee3b-146">-WhatIf</span></span>
<span data-ttu-id="9ee3b-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee3b-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee3b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee3b-149">CommonParameters</span></span>
<span data-ttu-id="9ee3b-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee3b-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ee3b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee3b-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ee3b-152">INPUTS</span></span>

### <span data-ttu-id="9ee3b-153">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="9ee3b-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9ee3b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ee3b-154">OUTPUTS</span></span>

### <span data-ttu-id="9ee3b-155">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="9ee3b-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9ee3b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ee3b-156">NOTES</span></span>
<span data-ttu-id="9ee3b-157">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="9ee3b-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9ee3b-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ee3b-158">RELATED LINKS</span></span>