---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524150"
---
# <span data-ttu-id="84e6e-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="84e6e-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="84e6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="84e6e-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="84e6e-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="84e6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84e6e-104">SYNTAX</span></span>

### <span data-ttu-id="84e6e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="84e6e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84e6e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84e6e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e6e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84e6e-107">DESCRIPTION</span></span>
<span data-ttu-id="84e6e-108">Set-AzDataFactoryV2Pipeline-cmdleten skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="84e6e-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="84e6e-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="84e6e-110">Om du anger parametern Force ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="84e6e-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="84e6e-111">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="84e6e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="84e6e-112">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="84e6e-112">-- Create linked services.</span></span>
<span data-ttu-id="84e6e-113">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="84e6e-113">-- Create datasets.</span></span>
<span data-ttu-id="84e6e-114">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="84e6e-114">-- Create a pipeline.</span></span>
<span data-ttu-id="84e6e-115">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="84e6e-116">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="84e6e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84e6e-117">EXAMPLES</span></span>

### <span data-ttu-id="84e6e-118">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="84e6e-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="84e6e-119">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="84e6e-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="84e6e-120">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="84e6e-121">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="84e6e-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="84e6e-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84e6e-122">PARAMETERS</span></span>

### <span data-ttu-id="84e6e-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84e6e-123">-DataFactoryName</span></span>
<span data-ttu-id="84e6e-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="84e6e-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="84e6e-125">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84e6e-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84e6e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e6e-126">-DefaultProfile</span></span>
<span data-ttu-id="84e6e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84e6e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e6e-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="84e6e-128">-DefinitionFile</span></span>
<span data-ttu-id="84e6e-129">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-129">The JSON file path.</span></span>

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

### <span data-ttu-id="84e6e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="84e6e-130">-Force</span></span>
<span data-ttu-id="84e6e-131">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="84e6e-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="84e6e-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="84e6e-132">-Name</span></span>
<span data-ttu-id="84e6e-133">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="84e6e-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="84e6e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e6e-134">-ResourceGroupName</span></span>
<span data-ttu-id="84e6e-135">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="84e6e-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84e6e-136">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84e6e-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84e6e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84e6e-137">-ResourceId</span></span>
<span data-ttu-id="84e6e-138">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="84e6e-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84e6e-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84e6e-139">-Confirm</span></span>
<span data-ttu-id="84e6e-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84e6e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e6e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e6e-141">-WhatIf</span></span>
<span data-ttu-id="84e6e-142">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84e6e-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="84e6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e6e-143">CommonParameters</span></span>
<span data-ttu-id="84e6e-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e6e-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e6e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e6e-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84e6e-146">INPUTS</span></span>

### <span data-ttu-id="84e6e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="84e6e-147">System.String</span></span>

## <span data-ttu-id="84e6e-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84e6e-148">OUTPUTS</span></span>

### <span data-ttu-id="84e6e-149">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="84e6e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="84e6e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84e6e-150">NOTES</span></span>
<span data-ttu-id="84e6e-151">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="84e6e-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84e6e-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84e6e-152">RELATED LINKS</span></span>

[<span data-ttu-id="84e6e-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="84e6e-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="84e6e-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="84e6e-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="84e6e-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="84e6e-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
