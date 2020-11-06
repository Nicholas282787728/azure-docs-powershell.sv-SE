---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585471"
---
# <span data-ttu-id="7bc81-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="7bc81-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="7bc81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bc81-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc81-103">Skapar en ny webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="7bc81-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bc81-104">SYNTAX</span></span>

### <span data-ttu-id="7bc81-105">Skapa en ny Azure ML-webtjänst från en JSON Definiton-fil.</span><span class="sxs-lookup"><span data-stu-id="7bc81-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bc81-106">Skapa en ny Azure ML-webtjänst från en webb tjänst instans definition.</span><span class="sxs-lookup"><span data-stu-id="7bc81-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bc81-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bc81-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc81-108">Skapar en Azure Machine Learning-webbtjänst i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7bc81-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="7bc81-109">Om en webb tjänst med samma namn finns i resurs gruppen fungerar samtalet som en uppdaterings åtgärd och den befintliga webb tjänsten skrivs över.</span><span class="sxs-lookup"><span data-stu-id="7bc81-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="7bc81-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bc81-110">EXAMPLES</span></span>

### <span data-ttu-id="7bc81-111">--------------------------Exempel 1: skapa en ny tjänst från en JSON-baserad definition--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc81-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="7bc81-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bc81-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="7bc81-113">Skapar en ny Azure Machine Learning-webbtjänst med namnet "mywebservicename" i gruppen "myresourcegroup" och det centrala amerikanska området, baserat på definitionen i den refererade JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="7bc81-114">--------------------------Exempel 2: skapa en ny tjänst från en objekt instans--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc81-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="7bc81-115">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bc81-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="7bc81-116">Du kan få en instans av en webb tjänst objekt att anpassa innan du publicerar den som en resurs genom att använda Import-AzureRmMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc81-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="7bc81-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bc81-117">PARAMETERS</span></span>

### <span data-ttu-id="7bc81-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7bc81-118">-DefinitionFile</span></span>
<span data-ttu-id="7bc81-119">Specifes sökvägen till filen som innehåller JSON-formatet för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7bc81-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="7bc81-120">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="7bc81-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc81-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7bc81-121">-Force</span></span>
<span data-ttu-id="7bc81-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7bc81-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7bc81-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="7bc81-123">-Location</span></span>
<span data-ttu-id="7bc81-124">Regionen för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7bc81-124">The region of the web service.</span></span>
<span data-ttu-id="7bc81-125">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="7bc81-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="7bc81-126">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="7bc81-127">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="7bc81-128">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="7bc81-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="7bc81-129">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzureRmResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc81-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="7bc81-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bc81-130">-Name</span></span>
<span data-ttu-id="7bc81-131">Namnet på webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7bc81-131">The name for the web service.</span></span>
<span data-ttu-id="7bc81-132">Namnet måste vara unikt i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="7bc81-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="7bc81-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="7bc81-134">Definitionen för den nya webb tjänsten som innehåller alla egenskaper som utgör tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7bc81-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="7bc81-135">Den här parametern är obligatorisk och representerar en instans av klassen Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="7bc81-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="7bc81-136">Du hittar den senaste specifikationen för webb tjänst definitionen i Swagger-specifikationen under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="7bc81-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc81-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc81-137">-ResourceGroupName</span></span>
<span data-ttu-id="7bc81-138">Resurs gruppen där webb tjänsten ska placeras.</span><span class="sxs-lookup"><span data-stu-id="7bc81-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="7bc81-139">Ange ett Azure Data Center-område, till exempel "västra USA" eller "Sydostasien".</span><span class="sxs-lookup"><span data-stu-id="7bc81-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="7bc81-140">Du kan använda en webb tjänst i vilken region som helst som stöder resurser av den typen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="7bc81-141">Webb tjänsten måste inte vara i samma region som din Azure-prenumeration eller samma region som resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7bc81-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="7bc81-142">Resurs grupper kan innehålla webb tjänster från olika regioner.</span><span class="sxs-lookup"><span data-stu-id="7bc81-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="7bc81-143">För att avgöra vilka regioner som stöder varje resurs typ använder du Get-AzureRmResourceProvider med ProviderNamespace parameter-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc81-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="7bc81-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bc81-144">-Confirm</span></span>
<span data-ttu-id="7bc81-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bc81-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc81-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc81-146">-WhatIf</span></span>
<span data-ttu-id="7bc81-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bc81-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc81-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bc81-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc81-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc81-149">-DefaultProfile</span></span>
<span data-ttu-id="7bc81-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc81-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc81-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc81-151">CommonParameters</span></span>
<span data-ttu-id="7bc81-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc81-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc81-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc81-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc81-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bc81-154">INPUTS</span></span>

### <span data-ttu-id="7bc81-155">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="7bc81-155">WebService</span></span>
<span data-ttu-id="7bc81-156">Parametern ' NewWebServiceDefinition ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="7bc81-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="7bc81-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bc81-157">OUTPUTS</span></span>

### <span data-ttu-id="7bc81-158">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="7bc81-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="7bc81-159">En sammanfattning av Azure Machine Learning web service.</span><span class="sxs-lookup"><span data-stu-id="7bc81-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="7bc81-160">Liknar beskrivningen som returneras när du anropar Get-AzureRmMlWebService cmdlet på en befintlig webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="7bc81-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="7bc81-161">Den här beskrivningen innehåller inte känsliga egenskaper som lagrings kontots autentiseringsuppgifter och tjänstens åtkomst nycklar.</span><span class="sxs-lookup"><span data-stu-id="7bc81-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="7bc81-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bc81-162">NOTES</span></span>
<span data-ttu-id="7bc81-163">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="7bc81-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7bc81-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bc81-164">RELATED LINKS</span></span>

