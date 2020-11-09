---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321039"
---
# <span data-ttu-id="ecd32-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="ecd32-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="ecd32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecd32-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd32-103">Hämtar information om aktiviteten körs för en pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="ecd32-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="ecd32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecd32-104">SYNTAX</span></span>

### <span data-ttu-id="ecd32-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ecd32-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecd32-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ecd32-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecd32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecd32-107">DESCRIPTION</span></span>
<span data-ttu-id="ecd32-108">Cmdleten **Get-AzDataFactoryV2ActivityRun** hämtar information om hur man kör i Azure Data Factory för den angivna pipelinen som inträffade under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="ecd32-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="ecd32-109">Du kan dessutom ange filter för aktivitets namn, länkat tjänst namn som kördes och status för kör.</span><span class="sxs-lookup"><span data-stu-id="ecd32-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="ecd32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecd32-110">EXAMPLES</span></span>

### <span data-ttu-id="ecd32-111">Exempel 1: Hämta alla aktiviteter för en pipeline-körning</span><span class="sxs-lookup"><span data-stu-id="ecd32-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="ecd32-112">Det här kommandot får information om all aktivitet körs i pipeline-körningen med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2017-09-01" och "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="ecd32-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="ecd32-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecd32-113">PARAMETERS</span></span>

### <span data-ttu-id="ecd32-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="ecd32-114">-ActivityName</span></span>
<span data-ttu-id="ecd32-115">Namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="ecd32-115">The name of the activity.</span></span>

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

### <span data-ttu-id="ecd32-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd32-116">-DataFactory</span></span>
<span data-ttu-id="ecd32-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="ecd32-117">The data factory object.</span></span>

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

### <span data-ttu-id="ecd32-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ecd32-118">-DataFactoryName</span></span>
<span data-ttu-id="ecd32-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ecd32-119">The data factory name.</span></span>

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

### <span data-ttu-id="ecd32-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd32-120">-DefaultProfile</span></span>
<span data-ttu-id="ecd32-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd32-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecd32-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="ecd32-122">-PipelineRunId</span></span>
<span data-ttu-id="ecd32-123">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="ecd32-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="ecd32-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd32-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecd32-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ecd32-125">The resource group name.</span></span>

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

### <span data-ttu-id="ecd32-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="ecd32-126">-RunStartedAfter</span></span>
<span data-ttu-id="ecd32-127">Den tid och det klock slag då förloppet körs.</span><span class="sxs-lookup"><span data-stu-id="ecd32-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="ecd32-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="ecd32-128">-RunStartedBefore</span></span>
<span data-ttu-id="ecd32-129">Tiden då den tid då förloppet körs.</span><span class="sxs-lookup"><span data-stu-id="ecd32-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="ecd32-130">-Status</span><span class="sxs-lookup"><span data-stu-id="ecd32-130">-Status</span></span>
<span data-ttu-id="ecd32-131">Status för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="ecd32-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="ecd32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd32-132">CommonParameters</span></span>
<span data-ttu-id="ecd32-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd32-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd32-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd32-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecd32-135">INPUTS</span></span>

### <span data-ttu-id="ecd32-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecd32-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="ecd32-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd32-137">System.String</span></span>

## <span data-ttu-id="ecd32-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecd32-138">OUTPUTS</span></span>

### <span data-ttu-id="ecd32-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="ecd32-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="ecd32-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecd32-140">NOTES</span></span>

## <span data-ttu-id="ecd32-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecd32-141">RELATED LINKS</span></span>

[<span data-ttu-id="ecd32-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ecd32-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ecd32-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ecd32-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

