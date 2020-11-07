---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2a936b9a75e9fc1053e2202950a6a6b4c49bd3a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758416"
---
# <span data-ttu-id="82c10-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82c10-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="82c10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82c10-102">SYNOPSIS</span></span>
<span data-ttu-id="82c10-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="82c10-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82c10-104">SYNTAX</span></span>

### <span data-ttu-id="82c10-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="82c10-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="82c10-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82c10-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="82c10-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82c10-107">DESCRIPTION</span></span>
<span data-ttu-id="82c10-108">Set-AzureRmDataFactoryV2Pipeline-cmdleten skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="82c10-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="82c10-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="82c10-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="82c10-110">Om du anger parametern Force ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="82c10-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="82c10-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="82c10-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="82c10-112">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="82c10-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="82c10-113">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="82c10-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="82c10-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82c10-114">EXAMPLES</span></span>

### <span data-ttu-id="82c10-115">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="82c10-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="82c10-116">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="82c10-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="82c10-117">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="82c10-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="82c10-118">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="82c10-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="82c10-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82c10-119">PARAMETERS</span></span>

### <span data-ttu-id="82c10-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82c10-120">-Confirm</span></span>
<span data-ttu-id="82c10-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82c10-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82c10-122">-DataFactoryName</span></span>
<span data-ttu-id="82c10-123">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="82c10-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="82c10-124">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="82c10-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="82c10-125">-DefinitionFile</span></span>
<span data-ttu-id="82c10-126">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="82c10-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-127">-Force</span><span class="sxs-lookup"><span data-stu-id="82c10-127">-Force</span></span>
<span data-ttu-id="82c10-128">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="82c10-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="82c10-129">-Name</span></span>
<span data-ttu-id="82c10-130">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="82c10-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c10-131">-ResourceGroupName</span></span>
<span data-ttu-id="82c10-132">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="82c10-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="82c10-133">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="82c10-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82c10-134">-ResourceId</span></span>
<span data-ttu-id="82c10-135">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="82c10-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c10-136">-WhatIf</span></span>
<span data-ttu-id="82c10-137">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82c10-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="82c10-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82c10-138">INPUTS</span></span>

### <span data-ttu-id="82c10-139">System. String</span><span class="sxs-lookup"><span data-stu-id="82c10-139">System.String</span></span>


## <span data-ttu-id="82c10-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82c10-140">OUTPUTS</span></span>

### <span data-ttu-id="82c10-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="82c10-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="82c10-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82c10-142">NOTES</span></span>
<span data-ttu-id="82c10-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="82c10-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="82c10-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82c10-144">RELATED LINKS</span></span>
[<span data-ttu-id="82c10-145">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82c10-145">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="82c10-146">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82c10-146">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="82c10-147">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="82c10-147">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
