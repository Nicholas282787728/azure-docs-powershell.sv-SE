---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320940"
---
# <span data-ttu-id="f264c-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="f264c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f264c-102">SYNOPSIS</span></span>
<span data-ttu-id="f264c-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="f264c-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="f264c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f264c-104">SYNTAX</span></span>

### <span data-ttu-id="f264c-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="f264c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f264c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f264c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f264c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f264c-107">DESCRIPTION</span></span>
<span data-ttu-id="f264c-108">Cmdleten **New-AzDataFactoryPipeline** skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f264c-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="f264c-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="f264c-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="f264c-110">Om du anger parametern *Force* ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f264c-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="f264c-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="f264c-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="f264c-112">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f264c-112">Create a data factory.</span></span> 
- <span data-ttu-id="f264c-113">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="f264c-113">Create linked services.</span></span> 
- <span data-ttu-id="f264c-114">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="f264c-114">Create datasets.</span></span> 
- <span data-ttu-id="f264c-115">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="f264c-115">Create a pipeline.</span></span>
<span data-ttu-id="f264c-116">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="f264c-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="f264c-117">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="f264c-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="f264c-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f264c-118">EXAMPLES</span></span>

### <span data-ttu-id="f264c-119">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="f264c-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="f264c-120">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="f264c-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="f264c-121">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="f264c-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="f264c-122">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="f264c-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="f264c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f264c-123">PARAMETERS</span></span>

### <span data-ttu-id="f264c-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f264c-124">-DataFactory</span></span>
<span data-ttu-id="f264c-125">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f264c-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f264c-126">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f264c-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f264c-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f264c-127">-DataFactoryName</span></span>
<span data-ttu-id="f264c-128">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f264c-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f264c-129">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f264c-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f264c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f264c-130">-DefaultProfile</span></span>
<span data-ttu-id="f264c-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f264c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f264c-132">-Fil</span><span class="sxs-lookup"><span data-stu-id="f264c-132">-File</span></span>
<span data-ttu-id="f264c-133">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av pipeline.</span><span class="sxs-lookup"><span data-stu-id="f264c-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f264c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f264c-134">-Force</span></span>
<span data-ttu-id="f264c-135">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f264c-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f264c-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="f264c-136">-Name</span></span>
<span data-ttu-id="f264c-137">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f264c-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f264c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f264c-138">-ResourceGroupName</span></span>
<span data-ttu-id="f264c-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f264c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f264c-140">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f264c-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f264c-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f264c-141">-Confirm</span></span>
<span data-ttu-id="f264c-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f264c-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f264c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f264c-143">-WhatIf</span></span>
<span data-ttu-id="f264c-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f264c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f264c-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f264c-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f264c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f264c-146">CommonParameters</span></span>
<span data-ttu-id="f264c-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f264c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f264c-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f264c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f264c-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f264c-149">INPUTS</span></span>

### <span data-ttu-id="f264c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f264c-150">System.String</span></span>

### <span data-ttu-id="f264c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f264c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f264c-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f264c-152">OUTPUTS</span></span>

### <span data-ttu-id="f264c-153">Microsoft. Azure. commands. DataFactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="f264c-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f264c-154">NOTES</span></span>
* <span data-ttu-id="f264c-155">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f264c-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f264c-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f264c-156">RELATED LINKS</span></span>

[<span data-ttu-id="f264c-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="f264c-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="f264c-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="f264c-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f264c-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f264c-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f264c-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

