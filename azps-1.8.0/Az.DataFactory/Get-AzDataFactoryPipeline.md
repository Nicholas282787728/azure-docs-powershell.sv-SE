---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754391"
---
# <span data-ttu-id="ea012-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ea012-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea012-102">SYNOPSIS</span></span>
<span data-ttu-id="ea012-103">Hämtar information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ea012-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="ea012-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea012-104">SYNTAX</span></span>

### <span data-ttu-id="ea012-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ea012-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea012-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ea012-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea012-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea012-107">DESCRIPTION</span></span>
<span data-ttu-id="ea012-108">Cmdleten **Get-AzDataFactoryPipeline** hämtar information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ea012-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="ea012-109">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="ea012-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="ea012-110">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ea012-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="ea012-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea012-111">EXAMPLES</span></span>

### <span data-ttu-id="ea012-112">Exempel 1: få information om alla rörledningar</span><span class="sxs-lookup"><span data-stu-id="ea012-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="ea012-113">Det här kommandot får information om alla rörledningar i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ea012-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="ea012-114">Du kan antingen välja något av följande exempel kommandon.</span><span class="sxs-lookup"><span data-stu-id="ea012-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="ea012-115">Den andra använder ett **DataFactory** -objekt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="ea012-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="ea012-116">Exempel 2: Hämta information om en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="ea012-117">Med det här kommandot får du information om pipeline med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ea012-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ea012-118">Kommandot skickar den informationen till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ea012-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea012-119">Denna cmdlet formaterar resultaten.</span><span class="sxs-lookup"><span data-stu-id="ea012-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="ea012-120">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="ea012-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="ea012-121">Exempel 3: Hämta egenskaper för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="ea012-122">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF, och använder sedan standard punkt notation för att visa egenskapen **Egenskaper** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea012-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="ea012-123">Exempel 4: Hämta aktiviteter för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="ea012-124">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen **Activities** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea012-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="ea012-125">Exempel 5: Hämta kör tids information för en specifik pipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="ea012-126">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF, och använder sedan standard punkt notation för att visa den **RuntimeInfo** -egenskap som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea012-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="ea012-127">Exempel 6: få information om indata för den första aktiviteten</span><span class="sxs-lookup"><span data-stu-id="ea012-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="ea012-128">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen **Activities** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea012-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="ea012-129">Kommandot visar egenskapen **indata** för det första elementet i matrisen **Activities** med hjälp av **format-lista**.</span><span class="sxs-lookup"><span data-stu-id="ea012-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="ea012-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea012-130">PARAMETERS</span></span>

### <span data-ttu-id="ea012-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ea012-131">-DataFactory</span></span>
<span data-ttu-id="ea012-132">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ea012-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ea012-133">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ea012-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea012-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ea012-134">-DataFactoryName</span></span>
<span data-ttu-id="ea012-135">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ea012-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ea012-136">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ea012-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea012-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea012-137">-DefaultProfile</span></span>
<span data-ttu-id="ea012-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ea012-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea012-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea012-139">-Name</span></span>
<span data-ttu-id="ea012-140">Anger namnet på den rörledning som du vill få information om.</span><span class="sxs-lookup"><span data-stu-id="ea012-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="ea012-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea012-141">-ResourceGroupName</span></span>
<span data-ttu-id="ea012-142">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ea012-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ea012-143">Denna cmdlet tar ledningar som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ea012-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea012-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea012-144">CommonParameters</span></span>
<span data-ttu-id="ea012-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea012-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea012-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea012-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea012-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea012-147">INPUTS</span></span>

### <span data-ttu-id="ea012-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ea012-148">System.String</span></span>

### <span data-ttu-id="ea012-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ea012-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ea012-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea012-150">OUTPUTS</span></span>

### <span data-ttu-id="ea012-151">Microsoft. Azure. commands. DataFactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="ea012-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea012-152">NOTES</span></span>
* <span data-ttu-id="ea012-153">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="ea012-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ea012-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea012-154">RELATED LINKS</span></span>

[<span data-ttu-id="ea012-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ea012-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="ea012-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="ea012-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ea012-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ea012-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ea012-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

