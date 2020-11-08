---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272984"
---
# <span data-ttu-id="507e2-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="507e2-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="507e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="507e2-102">SYNOPSIS</span></span>
<span data-ttu-id="507e2-103">Skapar eller uppdaterar ett data flöde i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="507e2-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="507e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="507e2-104">SYNTAX</span></span>

### <span data-ttu-id="507e2-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="507e2-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507e2-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="507e2-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="507e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="507e2-107">DESCRIPTION</span></span>
<span data-ttu-id="507e2-108">Cmdleten **set-AzSynapseDataFlow** skapar ett data flöde eller uppdaterar ett befintligt data flöde i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="507e2-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="507e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="507e2-109">EXAMPLES</span></span>

### <span data-ttu-id="507e2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="507e2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="507e2-111">Det här kommandot skapar ett data flöde med namnet ContosoDataFlow i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="507e2-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="507e2-112">Kommandot baserar data flödet på informationen i DataFlow.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="507e2-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="507e2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="507e2-113">PARAMETERS</span></span>

### <span data-ttu-id="507e2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="507e2-114">-AsJob</span></span>
<span data-ttu-id="507e2-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="507e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="507e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507e2-116">-DefaultProfile</span></span>
<span data-ttu-id="507e2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="507e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="507e2-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="507e2-118">-DefinitionFile</span></span>
<span data-ttu-id="507e2-119">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="507e2-119">The JSON file path.</span></span>

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

### <span data-ttu-id="507e2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="507e2-120">-Name</span></span>
<span data-ttu-id="507e2-121">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="507e2-121">The data flow name.</span></span>

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

### <span data-ttu-id="507e2-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="507e2-122">-WorkspaceName</span></span>
<span data-ttu-id="507e2-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="507e2-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="507e2-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="507e2-124">-WorkspaceObject</span></span>
<span data-ttu-id="507e2-125">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="507e2-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="507e2-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="507e2-126">-Confirm</span></span>
<span data-ttu-id="507e2-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="507e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="507e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507e2-128">-WhatIf</span></span>
<span data-ttu-id="507e2-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="507e2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="507e2-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="507e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="507e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507e2-131">CommonParameters</span></span>
<span data-ttu-id="507e2-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507e2-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="507e2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507e2-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="507e2-134">INPUTS</span></span>

### <span data-ttu-id="507e2-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="507e2-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="507e2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="507e2-136">OUTPUTS</span></span>

### <span data-ttu-id="507e2-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="507e2-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="507e2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="507e2-138">NOTES</span></span>

## <span data-ttu-id="507e2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="507e2-139">RELATED LINKS</span></span>
