---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258959"
---
# <span data-ttu-id="d8999-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="d8999-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="d8999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8999-102">SYNOPSIS</span></span>
<span data-ttu-id="d8999-103">Hämtar information om aktiviteten körs för en pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="d8999-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="d8999-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8999-104">SYNTAX</span></span>

### <span data-ttu-id="d8999-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d8999-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8999-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d8999-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8999-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8999-107">DESCRIPTION</span></span>
<span data-ttu-id="d8999-108">Cmdleten **Get-AzSynapseActivityRun** hämtar information om hur du kör i arbets ytan för den angivna pipelinen som inträffade under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="d8999-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="d8999-109">Du kan också ange filter för aktivitetens namn och status för kör.</span><span class="sxs-lookup"><span data-stu-id="d8999-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="d8999-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8999-110">EXAMPLES</span></span>

### <span data-ttu-id="d8999-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8999-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="d8999-112">Det här kommandot får information om all aktivitet körs i pipeline med namnet ContosoPipeline körs med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2018-09-01T21:00" och "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="d8999-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="d8999-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d8999-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="d8999-114">Det här kommandot får information om all aktivitet körs i pipeline med namnet ContosoPipeline körs med ID "f288712d-FB08-4cb8-96ef-82d3b9b30621" som inträffade mellan "2018-09-01T21:00" och "2018-09-30T21:00" till och med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="d8999-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="d8999-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8999-115">PARAMETERS</span></span>

### <span data-ttu-id="d8999-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d8999-116">-ActivityName</span></span>
<span data-ttu-id="d8999-117">Namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d8999-117">The name of the activity.</span></span>

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

### <span data-ttu-id="d8999-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8999-118">-DefaultProfile</span></span>
<span data-ttu-id="d8999-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8999-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8999-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d8999-120">-PipelineName</span></span>
<span data-ttu-id="d8999-121">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="d8999-121">The pipeline name.</span></span>

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

### <span data-ttu-id="d8999-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d8999-122">-PipelineRunId</span></span>
<span data-ttu-id="d8999-123">ID för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="d8999-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="d8999-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d8999-124">-RunStartedAfter</span></span>
<span data-ttu-id="d8999-125">Tiden då händelsen kör uppdaterades i ' ISO 8601 '-format.</span><span class="sxs-lookup"><span data-stu-id="d8999-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d8999-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d8999-126">-RunStartedBefore</span></span>
<span data-ttu-id="d8999-127">Tiden då händelsen kör uppdaterades i "ISO 8601"-format.</span><span class="sxs-lookup"><span data-stu-id="d8999-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d8999-128">-Status</span><span class="sxs-lookup"><span data-stu-id="d8999-128">-Status</span></span>
<span data-ttu-id="d8999-129">Status för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="d8999-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="d8999-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8999-130">-WorkspaceName</span></span>
<span data-ttu-id="d8999-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d8999-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d8999-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8999-132">-WorkspaceObject</span></span>
<span data-ttu-id="d8999-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8999-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d8999-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8999-134">CommonParameters</span></span>
<span data-ttu-id="d8999-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8999-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8999-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8999-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8999-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8999-137">INPUTS</span></span>

### <span data-ttu-id="d8999-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8999-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d8999-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8999-139">OUTPUTS</span></span>

### <span data-ttu-id="d8999-140">Microsoft. Azure. commands. Synapse. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="d8999-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="d8999-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8999-141">NOTES</span></span>

## <span data-ttu-id="d8999-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8999-142">RELATED LINKS</span></span>
