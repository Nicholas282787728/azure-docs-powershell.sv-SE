---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323550"
---
# <span data-ttu-id="4efef-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="4efef-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="4efef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4efef-102">SYNOPSIS</span></span>
<span data-ttu-id="4efef-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="4efef-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4efef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4efef-104">SYNTAX</span></span>

### <span data-ttu-id="4efef-105">GetByNameAndId (standard)</span><span class="sxs-lookup"><span data-stu-id="4efef-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4efef-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="4efef-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4efef-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="4efef-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4efef-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="4efef-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4efef-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4efef-109">DESCRIPTION</span></span>
<span data-ttu-id="4efef-110">Kommandot **Get-AzSynapsePipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="4efef-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4efef-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="4efef-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4efef-112">Om PipelineRunId inte anges visas information om alla körningar för de rörledningar som inträffade mellan värdena för RunStartedAfter och RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="4efef-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="4efef-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4efef-113">EXAMPLES</span></span>

### <span data-ttu-id="4efef-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4efef-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="4efef-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="4efef-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4efef-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4efef-116">PARAMETERS</span></span>

### <span data-ttu-id="4efef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efef-117">-DefaultProfile</span></span>
<span data-ttu-id="4efef-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4efef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4efef-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4efef-119">-PipelineName</span></span>
<span data-ttu-id="4efef-120">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="4efef-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4efef-121">-PipelineRunId</span></span>
<span data-ttu-id="4efef-122">ID för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="4efef-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="4efef-123">-RunStartedAfter</span></span>
<span data-ttu-id="4efef-124">Tiden då händelsen kör uppdaterades i ' ISO 8601 '-format.</span><span class="sxs-lookup"><span data-stu-id="4efef-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="4efef-125">-RunStartedBefore</span></span>
<span data-ttu-id="4efef-126">Tiden då händelsen kör uppdaterades i "ISO 8601"-format.</span><span class="sxs-lookup"><span data-stu-id="4efef-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4efef-127">-WorkspaceName</span></span>
<span data-ttu-id="4efef-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4efef-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4efef-129">-WorkspaceObject</span></span>
<span data-ttu-id="4efef-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4efef-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4efef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efef-131">CommonParameters</span></span>
<span data-ttu-id="4efef-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efef-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4efef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efef-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4efef-134">INPUTS</span></span>

### <span data-ttu-id="4efef-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4efef-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4efef-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4efef-136">OUTPUTS</span></span>

### <span data-ttu-id="4efef-137">Microsoft. Azure. commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4efef-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4efef-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4efef-138">NOTES</span></span>

## <span data-ttu-id="4efef-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4efef-139">RELATED LINKS</span></span>
