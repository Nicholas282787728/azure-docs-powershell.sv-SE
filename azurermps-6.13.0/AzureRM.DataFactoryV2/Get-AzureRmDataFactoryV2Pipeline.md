---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bff3a3910393a3708e416396fa21573adadebc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756200"
---
# <span data-ttu-id="fe245-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="fe245-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe245-102">SYNOPSIS</span></span>
<span data-ttu-id="fe245-103">Hämtar information om rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fe245-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe245-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe245-104">SYNTAX</span></span>

### <span data-ttu-id="fe245-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="fe245-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe245-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fe245-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe245-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe245-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe245-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe245-108">DESCRIPTION</span></span>
<span data-ttu-id="fe245-109">Get-AzureRmDataFactoryV2Pipeline cmdlet får information om rörledningar i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fe245-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="fe245-110">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="fe245-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="fe245-111">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fe245-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="fe245-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe245-112">EXAMPLES</span></span>

### <span data-ttu-id="fe245-113">Exempel 1: få information om alla rörledningar</span><span class="sxs-lookup"><span data-stu-id="fe245-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="fe245-114">Det här kommandot får information om alla rörledningar i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fe245-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="fe245-115">Du kan använda något av följande exempel kommandon.</span><span class="sxs-lookup"><span data-stu-id="fe245-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="fe245-116">Den andra använder ett DataFactory-objekt som en parameter.</span><span class="sxs-lookup"><span data-stu-id="fe245-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="fe245-117">Exempel 2: Hämta information om en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="fe245-118">Med det här kommandot får du information om pipeline med namnet DPWikisample i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fe245-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="fe245-119">Kommandot skickar den informationen till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="fe245-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe245-120">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="fe245-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="fe245-121">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="fe245-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="fe245-122">Exempel 3: Hämta egenskaper för en viss pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="fe245-123">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe245-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="fe245-124">Exempel 6: få information om indata för den första aktiviteten</span><span class="sxs-lookup"><span data-stu-id="fe245-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="fe245-125">Det här kommandot får information för pipelinen med namnet DPWikisample i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa egenskapen Activities som är associerad med den pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe245-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="fe245-126">Kommandot visar egenskapen indata för det första elementet i matrisen aktiviteter genom att använda Format-List cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe245-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="fe245-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe245-127">PARAMETERS</span></span>

### <span data-ttu-id="fe245-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe245-128">-DataFactory</span></span>
<span data-ttu-id="fe245-129">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="fe245-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="fe245-130">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe245-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe245-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe245-131">-DataFactoryName</span></span>
<span data-ttu-id="fe245-132">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="fe245-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fe245-133">Denna cmdlet tar ledningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe245-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe245-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe245-134">-DefaultProfile</span></span>
<span data-ttu-id="fe245-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe245-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe245-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe245-136">-Name</span></span>
<span data-ttu-id="fe245-137">Anger namnet på den rörledning som du vill få information om.</span><span class="sxs-lookup"><span data-stu-id="fe245-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="fe245-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe245-138">-ResourceGroupName</span></span>
<span data-ttu-id="fe245-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="fe245-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fe245-140">Denna cmdlet tar ledningar som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fe245-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe245-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe245-141">-ResourceId</span></span>
<span data-ttu-id="fe245-142">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="fe245-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fe245-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe245-143">CommonParameters</span></span>
<span data-ttu-id="fe245-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe245-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe245-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe245-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe245-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe245-146">INPUTS</span></span>

### <span data-ttu-id="fe245-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fe245-147">System.String</span></span>

### <span data-ttu-id="fe245-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fe245-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="fe245-149">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fe245-149">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="fe245-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe245-150">OUTPUTS</span></span>

### <span data-ttu-id="fe245-151">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="fe245-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe245-152">NOTES</span></span>
<span data-ttu-id="fe245-153">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="fe245-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fe245-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe245-154">RELATED LINKS</span></span>

[<span data-ttu-id="fe245-155">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fe245-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fe245-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe245-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
