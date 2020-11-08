---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258448"
---
# <span data-ttu-id="d5a0e-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d5a0e-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="d5a0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a0e-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="d5a0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5a0e-104">SYNTAX</span></span>

### <span data-ttu-id="d5a0e-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d5a0e-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a0e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d5a0e-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a0e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5a0e-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a0e-108">Kommandot **Get-AzSynapseTriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="d5a0e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5a0e-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a0e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d5a0e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="d5a0e-111">Det här kommandot visar information om hur du kör för ContosoTrigger i arbets ytans ContosoWorkspace som påbörjats mellan "2018-09-01T21:00" och "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="d5a0e-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="d5a0e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d5a0e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="d5a0e-113">Det här kommandot visar information om hur du kör för ContosoTrigger i arbets ytans ContosoWorkspace som påbörjats mellan "2018-09-01T21:00" och "2019-09-01T21:00" genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="d5a0e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5a0e-114">PARAMETERS</span></span>

### <span data-ttu-id="d5a0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a0e-115">-DefaultProfile</span></span>
<span data-ttu-id="d5a0e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a0e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5a0e-117">-Name</span></span>
<span data-ttu-id="d5a0e-118">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0e-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d5a0e-119">-RunStartedAfter</span></span>
<span data-ttu-id="d5a0e-120">Tiden då händelsen kör uppdaterades i ' ISO 8601 '-format.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d5a0e-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d5a0e-121">-RunStartedBefore</span></span>
<span data-ttu-id="d5a0e-122">Tiden då händelsen kör uppdaterades i "ISO 8601"-format.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d5a0e-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5a0e-123">-WorkspaceName</span></span>
<span data-ttu-id="d5a0e-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d5a0e-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5a0e-125">-WorkspaceObject</span></span>
<span data-ttu-id="d5a0e-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d5a0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a0e-127">CommonParameters</span></span>
<span data-ttu-id="d5a0e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a0e-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a0e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5a0e-130">INPUTS</span></span>

### <span data-ttu-id="d5a0e-131">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5a0e-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d5a0e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5a0e-132">OUTPUTS</span></span>

### <span data-ttu-id="d5a0e-133">Microsoft. Azure. commands. Synapse. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d5a0e-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="d5a0e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5a0e-134">NOTES</span></span>

## <span data-ttu-id="d5a0e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5a0e-135">RELATED LINKS</span></span>
