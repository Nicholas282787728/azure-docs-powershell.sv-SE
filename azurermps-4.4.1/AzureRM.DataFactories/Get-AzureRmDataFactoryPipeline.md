---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 9188e0084c73ab984c898e94cbf94c33cde52995
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585700"
---
# <span data-ttu-id="40fae-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="40fae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40fae-102">SYNOPSIS</span></span>
<span data-ttu-id="40fae-103">Hämtar information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="40fae-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40fae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40fae-104">SYNTAX</span></span>

### <span data-ttu-id="40fae-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="40fae-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40fae-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="40fae-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40fae-107">DESCRIPTION</span></span>
<span data-ttu-id="40fae-108">Cmdleten **Get-AzureRmDataFactoryPipeline** hämtar information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="40fae-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="40fae-109">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="40fae-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="40fae-110">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="40fae-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="40fae-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40fae-111">EXAMPLES</span></span>

### <span data-ttu-id="40fae-112">Exempel 1: få information om alla rörledningar</span><span class="sxs-lookup"><span data-stu-id="40fae-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="40fae-113">Det här kommandot får information om alla rörledningar i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="40fae-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="40fae-114">Du kan antingen välja något av följande exempel kommandon.</span><span class="sxs-lookup"><span data-stu-id="40fae-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="40fae-115">Den andra använder ett **DataFactory** -objekt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="40fae-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="40fae-116">Exempel 2: Hämta information om en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="40fae-117">Med det här kommandot får du information om pipeline med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="40fae-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="40fae-118">Kommandot skickar den informationen till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="40fae-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40fae-119">Denna cmdlet formaterar resultaten.</span><span class="sxs-lookup"><span data-stu-id="40fae-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="40fae-120">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="40fae-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="40fae-121">Exempel 3: Hämta egenskaper för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="40fae-122">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF, och använder sedan standard punkt notation för att visa egenskapen **Egenskaper** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="40fae-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="40fae-123">Exempel 4: Hämta aktiviteter för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

<span data-ttu-id="40fae-124">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen **Activities** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="40fae-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="40fae-125">Exempel 5: Hämta kör tids information för en specifik pipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="40fae-126">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF, och använder sedan standard punkt notation för att visa den **RuntimeInfo** -egenskap som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="40fae-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="40fae-127">Exempel 6: få information om indata för den första aktiviteten</span><span class="sxs-lookup"><span data-stu-id="40fae-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="40fae-128">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen **Activities** som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="40fae-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="40fae-129">Kommandot visar egenskapen **indata** för det första elementet i matrisen **Activities** med hjälp av **format-lista**.</span><span class="sxs-lookup"><span data-stu-id="40fae-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="40fae-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40fae-130">PARAMETERS</span></span>

### <span data-ttu-id="40fae-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="40fae-131">-DataFactory</span></span>
<span data-ttu-id="40fae-132">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="40fae-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="40fae-133">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="40fae-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40fae-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40fae-134">-DataFactoryName</span></span>
<span data-ttu-id="40fae-135">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="40fae-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="40fae-136">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="40fae-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40fae-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="40fae-137">-Name</span></span>
<span data-ttu-id="40fae-138">Anger namnet på den rörledning som du vill få information om.</span><span class="sxs-lookup"><span data-stu-id="40fae-138">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="40fae-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fae-139">-ResourceGroupName</span></span>
<span data-ttu-id="40fae-140">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="40fae-140">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="40fae-141">Denna cmdlet tar ledningar som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="40fae-141">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40fae-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fae-142">-DefaultProfile</span></span>
<span data-ttu-id="40fae-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40fae-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40fae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fae-144">CommonParameters</span></span>
<span data-ttu-id="40fae-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fae-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fae-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fae-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40fae-147">INPUTS</span></span>

## <span data-ttu-id="40fae-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40fae-148">OUTPUTS</span></span>

### <span data-ttu-id="40fae-149">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. commands. Utilities. PSPipeline, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. kommandon. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-149">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSPipeline, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="40fae-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40fae-150">NOTES</span></span>
* <span data-ttu-id="40fae-151">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="40fae-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="40fae-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40fae-152">RELATED LINKS</span></span>

[<span data-ttu-id="40fae-153">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-153">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40fae-154">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-154">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40fae-155">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-155">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40fae-156">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="40fae-156">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="40fae-157">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40fae-157">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


