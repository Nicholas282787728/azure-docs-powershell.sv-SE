---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 313fcacf071dcee53c5141fe97c33bc1a477fe69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927850"
---
# <span data-ttu-id="256c5-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="256c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="256c5-102">SYNOPSIS</span></span>
<span data-ttu-id="256c5-103">Hämtar information om rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="256c5-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="256c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="256c5-104">SYNTAX</span></span>

### <span data-ttu-id="256c5-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="256c5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="256c5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="256c5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="256c5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="256c5-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="256c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="256c5-108">DESCRIPTION</span></span>
<span data-ttu-id="256c5-109">Get-AzDataFactoryV2Pipeline cmdlet får information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="256c5-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="256c5-110">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="256c5-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="256c5-111">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="256c5-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="256c5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="256c5-112">EXAMPLES</span></span>

### <span data-ttu-id="256c5-113">Exempel 1: få information om alla rörledningar</span><span class="sxs-lookup"><span data-stu-id="256c5-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="256c5-114">Det här kommandot får information om alla rörledningar i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="256c5-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="256c5-115">Du kan använda något av följande exempel kommandon.</span><span class="sxs-lookup"><span data-stu-id="256c5-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="256c5-116">Den andra använder ett DataFactory-objekt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="256c5-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="256c5-117">Exempel 2: Hämta information om en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="256c5-118">Med det här kommandot får du information om pipeline med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="256c5-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="256c5-119">Kommandot skickar den informationen till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="256c5-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="256c5-120">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="256c5-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="256c5-121">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="256c5-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="256c5-122">Exempel 3: Hämta egenskaper för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="256c5-123">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="256c5-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="256c5-124">Exempel 6: få information om indata för den första aktiviteten</span><span class="sxs-lookup"><span data-stu-id="256c5-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="256c5-125">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="256c5-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="256c5-126">Kommandot visar egenskapen indata för det första elementet i matrisen aktiviteter genom att använda Format-List cmdlet.</span><span class="sxs-lookup"><span data-stu-id="256c5-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="256c5-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="256c5-127">PARAMETERS</span></span>

### <span data-ttu-id="256c5-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="256c5-128">-DataFactory</span></span>
<span data-ttu-id="256c5-129">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="256c5-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="256c5-130">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="256c5-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="256c5-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="256c5-131">-DataFactoryName</span></span>
<span data-ttu-id="256c5-132">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="256c5-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="256c5-133">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="256c5-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="256c5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256c5-134">-DefaultProfile</span></span>
<span data-ttu-id="256c5-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="256c5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="256c5-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="256c5-136">-Name</span></span>
<span data-ttu-id="256c5-137">Anger namnet på den rörledning som du vill få information om.</span><span class="sxs-lookup"><span data-stu-id="256c5-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256c5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256c5-138">-ResourceGroupName</span></span>
<span data-ttu-id="256c5-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="256c5-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="256c5-140">Denna cmdlet tar ledningar som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="256c5-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="256c5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="256c5-141">-ResourceId</span></span>
<span data-ttu-id="256c5-142">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="256c5-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="256c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256c5-143">CommonParameters</span></span>
<span data-ttu-id="256c5-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="256c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256c5-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="256c5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256c5-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="256c5-146">INPUTS</span></span>

### <span data-ttu-id="256c5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="256c5-147">System.String</span></span>

### <span data-ttu-id="256c5-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="256c5-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="256c5-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="256c5-149">OUTPUTS</span></span>

### <span data-ttu-id="256c5-150">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="256c5-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="256c5-151">NOTES</span></span>
<span data-ttu-id="256c5-152">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="256c5-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="256c5-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="256c5-153">RELATED LINKS</span></span>

[<span data-ttu-id="256c5-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="256c5-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="256c5-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="256c5-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()