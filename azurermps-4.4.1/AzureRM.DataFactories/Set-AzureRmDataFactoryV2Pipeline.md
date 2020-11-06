---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 510f0f5b943a1a0abab1bc97ac5e70fa6f450898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574981"
---
# <span data-ttu-id="e22c8-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e22c8-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e22c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e22c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e22c8-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e22c8-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e22c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e22c8-104">SYNTAX</span></span>

### <span data-ttu-id="e22c8-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e22c8-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e22c8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e22c8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22c8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e22c8-107">DESCRIPTION</span></span>
<span data-ttu-id="e22c8-108">Set-AzureRmDataFactoryV2Pipeline-cmdleten skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e22c8-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="e22c8-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="e22c8-110">Om du anger parametern Force ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e22c8-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="e22c8-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="e22c8-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="e22c8-112">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="e22c8-113">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="e22c8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e22c8-114">EXAMPLES</span></span>

### <span data-ttu-id="e22c8-115">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="e22c8-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="e22c8-116">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="e22c8-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="e22c8-117">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="e22c8-118">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="e22c8-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="e22c8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e22c8-119">PARAMETERS</span></span>

### <span data-ttu-id="e22c8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e22c8-120">-Confirm</span></span>
<span data-ttu-id="e22c8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e22c8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22c8-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e22c8-122">-DataFactoryName</span></span>
<span data-ttu-id="e22c8-123">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e22c8-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e22c8-124">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e22c8-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22c8-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e22c8-125">-DefinitionFile</span></span>
<span data-ttu-id="e22c8-126">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-126">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22c8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e22c8-127">-Force</span></span>
<span data-ttu-id="e22c8-128">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e22c8-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e22c8-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="e22c8-129">-Name</span></span>
<span data-ttu-id="e22c8-130">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e22c8-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22c8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22c8-131">-ResourceGroupName</span></span>
<span data-ttu-id="e22c8-132">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e22c8-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e22c8-133">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e22c8-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22c8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e22c8-134">-ResourceId</span></span>
<span data-ttu-id="e22c8-135">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e22c8-135">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22c8-136">-WhatIf</span></span>
<span data-ttu-id="e22c8-137">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e22c8-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e22c8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22c8-138">-DefaultProfile</span></span>
<span data-ttu-id="e22c8-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e22c8-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e22c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22c8-140">CommonParameters</span></span>
<span data-ttu-id="e22c8-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22c8-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22c8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22c8-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e22c8-143">INPUTS</span></span>

### <span data-ttu-id="e22c8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e22c8-144">System.String</span></span>

## <span data-ttu-id="e22c8-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e22c8-145">OUTPUTS</span></span>

### <span data-ttu-id="e22c8-146">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e22c8-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e22c8-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e22c8-147">NOTES</span></span>
<span data-ttu-id="e22c8-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e22c8-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e22c8-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e22c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="e22c8-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e22c8-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e22c8-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e22c8-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e22c8-152">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e22c8-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
