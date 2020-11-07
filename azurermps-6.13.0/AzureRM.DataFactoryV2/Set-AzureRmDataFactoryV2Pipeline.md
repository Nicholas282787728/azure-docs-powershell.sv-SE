---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: dcdf7cdf9de6de23a3178fe8cbb4ac0f67f43d30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585019"
---
# <span data-ttu-id="718a6-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="718a6-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="718a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="718a6-102">SYNOPSIS</span></span>
<span data-ttu-id="718a6-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="718a6-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="718a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="718a6-104">SYNTAX</span></span>

### <span data-ttu-id="718a6-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="718a6-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="718a6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="718a6-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="718a6-107">DESCRIPTION</span></span>
<span data-ttu-id="718a6-108">Set-AzureRmDataFactoryV2Pipeline-cmdleten skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="718a6-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="718a6-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="718a6-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="718a6-110">Om du anger parametern Force ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="718a6-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="718a6-111">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="718a6-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="718a6-112">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="718a6-112">-- Create linked services.</span></span>
<span data-ttu-id="718a6-113">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="718a6-113">-- Create datasets.</span></span>
<span data-ttu-id="718a6-114">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="718a6-114">-- Create a pipeline.</span></span>
<span data-ttu-id="718a6-115">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="718a6-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="718a6-116">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="718a6-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="718a6-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="718a6-117">EXAMPLES</span></span>

### <span data-ttu-id="718a6-118">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="718a6-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="718a6-119">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="718a6-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="718a6-120">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="718a6-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="718a6-121">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="718a6-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="718a6-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="718a6-122">PARAMETERS</span></span>

### <span data-ttu-id="718a6-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="718a6-123">-DataFactoryName</span></span>
<span data-ttu-id="718a6-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="718a6-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="718a6-125">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="718a6-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="718a6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718a6-126">-DefaultProfile</span></span>
<span data-ttu-id="718a6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="718a6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="718a6-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="718a6-128">-DefinitionFile</span></span>
<span data-ttu-id="718a6-129">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="718a6-129">The JSON file path.</span></span>

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

### <span data-ttu-id="718a6-130">-Force</span><span class="sxs-lookup"><span data-stu-id="718a6-130">-Force</span></span>
<span data-ttu-id="718a6-131">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="718a6-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="718a6-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="718a6-132">-Name</span></span>
<span data-ttu-id="718a6-133">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="718a6-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="718a6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718a6-134">-ResourceGroupName</span></span>
<span data-ttu-id="718a6-135">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="718a6-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="718a6-136">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="718a6-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="718a6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="718a6-137">-ResourceId</span></span>
<span data-ttu-id="718a6-138">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="718a6-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="718a6-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="718a6-139">-Confirm</span></span>
<span data-ttu-id="718a6-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="718a6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="718a6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718a6-141">-WhatIf</span></span>
<span data-ttu-id="718a6-142">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="718a6-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="718a6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718a6-143">CommonParameters</span></span>
<span data-ttu-id="718a6-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718a6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718a6-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718a6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718a6-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="718a6-146">INPUTS</span></span>

### <span data-ttu-id="718a6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="718a6-147">System.String</span></span>

## <span data-ttu-id="718a6-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="718a6-148">OUTPUTS</span></span>

### <span data-ttu-id="718a6-149">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="718a6-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="718a6-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="718a6-150">NOTES</span></span>
<span data-ttu-id="718a6-151">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="718a6-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="718a6-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="718a6-152">RELATED LINKS</span></span>

[<span data-ttu-id="718a6-153">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="718a6-153">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="718a6-154">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="718a6-154">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="718a6-155">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="718a6-155">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()