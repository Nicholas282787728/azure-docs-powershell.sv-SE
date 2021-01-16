---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397312"
---
# <span data-ttu-id="0c3ab-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="0c3ab-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="0c3ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3ab-103">Hämtar information om aktiviteten körs för en pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="0c3ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c3ab-104">SYNTAX</span></span>

### <span data-ttu-id="0c3ab-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="0c3ab-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c3ab-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="0c3ab-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c3ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="0c3ab-108">Cmdleten **Get-AzSynapseActivityRun** hämtar information om hur du kör i arbets ytan för den angivna pipelinen som inträffade under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="0c3ab-109">Du kan också ange filter för aktivitetens namn och status för kör.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="0c3ab-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c3ab-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3ab-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0c3ab-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="0c3ab-112">Det här kommandot får information om all aktivitet körs i pipeline med namnet ContosoPipeline körs med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2018-09-01T21:00" och "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="0c3ab-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="0c3ab-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0c3ab-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="0c3ab-114">Det här kommandot får information om all aktivitet körs i pipeline med namnet ContosoPipeline körs med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2018-09-01T21:00" och "2018-09-30T21:00" till och med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="0c3ab-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c3ab-115">PARAMETERS</span></span>

### <span data-ttu-id="0c3ab-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="0c3ab-116">-ActivityName</span></span>
<span data-ttu-id="0c3ab-117">Namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-117">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3ab-118">-DefaultProfile</span></span>
<span data-ttu-id="0c3ab-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3ab-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0c3ab-120">-PipelineName</span></span>
<span data-ttu-id="0c3ab-121">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="0c3ab-122">-PipelineRunId</span></span>
<span data-ttu-id="0c3ab-123">ID för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="0c3ab-124">-RunStartedAfter</span></span>
<span data-ttu-id="0c3ab-125">Tiden då händelsen kör uppdaterades i ' ISO 8601 '-format.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="0c3ab-126">-RunStartedBefore</span></span>
<span data-ttu-id="0c3ab-127">Tiden då händelsen kör uppdaterades i "ISO 8601"-format.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-128">-Status</span><span class="sxs-lookup"><span data-stu-id="0c3ab-128">-Status</span></span>
<span data-ttu-id="0c3ab-129">Status för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-129">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c3ab-130">-WorkspaceName</span></span>
<span data-ttu-id="0c3ab-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0c3ab-132">-WorkspaceObject</span></span>
<span data-ttu-id="0c3ab-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3ab-134">CommonParameters</span></span>
<span data-ttu-id="0c3ab-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3ab-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c3ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3ab-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c3ab-137">INPUTS</span></span>

### <span data-ttu-id="0c3ab-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c3ab-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0c3ab-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c3ab-139">OUTPUTS</span></span>

### <span data-ttu-id="0c3ab-140">Microsoft. Azure. commands. Synapse. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="0c3ab-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="0c3ab-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c3ab-141">NOTES</span></span>

## <span data-ttu-id="0c3ab-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c3ab-142">RELATED LINKS</span></span>
