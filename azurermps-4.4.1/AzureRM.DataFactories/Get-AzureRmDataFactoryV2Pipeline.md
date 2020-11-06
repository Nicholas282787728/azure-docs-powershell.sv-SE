---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e0abd64298d74c52f2081e6d36f42b1ad2dee913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574719"
---
# <span data-ttu-id="f4e2b-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f4e2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e2b-103">Hämtar information om rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4e2b-104">SYNTAX</span></span>

### <span data-ttu-id="f4e2b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="f4e2b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e2b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f4e2b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e2b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4e2b-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e2b-108">Get-AzureRmDataFactoryV2Pipeline cmdlet får information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="f4e2b-109">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="f4e2b-110">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="f4e2b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4e2b-111">EXAMPLES</span></span>

### <span data-ttu-id="f4e2b-112">Exempel 1: få information om alla rörledningar</span><span class="sxs-lookup"><span data-stu-id="f4e2b-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="f4e2b-113">Det här kommandot får information om alla rörledningar i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="f4e2b-114">Du kan använda något av följande exempel kommandon.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="f4e2b-115">Den andra använder ett DataFactory-objekt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="f4e2b-116">Exempel 2: Hämta information om en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="f4e2b-117">Med det här kommandot får du information om pipeline med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="f4e2b-118">Kommandot skickar den informationen till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4e2b-119">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f4e2b-120">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="f4e2b-121">Exempel 3: Hämta egenskaper för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="f4e2b-122">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="f4e2b-123">Exempel 6: få information om indata för den första aktiviteten</span><span class="sxs-lookup"><span data-stu-id="f4e2b-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="f4e2b-124">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="f4e2b-125">Kommandot visar egenskapen indata för det första elementet i matrisen aktiviteter genom att använda Format-List cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="f4e2b-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4e2b-126">PARAMETERS</span></span>

### <span data-ttu-id="f4e2b-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4e2b-127">-DataFactory</span></span>
<span data-ttu-id="f4e2b-128">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="f4e2b-129">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e2b-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f4e2b-130">-DataFactoryName</span></span>
<span data-ttu-id="f4e2b-131">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f4e2b-132">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e2b-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4e2b-133">-Name</span></span>
<span data-ttu-id="f4e2b-134">Anger namnet på den rörledning som du vill få information om.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e2b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e2b-135">-ResourceGroupName</span></span>
<span data-ttu-id="f4e2b-136">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f4e2b-137">Denna cmdlet tar ledningar som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4e2b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e2b-138">-DefaultProfile</span></span>
<span data-ttu-id="f4e2b-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e2b-140">CommonParameters</span></span>
<span data-ttu-id="f4e2b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e2b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e2b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e2b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4e2b-143">INPUTS</span></span>

### <span data-ttu-id="f4e2b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e2b-144">System.String</span></span>
<span data-ttu-id="f4e2b-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f4e2b-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f4e2b-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4e2b-146">OUTPUTS</span></span>

### <span data-ttu-id="f4e2b-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4e2b-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f4e2b-148">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f4e2b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4e2b-149">NOTES</span></span>
<span data-ttu-id="f4e2b-150">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f4e2b-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f4e2b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4e2b-151">RELATED LINKS</span></span>

[<span data-ttu-id="f4e2b-152">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-152">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f4e2b-153">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-153">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f4e2b-154">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f4e2b-154">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
