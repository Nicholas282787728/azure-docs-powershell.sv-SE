---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577072"
---
# <span data-ttu-id="799db-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="799db-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="799db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="799db-102">SYNOPSIS</span></span>
<span data-ttu-id="799db-103">Hämtar information om aktiviteten körs för en pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="799db-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="799db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="799db-104">SYNTAX</span></span>

### <span data-ttu-id="799db-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="799db-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="799db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="799db-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="799db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="799db-107">DESCRIPTION</span></span>
<span data-ttu-id="799db-108">Cmdleten **Get-AzureRmDataFactoryV2ActivityRun** hämtar information om hur man kör i Azure Data Factory för den angivna pipelinen som inträffade under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="799db-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="799db-109">Du kan dessutom ange filter för aktivitets namn, länkat tjänst namn som kördes och status för kör.</span><span class="sxs-lookup"><span data-stu-id="799db-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="799db-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="799db-110">EXAMPLES</span></span>

### <span data-ttu-id="799db-111">Exempel 1: Hämta alla aktiviteter för en pipeline-körning</span><span class="sxs-lookup"><span data-stu-id="799db-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="799db-112">Det här kommandot får information om all aktivitet körs i pipeline-körningen med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2017-09-01" och "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="799db-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="799db-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="799db-113">PARAMETERS</span></span>

### <span data-ttu-id="799db-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="799db-114">-ActivityName</span></span>
<span data-ttu-id="799db-115">Namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="799db-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="799db-116">-DataFactory</span></span>
<span data-ttu-id="799db-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="799db-117">The data factory object.</span></span>

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

### <span data-ttu-id="799db-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="799db-118">-DataFactoryName</span></span>
<span data-ttu-id="799db-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="799db-119">The data factory name.</span></span>

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

### <span data-ttu-id="799db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799db-120">-DefaultProfile</span></span>
<span data-ttu-id="799db-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="799db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="799db-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="799db-122">-LinkedServiceName</span></span>
<span data-ttu-id="799db-123">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="799db-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="799db-124">-PipelineRunId</span></span>
<span data-ttu-id="799db-125">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="799db-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799db-126">-ResourceGroupName</span></span>
<span data-ttu-id="799db-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="799db-127">The resource group name.</span></span>

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

### <span data-ttu-id="799db-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="799db-128">-RunStartedAfter</span></span>
<span data-ttu-id="799db-129">Den tid och det klock slag då förloppet körs.</span><span class="sxs-lookup"><span data-stu-id="799db-129">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="799db-130">-RunStartedBefore</span></span>
<span data-ttu-id="799db-131">Tiden då den tid då förloppet körs.</span><span class="sxs-lookup"><span data-stu-id="799db-131">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-132">-Status</span><span class="sxs-lookup"><span data-stu-id="799db-132">-Status</span></span>
<span data-ttu-id="799db-133">Status för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="799db-133">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799db-134">CommonParameters</span></span>
<span data-ttu-id="799db-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="799db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799db-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799db-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="799db-137">INPUTS</span></span>

### <span data-ttu-id="799db-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="799db-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="799db-139">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="799db-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="799db-140">System. String</span><span class="sxs-lookup"><span data-stu-id="799db-140">System.String</span></span>

## <span data-ttu-id="799db-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="799db-141">OUTPUTS</span></span>

### <span data-ttu-id="799db-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="799db-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="799db-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="799db-143">NOTES</span></span>

## <span data-ttu-id="799db-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="799db-144">RELATED LINKS</span></span>

[<span data-ttu-id="799db-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="799db-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="799db-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="799db-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

