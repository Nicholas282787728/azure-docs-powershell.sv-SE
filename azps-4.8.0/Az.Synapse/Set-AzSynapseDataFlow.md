---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261186"
---
# <span data-ttu-id="eeb0a-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="eeb0a-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="eeb0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eeb0a-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb0a-103">Skapar eller uppdaterar ett data flöde i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="eeb0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eeb0a-104">SYNTAX</span></span>

### <span data-ttu-id="eeb0a-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="eeb0a-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb0a-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="eeb0a-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb0a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eeb0a-107">DESCRIPTION</span></span>
<span data-ttu-id="eeb0a-108">Cmdleten **set-AzSynapseDataFlow** skapar ett data flöde eller uppdaterar ett befintligt data flöde i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="eeb0a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eeb0a-109">EXAMPLES</span></span>

### <span data-ttu-id="eeb0a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eeb0a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="eeb0a-111">Det här kommandot skapar ett data flöde med namnet ContosoDataFlow i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="eeb0a-112">Kommandot baserar data flödet på informationen i DataFlow.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="eeb0a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eeb0a-113">PARAMETERS</span></span>

### <span data-ttu-id="eeb0a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeb0a-114">-AsJob</span></span>
<span data-ttu-id="eeb0a-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eeb0a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb0a-116">-DefaultProfile</span></span>
<span data-ttu-id="eeb0a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb0a-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="eeb0a-118">-DefinitionFile</span></span>
<span data-ttu-id="eeb0a-119">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="eeb0a-120">-Name</span></span>
<span data-ttu-id="eeb0a-121">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eeb0a-122">-WorkspaceName</span></span>
<span data-ttu-id="eeb0a-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="eeb0a-124">-WorkspaceObject</span></span>
<span data-ttu-id="eeb0a-125">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eeb0a-126">-Confirm</span></span>
<span data-ttu-id="eeb0a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb0a-128">-WhatIf</span></span>
<span data-ttu-id="eeb0a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb0a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb0a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb0a-131">CommonParameters</span></span>
<span data-ttu-id="eeb0a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb0a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb0a-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeb0a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb0a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eeb0a-134">INPUTS</span></span>

### <span data-ttu-id="eeb0a-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eeb0a-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="eeb0a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eeb0a-136">OUTPUTS</span></span>

### <span data-ttu-id="eeb0a-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="eeb0a-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="eeb0a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eeb0a-138">NOTES</span></span>

## <span data-ttu-id="eeb0a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eeb0a-139">RELATED LINKS</span></span>
