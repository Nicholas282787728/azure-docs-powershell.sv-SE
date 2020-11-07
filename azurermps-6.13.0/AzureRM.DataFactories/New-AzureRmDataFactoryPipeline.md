---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 7ad7eb0f87972c3a64b3fb966259d25d527c20c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575252"
---
# <span data-ttu-id="dbf48-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="dbf48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbf48-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf48-103">Skapar en pipeline i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="dbf48-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbf48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbf48-104">SYNTAX</span></span>

### <span data-ttu-id="dbf48-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="dbf48-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbf48-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dbf48-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf48-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbf48-107">DESCRIPTION</span></span>
<span data-ttu-id="dbf48-108">Cmdleten **New-AzureRmDataFactoryPipeline** skapar en pipeline i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dbf48-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="dbf48-109">Om du anger ett namn för en pipeline som redan finns ber cmdleten dig om bekräftelse innan den ersätter pipelinen.</span><span class="sxs-lookup"><span data-stu-id="dbf48-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="dbf48-110">Om du anger parametern *Force* ersätter cmdlet den befintliga pipeline utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dbf48-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="dbf48-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="dbf48-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="dbf48-112">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="dbf48-112">Create a data factory.</span></span> 
- <span data-ttu-id="dbf48-113">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="dbf48-113">Create linked services.</span></span> 
- <span data-ttu-id="dbf48-114">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="dbf48-114">Create datasets.</span></span> 
- <span data-ttu-id="dbf48-115">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="dbf48-115">Create a pipeline.</span></span>
<span data-ttu-id="dbf48-116">Om det redan finns en pipeline med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga pipeline med den nya pipelinen.</span><span class="sxs-lookup"><span data-stu-id="dbf48-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="dbf48-117">Om du bekräftar att det befintliga pipeline ska skrivas över ersätts även försäljnings förlopps definitionen.</span><span class="sxs-lookup"><span data-stu-id="dbf48-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="dbf48-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbf48-118">EXAMPLES</span></span>

### <span data-ttu-id="dbf48-119">Exempel 1: skapa en rörledning</span><span class="sxs-lookup"><span data-stu-id="dbf48-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="dbf48-120">Det här kommandot skapar en pipeline med namnet DPWikisample i data fabriken med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="dbf48-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="dbf48-121">Kommandot baserar sig på informationen i DPWikisample.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="dbf48-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="dbf48-122">Den här filen innehåller information om aktiviteter som kopierings aktivitet och HDInsight-aktivitet i pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbf48-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="dbf48-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbf48-123">PARAMETERS</span></span>

### <span data-ttu-id="dbf48-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dbf48-124">-DataFactory</span></span>
<span data-ttu-id="dbf48-125">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dbf48-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dbf48-126">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dbf48-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dbf48-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dbf48-127">-DataFactoryName</span></span>
<span data-ttu-id="dbf48-128">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="dbf48-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dbf48-129">Denna cmdlet skapar en pipeline för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dbf48-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dbf48-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf48-130">-DefaultProfile</span></span>
<span data-ttu-id="dbf48-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dbf48-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbf48-132">-Fil</span><span class="sxs-lookup"><span data-stu-id="dbf48-132">-File</span></span>
<span data-ttu-id="dbf48-133">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbf48-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="dbf48-134">-Force</span><span class="sxs-lookup"><span data-stu-id="dbf48-134">-Force</span></span>
<span data-ttu-id="dbf48-135">Anger att denna cmdlet ersätter en befintlig pipeline utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dbf48-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dbf48-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbf48-136">-Name</span></span>
<span data-ttu-id="dbf48-137">Anger namnet på den pipeline som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dbf48-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="dbf48-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf48-138">-ResourceGroupName</span></span>
<span data-ttu-id="dbf48-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="dbf48-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dbf48-140">Denna cmdlet skapar en pipeline för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dbf48-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dbf48-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbf48-141">-Confirm</span></span>
<span data-ttu-id="dbf48-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbf48-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf48-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf48-143">-WhatIf</span></span>
<span data-ttu-id="dbf48-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbf48-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf48-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbf48-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf48-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf48-146">CommonParameters</span></span>
<span data-ttu-id="dbf48-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf48-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf48-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf48-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf48-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbf48-149">INPUTS</span></span>

### <span data-ttu-id="dbf48-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dbf48-150">System.String</span></span>

### <span data-ttu-id="dbf48-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dbf48-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="dbf48-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbf48-152">OUTPUTS</span></span>

### <span data-ttu-id="dbf48-153">Microsoft. Azure. commands. DataFactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="dbf48-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbf48-154">NOTES</span></span>
* <span data-ttu-id="dbf48-155">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="dbf48-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dbf48-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbf48-156">RELATED LINKS</span></span>

[<span data-ttu-id="dbf48-157">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dbf48-158">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dbf48-159">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dbf48-160">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="dbf48-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="dbf48-161">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dbf48-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

